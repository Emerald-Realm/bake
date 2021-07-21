<template>
  <div class="testimonies H-row" id="testimony">
    <p class="header-two">From Our Customers</p>
    <div class="testimony">
      <BaseTestimonyCard :TestimonyList="testimonyList" />
    </div>
  </div>
</template>

<script>
import BaseTestimonyCard from "./BaseTestimonyCard";
import testimonyList from "../../assets/APIs/testimonyList";

export default {
  name: "Testimony",
  components: {
    BaseTestimonyCard,
  },
  data() {
    return {
      testimonyList,
    };
  },
};
</script>

<style scoped>
.testimony {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5vw;
}

@media screen and (max-width: 799px) {
  .testimony {
    overflow-x: scroll;
  }
}
</style>