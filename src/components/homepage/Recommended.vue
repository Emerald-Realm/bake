{<template>
  <div class="recommended H-row" id="recommendation">
    <p class="header-two">Our Recommendations</p>
    <div class="recommendations">
      <BaseMenuCard :List="RecommendedList" />
    </div>
  </div>
</template>

<script>
import BaseMenuCard from "../menu/BaseMenuCard";
import RecommendedList from "../../assets/APIs/RecommendedList";

export default {
  name: "Recommended",
  components: {
    BaseMenuCard,
  },
  data() {
    return {
      RecommendedList,
    };
  },
};
</script>

<style scoped>
.recommendations {
  margin: 0vw 5vw;
  display: flex;
  grid-template-rows: 1;
  overflow-x: scroll;
  overflow-y: hidden;
  align-items: center;
  justify-content: space-around;
}

@media screen and (min-width: 800px) {
  .recommendations {
    margin: 0vw 5vw;
    display: flex;
    align-items: center;
    justify-content: space-around;
    overflow : hidden;
  }
}
</style>