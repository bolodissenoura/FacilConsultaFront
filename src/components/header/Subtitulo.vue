<template>
    <div >
        <h5 class="tituloFonte">{{ nome }}</h5>
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
    .tituloFonte{
        display: flex;
        margin: 5% 0px 0px 8%;
        font-size: 21px;
        font-family: 'Open Sans', sans-serif;
        font-weight:800;
    }
</style>
