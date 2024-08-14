<template>
  <section class="MVPCard">
    <p class="MVPCardName">MVP J3</p>
    <img class="MVPPlayerImage" :alt="player.name" :src="player.image" />
    <MatchResultMVP id="MatchResultMVP" :team1 :team2 :result />
    <p class="MVPPlayerName">{{ player.name }}</p>
  </section>
</template>

<script>

import MatchResultMVP from './MatchResultMVP.vue';

export default {
  components: {
      MatchResultMVP
    },
  props: {
    player: {
      type: Object,
      required: true
    },
    team1: {
      type: Object,
      required: true
    },
    team2: {
      type: Object,
      required: true
    },
    result: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

.MVPCard {
  width: 360px;
  height: 440px;
  border-radius: 15px;
  background-color: #0960ed;
}

.MVPCardName {
  font-size: 32px;
  font-weight: bold;
  color: #E5C100;
  background-color: #2E3136;
  width: fit-content;
  padding: 8px;
  border-radius: 15px 0px;
  margin: 0;
}

.MVPPlayerImage {
  width: 280px;
  height: 370px;
  position: relative;
  left: 70px;
  top: -30px;
}

.MVPPlayerName{
  font-size: 32px;
  font-weight: bold;
  color: #E5C100;
  width: 100%;
  height: 50px;
  background-color: #2E3136;
  text-align: center;
  align-content: center;
  border-radius: 0px 0px 15px 15px;
  position: relative;
  top: -289px;
}

#MatchResultMVP{
  position: relative;
  top: -320px;
}
</style>