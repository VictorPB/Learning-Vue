<template>
    <section class="MVPMatchResultComponent">
        <img class="MVPMatchTeamImage" :alt="team1.name" :src="team1.image" />

            <section class="MVPResult">
                <p class="MVPGoal">{{result.team1}}</p>
                <p>VS</p>
                <p class="MVPGoal">{{result.team2}}</p>
            </section>

        <img class="MVPMatchTeamImage" :alt="team2.name" :src="team2.image" />      
    </section>
</template>

<script>
export default {
  props: {
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
.MVPMatchResultComponent {
    background-color: #2E3136;
    width: 100px;
    height: 220px;
    border-radius: 0px 15px 15px 0px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}
.MVPResult {
    display: flex;
    height: 50px;
    width: 100px;
    gap: 8px;
    font-weight: bold;
    justify-content: center;
    align-items: center;
    color : #FFF;
}

.MVPGoal {
    font-size: 40px;
    color: #E5C100;
}

.MVPMatchTeamImage {
    height: 80px;
}
</style>