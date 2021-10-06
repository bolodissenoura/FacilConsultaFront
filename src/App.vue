<template>
    <div class="center-screen">
      <div class="container">
          <Titulo/>
          <Subtitulo/>
          <InputText/>
      </div>
    </div>
</template>

<script>
  import Titulo from './components/header/Titulo.vue'
  import Subtitulo from './components/header/Subtitulo.vue'
  import InputText from './components/form/InputText.vue'

  export default {
    name: 'App',
    components: {
      Titulo,
      Subtitulo,
      InputText
    },
    data() {
    return{        
        nome: 'Daniel'
    }
}
  }
</script>
 <style>
    .container{
        background-color:#fff;
        height: auto;
        width:800px;
        border-radius: 20px;
        box-shadow: 0 0 1em rgba(0, 0, 0, 0.2);
    }
    .center-screen {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        min-height: 100vh;
    }
 </style>
