<template>
    <h2 class="titulo">{{ Titulo }}</h2>
    <h5 class="subTitulo">{{ Subtitulo }}</h5>
    <div class="row">
        
        <form style="margin: 5% 0px 0px 5%;" >
            <div class="form-group">
                <label class="tituloInput" for="name">Especialidade Principal*</label>
                <select type="text" class="form-control inputSelect" placeholder="Selecione a especialidade">
                    <option selected>Selecione a especialidade</option>
                    <option value="Cardiologia">Cardiologia</option>
                    <option value="Dermatologia">Dermatologia</option>
                    <option value="Neurologia">Neurologia</option>
                    <option value="Oftalmologia">Oftalmologia</option>
                    <option value="Psiquiatria">Psiquiatria</option>
                    <option value="Urologia">Urologia</option>
                </select>
            </div>

            <div class="form-group">
                <label class="tituloInput" for="name">Especialidade Principal*</label>
                    <div class="input-group-prepend">
                        <span style="background-color:#483698;color:#fff;font-weight:bold;" class="input-group-text">R$</span>
                        <input type="number" style="margin-left:-10px;" class="form-control precoInput" placeholder="Valor">
                    </div>
                        
            </div>
            
            <label class="tituloInput" for="name">Formas de pagamento da consulta*</label>
            <div class="box-check">
                <input type="checkbox" style="display:flex;" >
                <p>Pix</p>
            </div>

            <div class="row ">
                <div class="col-md-4">
                    <div class="progress" style="height: 25px;margin-top:30px;">
                        <div class="progress-bar" role="progressbar"
                         style="width: 100%;background-color: rgb(72, 54, 152);" 
                         aria-valuenow="25" aria-valuemin="0" 
                         aria-valuemax="100">
                         </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <h6 class="contagem" for="CPF">2 de 2</h6>
                </div>
            </div>
            <button @click="$router.push('cadastro')" type="submit" class="btn">PRÓXIMO</button>
        </form>
    <img src="../../assets/desktop-pagina-2.png" style="width:300px;height:300px;" class="rounded" >
    </div>
        
</template>

<script>
    //Mascara de CPF
        document.addEventListener('keydown', function(event) { //pega o evento de precionar uma tecla
        if(event.keyCode != 46 && event.keyCode != 8){//verifica se a tecla precionada nao e um backspace e delete
        var i = document.getElementById("CPF").value.length; //aqui pega o tamanho do input
        if (i === 3 || i === 7) //aqui faz a divisoes colocando um ponto no terceiro e setimo indice
        document.getElementById("CPF").value = document.getElementById("CPF").value + ".";
        else if (i === 11) //aqui faz a divisao colocando o tracinho no decimo primeiro indice
        document.getElementById("CPF").value = document.getElementById("CPF").value + "-";
    }
    });
    //Mascara de Numero Celular
    //     document.addEventListener('keydown', function(event) { //pega o evento de precionar uma tecla
    //     if(event.keyCode != 46 && event.keyCode != 8){//verifica se a tecla precionada nao e um backspace e delete
    //     var i = document.getElementById("phone").value.length; //aqui pega o tamanho do input
    //     if (i === 0 ) //aqui faz a divisoes colocando um ( 
    //     document.getElementById("phone").value = document.getElementById("phone").value + "(";
    //     if (i === 3 ) //aqui faz a divisoes colocando um )
    //     document.getElementById("phone").value = document.getElementById("phone").value + ")";
    //     if (i === 5 ) //aqui faz a divisoes colocando um espaco em branco apos o 5 indice
    //     document.getElementById("phone").value = document.getElementById("phone").value + " ";
    //     else if (i === 10) //aqui faz a divisao colocando o tracinho no decimo indice
    //     document.getElementById("phone").value = document.getElementById("phone").value + "-";
    // }
    // });
    export default{
        name: 'FormAtendimento',
        data() {
            return{        
                Titulo: 'Sobre o atendimento',
                Subtitulo: 'Detalhes do atendimento'
            }
        },
        methods: {
        //Metodo para Input Number Only 
        NumbersOnly(evt) {
        evt = (evt) ? evt : window.event;
        var charCode = (evt.which) ? evt.which : evt.keyCode;
        if ((charCode > 31 && (charCode < 48 || charCode > 57)) && charCode !== 46) {
            evt.preventDefault();;
        } else {
            return true;
            }
            }
        }
        }
</script>

<style scoped>
    .tituloInput{
        max-width: 300px;
        min-width: 100px;
        display: flex;
    }
    .inputName{
        width: 400px;
    }
    .precoInput{
        width: 210px;
    }

    input, select{
        border-color: #483698;
    }

    input:focus, select:focus{
        border-color: #483698;  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(72, 54, 152, 0.6);
        box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(72, 54, 152, 0.6);
    }

    h6{
        font-family: 'Comfortaa', cursive;
        color:#483698;
    }
    .formTotal{
        margin-left:4%;
    }
    button{
        margin-bottom:30px;
        border-radius: 15px;
        width:400px;
        margin-top:15px;
        text-align: center;
        background-color:rgb(72, 54, 152);
        color:#fff;
    }
    .progress{
        width:300px;
    }
    .contagem{
        margin-top:30px;
        font-size:20px;
        margin-right:-300px;
    }
    .box-check{
        width: 90%;
        font-family: 'Open Sans', sans-serif;
        height: 30px;
        background-color: #F9F9F9;
        border-radius: 10px;
        box-shadow:  3px 3px 2px rgba(0, 0, 0, 0.09)
    }

    /* Escondendo as flechinhas do Input Number  */
    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }
    input[type=number] {
        -moz-appearance:textfield; /* Firefox */
    }

    /* Deixando Responsivo  */
    @media (max-width: 600px)
    {
        .inputName{
            width: 90%;
        }
        .inputSelect{
            width: 150px;
        }
        .inputNumber{
            width: 70%;
        }
        img{
            display: none;
        }
        .progress{
            width: 250px;
        }
        .contagem{
            margin-top:-25px;
            font-size:20px;
            margin-left: -60px;
        }
        button{
            display:auto;
            border-radius: 15px;
            margin-left: -20px;
            width:98%;
            margin-top:15px;
            text-align: center;
            background-color:rgb(72, 54, 152);
            color:#fff;
        }
    }
</style>

