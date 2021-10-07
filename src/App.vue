<template>
    <div class="center-screen">
      <div class="container-fluid">
        <router-view></router-view>
      </div>
    </div>
</template>

<script>
  import Profissional from './views/Profissional.vue'
  export default {
    name: 'App',
    components: {
      Profissional
    }

  }
</script>
 <style>
    .container-fluid{
        background-color:#fff;
        height: auto;
        width: 900px;
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

    @media (max-width: 600px)
    {
        .container-fluid{
          border-radius: 0px;
          border-top-left-radius: 60px;
          border-top-right-radius: 60px;
          margin-top:80px;
          max-width: 100%;
          height: 92vh;
          overflow-x: hidden;
        }
    }
 </style>
