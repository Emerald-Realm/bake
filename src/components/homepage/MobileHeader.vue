<template>
  <div class="mobile-header" id="home">
    <!-- Main Row -->
    <div class="logo-row">
      <img class="logo" :src="logo" alt="" />
      <div class="btns">
        <button class="menu">
          <a href="#" @click="handleMenuFall()">{{
            fall ? "Close Products" : "Products"
          }}</a>
        </button>
        <button class="menu" @click="handleSideMenu()">
          {{ status ? "Close Menu" : "Menu" }}
        </button>
      </div>
    </div>
    <!-- Menu List -->
    <ul class="navbar">
      <a href="#home" @click="scrollToTop()" class="nav-link">
        <li>Home</li>
      </a>
      <a href="#service" class="nav-link">
        <li>Service</li>
      </a>
      <a href="#product" class="nav-link">
        <li>Our Products</li>
      </a>
      <a href="#philosophy" class="nav-link">
        <li>Philosophy</li>
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
    </ul>
  </div>
</template>

<script>
import logo from "../../assets/logo.svg";

export default {
  name: "MobileHeader",
  data() {
    return {
      status: false,
      fall: false,
      logo,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    },

    handleSideMenu() {
      this.status = !this.status;
      const navbar = document.querySelector(".mobile-header");
      if (navbar.classList.contains("show-navbar")) {
        navbar.classList.remove("show-navbar");
      } else {
        navbar.classList.add("show-navbar");
      }
    },

    handleMenuFall() {
      this.fall= !this.fall;

      const sideMenu = document.querySelector(".side-menu");
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
@media screen and (max-width: 799px) {
  .logo {
    padding-top: 1vh;
    height: 5vh;
  }

  .logo-row {
    display: flex;
    width: 90vw;
    margin: 0vw 5vw;
    align-items: center;
    justify-content: space-between;
  }

  .btns {
    display: flex;
    align-items: center;
    gap: 5vw;
  }

  .menu {
    display: block;

    font-size: var(--link_size);
    color: var(--link_color);
    padding-top: 1vh;
  }

  .mobile-header {
    position: fixed;
    width: 0vw;
    z-index: 10;
    top: 0;
    left: 0;
    margin: 0vw 0vw;
    transition: 1s all ease;
  }

  .navbar {
    display: block;
    margin-top: 10vw;
    list-style: none;
    overflow: hidden;
    transition: 1s all ease;
  }

  @keyframes change {
    0% {
      width: 0vw;
      opacity: 0;
    }

    100% {
      width: 80vw;
      opacity: 1;
      background-color: var(--main_color);
    }
  }

  ul {
    margin: 0vw;
    padding: 0vw;
    padding-left: 5vw;
  }

  .show-navbar {
    display: block;
    width: 100vw;
    height: 100vh;
    background-color: rgba(250, 250, 250, 0.7);
    list-style: none;
    animation: change 5s linear infinite;
  }

  a {
    text-decoration: none;
    font-size: var(--link_size);
  }

  li {
    margin: 5vw 2vw;
    text-align: left;
    color: var(--link_color);
    font-size: var(--link_size);
    font-weight: bold;
  }
}
</style>
