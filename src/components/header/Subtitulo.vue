<template>
    <div >
        <h5 class="subTitulo">{{ nome }}</h5>
    </div>
</template>

<script>
export default{
    name: 'Titulo',
    data() {
        return{        
            nome: 'Dados do profissional'
        }
    }
}
</script>
<style>
    .subTitulo{
        display: flex;
        margin: 3% 0px 0px 5%;
        font-size: 21px;
        font-family: 'Open Sans', sans-serif;
        font-weight:800;
    }
        @media (max-width: 600px)
    {
        .subTitulo{
            margin-top: 30px;
        }
    }
</style>
