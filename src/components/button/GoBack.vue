<template>
    <div class="goBack">
        <a @click="goBack"> a </a>
    </div>
</template>

<script>

export default {
    name: 'GoBack',
    methods: {
        goBack(){
            return this.$router.go(-1)
        }
    }
}
</script>
<style scoped>
    .goBack{
        display: flex;
        padding-top: -100px;
    }
</style>