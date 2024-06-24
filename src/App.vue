<script>
  import AppsPanel from './components/AppPanel.vue'

  export default {
    components: {
      AppsPanel
    },
    data() {
      return{
        title: "X Perfiles sugeridos",
        description: "Proyecto para aprender Vue que consiste en crear uun clon de la sección de sugerencias de perfiles de X. En ellas aparece el nombre, perfil, foto y botón de seguir que tiene animación y cambia según su estado.",
        image: "/src/assets/x_follow_card.png",
        alt: "Sección de sugerencias de perfiles de X."
      }
    }
  }
</script>


<template>

  <header>
    <h1>Welcome to my Vue 3 Apps</h1>
    <img alt="Vue logo" src="/src/assets/logo.svg" width="125" height="125" />
  </header>
  
  <br>

  <main>
    <AppsPanel :title :description :image :alt/>
  </main>

  <br>

  <footer>
    <p>Footer content</p>
  </footer>

</template>


<style>
  header {
    line-height: 1.5;
  }

  body{
    background-color: #0a0a0b;
  }

</style>