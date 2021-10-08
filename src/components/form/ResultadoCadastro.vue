<template>
    <h2 class="titulo">{{ Titulo }}</h2>

    <div class="row">
        <form style="margin: 5% 0px 0px 5%;" >
                <div class="form-group">
                    <label class="tituloInput resultadoTitulo" for="name">Nome Completo</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">CPF</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">Número de celular ou telefone</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">Estado/Cidade</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">Especialidade principal</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">Preço da consulta</label>
                    <p class="tituloInput">Fabricio</p>
                    <label class="tituloInput resultadoTitulo" for="name">Formas de pagamento da consulta</label>
                    <p class="tituloInput">Fabricio</p>
            </div>

            <button type="submit" class="btn">CADASTRAR PROFISSIONAL</button><br/>
            <a style="font-family: 'Comfortaa', cursive;color:#483698;" href="">Editar cadastro</a>
        </form>
    <img src="../../assets/desktop-pagina-3.png" style="width:400px;height:400px;" class="rounded" >
    </div>
        
</template>

<script>
    
    export default{
        name: 'FormAtendimento',
        data() {
            return{        
                Titulo: 'Revisão do Cadastro'
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
    
    .resultadoTitulo{
        font-weight:bold;
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
        background-color:#FBDE40;
        color:#000;
        font-family: 'Comfortaa', cursive;
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
        width: 300px;
        font-family: 'Open Sans', sans-serif;
        height:auto;
        background-color: #F9F9F9;
        border-radius: 10px;
        box-shadow:  3px 3px 2px rgba(0, 0, 0, 0.09)
    }
    .box-check-cartao{
        width: 300px;
        font-family: 'Open Sans', sans-serif;
        height:auto;
        background-color: #F9F9F9;
        box-shadow:  3px 3px 2px rgba(0, 0, 0, 0.09)
    }
    .checkbox{filter: hue-rotate(30deg)}


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

