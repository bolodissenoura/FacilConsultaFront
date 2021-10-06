<template>
    <div >
        <h2 class="subFonte">{{ nome }}</h2>
    </div>
</template>

<script>
export default{
    name: 'Titulo',
    data() {
        return{        
            nome: 'Sobre o profissional'
        }
    }
}
</script>
<style>
    .subFonte{
        display: flex;
        color: #483698;
        font-size: 35px;
        margin: 5% 0px 0px 8%;
        font-family: 'Comfortaa', cursive;
        font-weight:800;
    }
</style>
