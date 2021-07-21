<template>
  <div class="menu-card" v-for="item in List" :key="item.id">
    <img :src="item.image" alt="menu" class="menu-img" />
    <div class="context">
      <p class="name">{{ item.name }}</p>
      <p class="price">{{ item.price }}</p>
      <button class="order">Order</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseMenuCard",
  props: {
    List: Array,
  },
};
</script>

<style scoped>
  .menu-card {
    display: flex;
    flex-direction: column;
    border: 2px solid burlywood;
    border-radius: 5%;
    margin: 2vw 2vw;
    overflow: hidden;
  }

.order {
  width: 70%;
  padding: 0.5vw;
  border: 3px solid burlywood;
  background-color: white;
  color: burlywood;
  border-radius: 5%;
  font-weight: bold;
  margin-bottom: 1rem;
  transition: all 1s ease-out;
}

.order:hover {
  background-color: burlywood;
  color: white;
}

@media screen and (max-width: 799px) {
.menu-card {
  display: flex;
  flex-direction: column;
  width: 24vw;
  flex-shrink: 0;
  border: 2px solid burlywood;
  border-radius: 5%;
  margin: 2vw 2vw;
  overflow: hidden;
}
}

img {
  flex-grow: 0;
  width: 100%;
  overflow: hidden;
  transition: all 1s ease-out;
  border-bottom: solid white 4px;
}

img:hover {
  overflow: hidden;
  border-bottom: solid chocolate 4px;
  transform: scale(1.1);
}
</style>