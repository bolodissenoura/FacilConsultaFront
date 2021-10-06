<template>
    <div>
        <form style="margin: 5% 0px 0px 8%;">
            <div class="form-group">
                <label class="tituloInput" for="name">Nome Completo*</label>
                <input 
                type="name" 
                class="form-control inputName" 
                id="name" aria-describedby="name" 
                minlength="3"
                maxlength="48"
                placeholder="Digite o nome completo">
            </div>
            <div class="form-group">
                <label class="tituloInput" for="CPF">CPF*</label>
                <input 
                type="text"
                inputmode="numeric" 
                class="form-control inputNumber"
                maxlength="14" id="CPF" 
                v-on:keypress="NumbersOnly"
                placeholder="Digite um CPF">
                
            </div>
            <div class="form-group">
                <label class="tituloInput" for="CPF">Número de celular*</label>
                <input 
                type="tel"
                inputmode="numeric" 
                class="form-control inputNumber"
                maxlength="15" id="phone" 
                v-on:keypress="NumbersOnly"
                placeholder="(00)0 0000-0000">
            </div>
            <div class="row">
                <div class="col-md-4">
                    <label class="tituloInput" for="CPF">Estado*</label>
                    <select type="text" class="form-control inputSelect" placeholder="First name">
                        <option>...</option>
                    </select>
                </div>
                <div class="col-md-4">
                    <label class="tituloInput" for="CPF">Cidade*</label>
                    <select type="text" class="form-control inputSelect" placeholder="Last name">

                    </select>
                </div>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="progress" style="height: 25px;width:300px;margin-top:30px;">
                        <div class="progress-bar" role="progressbar" style="width: 50%;background-color: rgb(72, 54, 152);" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                </div>
                <div class="col-md-4">
                    <h6 style="margin-top:30px;font-size:20px;" for="CPF">1 de 2</h6>
                </div>
            </div>
            <button type="submit" class="btn">PRÓXIMO</button>
        </form>
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
        document.addEventListener('keydown', function(event) { //pega o evento de precionar uma tecla
        if(event.keyCode != 46 && event.keyCode != 8){//verifica se a tecla precionada nao e um backspace e delete
        var i = document.getElementById("phone").value.length; //aqui pega o tamanho do input
        if (i === 0 ) //aqui faz a divisoes colocando um ( 
        document.getElementById("phone").value = document.getElementById("phone").value + "(";
        if (i === 3 ) //aqui faz a divisoes colocando um )
        document.getElementById("phone").value = document.getElementById("phone").value + ")";
        if (i === 5 ) //aqui faz a divisoes colocando um espaco em branco apos o 5 indice
        document.getElementById("phone").value = document.getElementById("phone").value + " ";
        else if (i === 10) //aqui faz a divisao colocando o tracinho no decimo indice
        document.getElementById("phone").value = document.getElementById("phone").value + "-";
    }
    });
    export default{
        name: 'InputText',
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
    .inputNumber{
        width: 300px;
    }
    .inputSelect{
        width: 230px;
    }
    input, select{
        border-color: #483698;
    }
    input:focus, select:focus{
        border-color: #483698;  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(72, 54, 152, 0.6);
        box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(72, 54, 152, 0.6);
    }
    h6{font-family: 'Comfortaa', cursive;color:#483698;}
    button{display:flex;margin-bottom:30px;width:400px;text-align: center;background-color:rgb(72, 54, 152);color:#fff;}
    
</style>

