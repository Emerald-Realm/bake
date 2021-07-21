<template>
  <div
    class="baseTestimonyCard"
    v-for="testimony in TestimonyList"
    :key="testimony.id"
  >
    <p class="context">{{ testimony.context }}</p>
    <img :src="testimony.image" :alt="testimony.name" />
    <p class="name">{{ testimony.name }}</p>
  </div>
</template>

<script>
export default {
  name: "BaseTestimonyCard",
  props: {
    TestimonyList: Array,
  },
};
</script>

<style scoped>
.baseTestimonyCard {
  display: flex;
  flex-shrink: 0;
  width: 18vw;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

img {
  /* height: 5vw; */
  width: 50%;
  border-radius: 99px;
}
@media screen and (max-width: 799px) {
.baseTestimonyCard {
    width: 40vw;
}
img {
    width: 35%;
}
}
</style>