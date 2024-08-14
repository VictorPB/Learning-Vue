<template>
    <section class="MatchResultComponent">
        <img class="MatchTeamImage" :alt="team1.name" :src="team1.image" />

        <section class="MatchResult">
            <section id="Result">
                <p class="Goal">{{result.team1}}</p>
                <p>VS</p>
                <p class="Goal">{{result.team2}}</p>
            </section>

            <p class="matchDate">{{date}}</p>
        </section>

        <img class="MatchTeamImage" :alt="team2.name" :src="team2.image" />      
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
    },
    date: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.MatchResultComponent {
    background-color: #2E3136;
    width: 365px;
    height: 100px;
    border-radius: 15px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.MatchResult{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
}

#Result {
    display: flex;
    height: 50px;
    width: 100px;
    gap: 15px;
    font-weight: bold;
    justify-content: center;
    align-items: center;
    position: relative;
    top: 15px;
}

.matchDate {
    font-size: 14px;
    position: relative;
    top: 10px;
}

.Goal {
    font-size: 48px;
    color: #E5C100;
}

.MatchTeamImage {
    height: 90px;
}
</style>