<template>
  <div class="homepage">
    <TheHeader />
    <hr />
    <Carousel />
    <hr />
    <Service />
    <hr />
    <Products />
    <hr />
    <!-- <Philosophy /> -->
    <hr />
    <Recommended />
    <hr />
    <About />
    <hr />
    <Additions />
    <hr />
    <Contact />
    <hr />
    <Testimony />
    <hr />
    <TheFooter />
    <hr />
    <div></div>
  </div>
</template>

<script>
import TheHeader from "./homepage/TheHeader";
import TheFooter from "./homepage/TheFooter";
import Philosophy from "./homepage/Philosophy";
import About from "./homepage/About";
import Contact from "./homepage/Contact.vue";
import Service from "./homepage/Service.vue";
import Products from './homepage/Products.vue';
import Recommended from './homepage/Recommended.vue';
import Additions from './homepage/Additions.vue';
import Testimony from './homepage/Testimony.vue';
import Carousel from './homepage/Carousel.vue';



export default {
  name: "Home",
  components: {
    TheHeader,
    TheFooter,
    // Philosophy,
    About,
    Contact,
    Service,
    Products,
    Recommended,
    Additions,
    Testimony,
    Carousel,
  },
};
</script>

<style>
  .show {
    opacity: 1;
  }
</style>
