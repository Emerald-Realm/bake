<template>
  <div class="showcase">
      <img :src="image" alt="">
  </div>
</template>

<script>
export default {
    name:'ShowCase',
    props: {
        image: String,
    }
}
</script>

<style scoped>
    img {
        width: 95vw;
    }
</style>