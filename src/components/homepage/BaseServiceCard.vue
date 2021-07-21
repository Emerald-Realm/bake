<template>
  <div class="service-card" v-for="service in serviceList" :key="service.id">
    <img :src="service.logo" alt="#" class="service-logo" />
    <div class="service-context">
      <p>
        {{ service.topic }}
      </p>
      <p>
        {{ service.context }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseServiceCard",
  props: {
    serviceList: Array,
  },
};
</script>

<style scoped>
@media screen and (min-width: 800px) {
  img {
    /* width: 80px; */
    width: 30vw;
  }
}

.service-card {
  display: flex;
  flex-direction: column;
  place-items: center;
  text-align: center;
}

img {
  width: 50%;
}
</style>