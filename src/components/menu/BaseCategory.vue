{<template>
  <div
    v-for="category in categoryList"
    :key="category.id"
    class="H-row"
    :id="category.class"
  >
    <p class="header-two">{{ category.name }}</p>
    <div class="category">
      <BaseMenuCard :List="RecommendedList" />
    </div>
  </div>
</template>

<script>
import BaseMenuCard from "../menu/BaseMenuCard";
import RecommendedList from "../../assets/APIs/RecommendedList";

export default {
  name: "BaseCategory",
  components: {
    BaseMenuCard,
  },
  props: {
    categoryList: Array,
  },
  data() {
    return {
      RecommendedList,
    };
  },
};
</script>

<style scoped>
.category {
  margin: 0vw 5vw;
  display: flex;
  grid-template-rows: 1;
  overflow-x: scroll;
  overflow-y: hidden;
  align-items: center;
  justify-content: space-around;
}

@media screen and (min-width: 800px) {
  .category {
    margin: 0vw 5vw;
    display: flex;
    align-items: center;
    justify-content: space-around;
    overflow: hidden;
  }
}
</style>