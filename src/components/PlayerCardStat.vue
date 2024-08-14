<template>
  <section class="PlayerCardStat">
    <p class="statName">{{statName}}</p>
    <p class="statValue">{{statValue}}</p>
  </section>
</template>

<script>
export default {
  props: {
    statName: {
      type: String,
      required: true
    },
    statValue: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>

.PlayerCardStat {
  width: 75px;
  height: 75px;
  border-radius: 15px;
  background: #4B5058;

  display: block;
  align-content:space-evenly;
  text-align: center;
}

.statName {
  width: 75px;
  height: 14px;
  color: #F5F5F5;
  margin: 0;
  position: relative;
  top: -5px;

  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.statValue {
  width: 75px;
  height: 40px;
  color: #F5F5F5;
  margin: 0;
  position: relative;
  top: -5px;

  font-size: 40px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
</style>