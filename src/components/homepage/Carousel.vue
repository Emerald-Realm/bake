<template>
  <!-- the carousel component containing forward and backwards btns -->
  <div class="carousel" :style="styles">
    <button class="prev" @click="prevIndex()">&#10094; Previous</button>
    <!-- <ShowCase :image="productList[index].image" /> -->
    <button class="next" @click="nextIndex()">Next &#10095;</button>
  </div>
</template>

<script>
// intialization of variables, styles and imports
import productList from "../../assets/APIs/productList";
import ShowCase from "./ShowCase";

let index = 0;
let newIndex;
let length = productList.length - 1;

let styles = {
  backgroundImage: `url(${productList[index].image})`,
  border: "1px solid brown",
  backgroundSize: "cover",
  backgroundPosition: "center",
};

setInterval(() => {
  let newIndex = index++;
  index = newIndex;
  return index;
}, 2000);

export default {
  name: "Carousel",
  components: {
    ShowCase,
  },
  data() {
    return {
      productList,
      index,
      styles,
    };
  },
  methods: {
    prevIndex() {
      if (this.index == 0) {
        newIndex = length;
      } else {
        newIndex = this.index - 1;
      }
      this.index = newIndex;
      // changing backgroud with respect to index value
      this.styles = {
        ...this.styles,
        backgroundImage: `url(${productList[this.index].image})`,
      };
    },

    nextIndex() {
      if (this.index == length) {
        newIndex = 0;
      } else {
        newIndex = this.index + 1;
      }
      setInterval(() => {
        newIndex++
      }, 2000)
      this.index = newIndex;
      // changing backgroud with respect to index value
      this.styles = {
        ...this.styles,
        backgroundImage: `url(${productList[this.index].image})`,
      };
    },
  },
};
</script>

<style>
.carousel {
  height: 50vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* gap: 86vw; */
}
button {
  padding: 0.5vw;
  background-color: white;
  color: var(--main_color);
  border: none;
  border-radius: 10%;
}

button:hover {
  background-color: var(--main_color);
  color: white;
}

</style>
