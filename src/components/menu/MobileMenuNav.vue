<template>
  <div class="mobile-header" id="home">
    <div class="logo-row">
      <p>logo</p>
      <button class="menu" @click="handleMenu()">
        {{ status ? "Close" : "Menu" }}
      </button>
    </div>
    <ul class="navbar">
      <a href="#home" @click="scrollToTop()" class="nav-link">
        <li>Home</li>
      </a>
      <a href="#service" class="nav-link">
        <li>Service</li>
      </a>
      <a href="#product" class="nav-link">
        <li>Products</li>
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
      <a href="#" @click="handleSide()" class="nav-link">
        <li>Menu</li>
      </a>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MobileMenuNav",
  data() {
    return {
      status: false,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    },
    handleMenu() {
      this.status = !this.status;
      const navbar = document.querySelector(".mobile-header");
      if (this.status) {
        navbar.classList.add("show-navbar");
      } else {
        navbar.classList.remove("show-navbar");
      }
    },
    handleSide() {
      const sideMenu = document.querySelector(".side-menu");
      console.log(this.fall);
      this.fall = !this.fall;
      if (this.fall) {
        sideMenu.classList.add("tall");
      } else {
        sideMenu.classList.remove("tall");
      }
    },
  },
};
</script>

<style scoped>
@media screen and (max-width: 799px) {
  .logo-row {
    display: flex;
    gap: 70vw;
    margin: 0vw 5vw;
    align-items: center;
    justify-content: space-between;
  }

  .menu {
    display: block;
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
    background-color: azure;
    list-style: none;
    /* animation: change 1s forwards; */
  }

  a {
    text-decoration: none;
  }

  li {
    margin: 5vw 2vw;
    text-align: left;
  }
}
</style>
