<template>
  <div class="desktop-header" id="home">
    <!-- First Navigation Row -->
    <div class="logo-row">
      <img class="logo" :src="logo" alt="" />
    </div>
    <!-- Second Navigation Row -->
    <div class="second-row">
      <ul class="navbar" v-if="navShows">
        <a href="#home" class="nav-link">
          <li @click="scrollToTop">Home</li>
        </a>
        <a href="#service" class="nav-link">
          <li>Service</li>
        </a>
        <a href="#product" class="nav-link">
          <li>Products</li>
        </a>
        <a href="#recommendation" class="nav-link">
          <li>Recommendation</li>
        </a>
        <a href="#about" class="nav-link">
          <li>About</li>
        </a>
        <a href="#new" class="nav-link">
          <li>New</li>
        </a>
        <a href="#contact" class="nav-link">
          <li>Contact</li>
        </a>
        <a href="#testimony" class="nav-link">
          <li>Testimony</li>
        </a>
        <a href="#" @click="handleMenuFall()" class="nav-link stay">
          <li>{{ navShows ? "Products List" : "Close Product List" }}</li>
        </a>
      </ul>
      <a v-else href="#" @click="handleMenuFall()" class="nav-link stay">
        <li>{{ navShows ? "Products List" : "Close Product List" }}</li>
      </a>
    </div>
  </div>
</template>

<script>
import logo from "../../assets/logo.svg";

export default {
  name: "DesktopHeader",
  data() {
    return {
      logo,
      navShows: true,
    };
  },
  methods: {
   scrollToTop() {
      window.scrollTo(0, 0);
    },
    // manipulate menu fall
    handleMenuFall() {
      this.navShows = !this.navShows;
      const sideMenu = document.querySelector(".side-menu");
      console.log(this.navShows);
      if (sideMenu.classList.contains("tall")) {
        sideMenu.classList.remove("tall");
      } else {
        sideMenu.classList.add("tall");
      }
    },
  },
};
</script>

<style scoped>
.second-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  /* display: grid; */
  grid-template-columns: 80% 20%;
  gap: 2vw;
  flex-flow: row-reverse;
}

.logo {
  height: 5vh;
}

.menu {
  display: none;
}
#home {
  padding: 0.5vw 0vw 0vw 0vw;
}

.navbar {
  padding: 0vw;
  display: flex;
  align-items: center;
  justify-content: space-between;
  list-style: none;
  flex-grow: 1;
}
.nav-link {
  text-decoration: none;
  color: var(--link_color);
}

.nav-link:hover {
  color: var(--main_color);
}

.hide {
  display: none;
}

.stay {
  display: block;
  background-color: brown;
  color: white;
  border-radius: 0.2rem;
  padding: 0.5rem 0.8rem;
  /* min-width: 5vw; */
  /* width: 100%; */
}
</style>
