<template>
  <div class="products H-row" id="product">
    <p class="header-two">Our Products</p>
    <div class="products-content">
      <BaseProductCard :productList="productList" />
    </div>
  </div>
</template>

<script>
import productList from "../../assets/APIs/productList";
import BaseProductCard from "./BaseProductCard";

export default {
  name: "Products",
  components: {
    BaseProductCard,
  },
  data() {
    return {
      productList,
    };
  },
};
</script>

<style scoped>
 .products {
    margin: 0vw 5vw;
  }

  .products-content {
    display: grid;
    gap: 3vw;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr 1fr;
    align-items: center;
    justify-content: space-between;
  }
@media screen and (min-width: 800px) {
  .products {
    margin: 0vw 10vw;
  }

  .products-content {
    display: grid;
    gap: 3vw;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr 1fr;
    align-items: center;
    justify-content: space-between;
  }
}
</style>
