<script>
  import AppsPanel from './components/AppPanel.vue'

  export default {
    components: {
      AppsPanel
    },
    data() {
      return{
        title: "X Perfiles sugeridos",
        description: "Proyecto para aprender Vue que consiste en crear un clon de la sección de sugerencias de perfiles de X. En ellas aparece el nombre, perfil, foto y botón de seguir que tiene animación y cambia según su estado.",
        image: "/src/assets/x_follow_card.png",
        alt: "Sección de sugerencias de perfiles de X."
      }
    }
  }
</script>


<template>

  <header>
    <img alt="Vue logo" src="/src/assets/logo.svg"/>
    <h1>Welcome to my Vue Components and Apps</h1>
  </header>

  <main>
    <AppsPanel :title :description :image :alt/>
  </main>

  <footer>
    <p>Footer content</p>
  </footer>

</template>


<style>
  #app {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 5fr 1fr;
    margin: 0;
    height: 100vh;
    font-weight: normal;
    padding: 0;
    justify-items: center;
  }

  main{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    margin: 30px;
  }

  header{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: aquamarine;
    width: 100vw;

    img{
      width: 100px;
      height: 100px;
    }
  }

</style>