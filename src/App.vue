<template>
  <div class="class">
    <Home />
    <Menu />
  </div>
</template>

<script>
import Home from "./components/Home";
import Menu from "./components/menu/Menu.vue";

export default {
  name: "App",
  components: {
    Home,
    Menu,
  },
};
</script>

<style>
#app {
  --main_color: burlywood;
  --sec_color: bisque;
  --tet_color: blanchedalmond;
  --link_color: brown;
  --link_size: 18px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
  text-decoration: none;
  padding: 0px;
  margin: 0px;
  list-style: none;
  /* margin-top: 60px; */
}

a {
  color: var(--link_color);
}

html {
  scroll-behavior: smooth;
  scroll-margin-top: -5rem;
  scroll-padding-top: 5rem;
}

.header-two {
  font-size: 5vw;
  font-weight: bold;
  color: var(--link_color);
}

@media screen and (min-width: 800px) {
  .H-row {
    padding-top: 5vw;
    margin-top: -5vw;
  }

  .header-two {
    font-size: 2vw;
  }

  hr:not(:first) {
    margin: 3vw 0vw 0vw 0vw;
  }
}
</style>
