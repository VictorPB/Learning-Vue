<template>
  <section class="playerCard">
    <section class="playerCardImage" :style="`background: linear-gradient(180deg, ${player.team.colors.primary} 0%, ${player.team.colors.secondary} 100%);`">
      <img class="teamImage" :alt="player.team.name" :src="player.team.image" />
      <img class="playerImage" :alt="player.name" :src="player.image" />
    </section>
    <p class="playerName"> {{player.name}} </p>
    <aside class="playerStats">
      <section v-for="stat in player.stats" :key="stat.key">
        <PlayerCardStat :statName="stat.name" :statValue="stat.value"/>
      </section>
    </aside>
  </section>
</template>

<script>
import PlayerCardStat from './PlayerCardStat.vue';

  export default {
  components: {
    PlayerCardStat
  },
  props: {
    player: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>

.playerCard {
  width: 400px;
  height: 480px;
  border-radius: 15px;
  background-color: #131416;
  display: grid;
  grid-template-rows: 2;
  grid-template-columns: 2;
  
}

.playerCardImage {
  width: 312.5px;
  height: 423.5px;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25) inset;
  border-radius: 15px 0px;
  background: linear-gradient(209deg, #FFE974 2.26%, #1813EA 100%);
  overflow: hidden;
}

.teamImage {
  width: 100px;
  height: 100px;
  position: relative;
  left: 15px;
  top: 15px;
  
}

.playerImage {
  height: 400px;
  border-radius: 15px 0px;
  position: relative;
  left: 20px;
  bottom: 79.6px;
}

.playerName{
  display: flex;
  height: 32px;
  margin: 12px;
  justify-content: center;
  align-items: center;

  color: #F5F5F5;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;

  grid-row: 2 / 3;
  grid-column: 1 / 3;
}

.playerStats{
  width: 75px;
  display: flex;
  flex-direction: column;
  justify-content:space-around;
  margin-top: 5px;

  position: relative;
  grid-row: 1 / 2;
  grid-column: 2 / 3;
}
</style>