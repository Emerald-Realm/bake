<template>
  <div class="desktop-menu" id="product-menu">
    <ul class="navbar">
      <a href="#cake" @click="scrollToTop()" class="nav-link">
        <li>Cakes</li>
      </a>
      <a href="#pastery" class="nav-link">
        <li>Pasteries</li>
      </a>
      <a href="#custom-cake" class="nav-link">
        <li>Custom-cakes</li>
      </a>
      <a href="#bread" class="nav-link">
        <li>Breads</li>
      </a>
      <a href="#snack" class="nav-link">
        <li>Snacks</li>
      </a>
      <a href="#cookie" class="nav-link">
        <li>Cookies</li>
      </a>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DesktopMenuNav",
};
</script>

<style scoped>

.desktop-menu {
  display: none;
}

@media screen and (min-width: 800px) {

.desktop-menu {
  display: block;
}
  .hide {
    display: none;
  }

  .menu {
    display: none;
  }

  #menu-product {
    padding: 0.5vw 0vw 0vw 0vw;
  }

  .navbar {
    position: sticky;
    width: 9vw;
    text-align: left;
    display: flex;
    display: grid;
    align-items: center;
    justify-content: space-between;
    list-style: none;
    margin: 0;
    padding: 20vh 0vh 20vh 0vh;
  }
  .nav-link {
    text-decoration: none;
    margin: 0.5vw 0vw 0.5vw 0vw;
  }

  .nav-link:hover {
    color: burlywood;
  }
}
</style>
