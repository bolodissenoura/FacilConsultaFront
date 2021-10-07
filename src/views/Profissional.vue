<template>
    <div>
        <Titulo/>
        <Subtitulo/>
        <InputText/>
    </div>
</template>

<script>
    import Titulo from '../components/header/Titulo.vue'
    import Subtitulo from '../components/header/Subtitulo.vue'
    import InputText from '../components/form/InputText.vue'

    export default {
        name: 'Profissional',
        components: {
            Titulo,
            Subtitulo,
            InputText
        }
    }
</script>
