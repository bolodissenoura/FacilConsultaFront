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
            nome: 'Dados do Profissional'
        }
    }
}
</script>
<style>
    .tituloFonte{
        display: flex;
        margin: 5% 0px 0px 8%;
        font-family: 'Comfortaa', cursive;
        font-weight:bold;
    }
</style>
