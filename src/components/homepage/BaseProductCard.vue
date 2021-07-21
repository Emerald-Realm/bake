<template>
  <div class="productCard" v-for="product in productList" :key="product.id">
    <img :src="product.image" alt="#" class="product-img" />
    <p class="product-text" @click="handleProductClick()">
      {{ product.context }}
    </p>
  </div>
</template>

<script>
export default {
  name: "BaseProductCard",
  props: {
    productList: Array,
  },
  methods: {
    handleProductClick() {
      const sideMenu = document.querySelector(".side-menu");
      if (sideMenu.classList.contains('tall')) {
        sideMenu.classList.remove("tall");
      } else {
        sideMenu.classList.add("tall");
      }
    },
  },
};
</script>

<style scoped>
.productCard {
  display: flex;
  flex-direction: column;
  border: 5px solid burlywood;
  border-style: inset;
  overflow: hidden;
}

img {
  flex-grow: 0;
  width: 100%;
  overflow: hidden;
  transition: all 1s ease-in-out;
  border-bottom: solid white 4px;
}

img:hover {
  overflow: hidden;
  border-bottom: solid chocolate 4px;
  transform: scale(1.01);
}

.product-text {
  cursor: pointer;
  transition: 1s all ease-out;
}

.product-text:hover {
  color: grey;
  text-decoration: 1px solid grey underline;
}
</style>
