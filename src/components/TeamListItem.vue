<template>
  <section id="teamListItem">
    <div id="gradient" :style="`background: linear-gradient(180deg, ${gradientColors[0]} 0%, ${gradientColors[1]} 100%);`"></div>
    <img id="teamImage" :alt=" teamName" :src="teamImage" />
    <p id="teamName"> {{teamName}} </p>
  </section>
</template>

<script>
export default {
  props: {
    teamName: {
      type: String,
      required: true
    },
    teamImage: {
      type: String,
      required: true
    },
    gradientColors:{
      type: Array,
      required: true
    }
  }
}
</script>

<style>
  #teamListItem {
    background-color: #2E3136;
    width: 475px;
    height: 175px;
    border-radius: 15px;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.50);
    overflow: hidden;
    display: grid;
    grid-template-columns: 2fr 3fr;
    grid-template-rows: 1fr;
    align-items: center;
    justify-items: center;
    align-content: center;
    position: relative;
  }

  #teamListItem:hover #teamImage{
    transform: scale(1.1); 
  }

  #teamListItem:hover #teamName{
    background-image: linear-gradient(
      -225deg,
      #fff 30%,
      #1813EA 35%,
      #FFE974 55%,
      #fff 60%
    );
    background-size: auto auto;
    background-clip: border-box;
    background-size: 300% auto;
    color: #fff;
    background-clip: text;

    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: textclip 1s linear 1 forwards;
  }

  @keyframes textclip {
    to {
      background-position: 100% center;
    }
  }

  #gradient {
    width: 220px;
    height: 300px;
    transform: rotate(20deg);
    
    grid-row: 1 / 2;
    grid-column: 1 / 2;
    position: absolute;
    left: -30px;
  }

  #teamImage {
    width: 150px;
    height: 150px;

    grid-row: 1 / 2;
    grid-column: 1 / 2;

    position: absolute;
    transition-duration: 0.3s;
  }

  #teamName {
    color: #dddddd;
    font-size: 30px;
    font-weight: bold;
    left: -50px;

    grid-row: 1 / 2;
    grid-column: 2 / 3;

    transition-duration: 0.3s;
  }

</style>