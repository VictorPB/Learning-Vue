<template>

  <header>
    <img alt="Vue logo" src="/src/assets/logo.svg"/>
    <h1>Welcome to my Vue Components and Apps</h1>
  </header>

  <main>
    <AppsPanel :title :description :image :alt/> 
    <TeamListItem :team/>
    <PlayerCardStat statName="Asistencias" statValue="10"/>
    <PlayerCard :player/>
    <MatchResult :team1 :team2 :result :date/>
  </main>

  <footer>
    <p>Footer content</p>
  </footer>

</template>


<script>
  import AppsPanel from './components/AppPanel.vue'
  import TeamListItem from './components/TeamListItem.vue'
  import PlayerCardStat from './components/PlayerCardStat.vue'
  import PlayerCard from './components/PlayerCard.vue';
  import MatchResult from './components/MatchResult.vue';

  export default {
    components: {
      AppsPanel,
      TeamListItem,
      PlayerCardStat,
      PlayerCard,
      MatchResult
    },
    data() {
      return{
        title: "X Perfiles sugeridos",
        description: "Proyecto para aprender Vue que consiste en crear un clon de la sección de sugerencias de perfiles de X. En ellas aparece el nombre, perfil, foto y botón de seguir que tiene animación y cambia según su estado.",
        image: "/src/assets/x_follow_card.png",
        alt: "Sección de sugerencias de perfiles de X.",

        team: {
          name: "Valderrubio FC",
          image: "/src/assets/peña.png",
          colors: {
            primary: "#FFE974",
            secondary: "#1813EA"
          }
        },

        player: {
          name: "Víctor Pérez",
          image: "/src/assets/Victor2.png",
          team: {
            name: "Valderrubio FC",
            image: "/src/assets/peña.png",
            colors: {
              primary: "#FFE974",
              secondary: "#1813EA"
            }
          },
          stats: [
            {name: "Posición", value: "DC"},
            {name: "Número", value: "27"},
            {name: "Goles", value: "14"},
            {name: "Asistencias", value: "9"},
            {name: "Edad", value: "23"}
          ]
        },

        team1:{
          name: "Valderrubio FC",
          image: "/src/assets/peña.png",
          colors: {
            primary: "#FFE974",
            secondary: "#1813EA"
          }
        },
        team2:{
          name: "Atletico de Madrid",
          image: "/src/assets/Atleti.png",
          colors: {
            primary: "#FF0000",
            secondary: "#FFFFFF"
          }
        },
        result:{
          team1: 5,
          team2: 2
        },
        date: "18/08 - 21:00"
      }
    }
  }
</script>


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
    gap:30px;
    margin: 30px;
    justify-items: center;
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