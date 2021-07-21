<template>
  <p class="motto">Perfection Breeds Perfection</p>
  <hr />
  <div id="service" class="H-row">
    <p class="header-two">We Offer</p>
    <div class="service">
      <BaseServiceCard :serviceList="serviceList" />
    </div>
  </div>
</template>

<script>
import BaseServiceCard from "./BaseServiceCard";
import serviceList from "../../assets/APIs/serviceList";

export default {
  name: "Service",
  components: {
    BaseServiceCard,
  },
  data() {
    return {
      serviceList,
    };
  },
};
</script>

<style scoped>
  .service {
    margin : 0vw 5vw;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2vw;
    align-items: center;
    text-align: left;
    justify-content: space-between;
  }
@media screen and (min-width: 800px) {
  .service {
    text-align: center;
  }
}
</style>
