<template>
  <div class="side-menu">
    <!-- Menu Navigation -->
    <div class="menus-nav">
      <DesktopMenuNav />
    </div>
    <!-- Menu Content -->
    <div class="menus">
      <BaseCategory :categoryList="categoryList" />
    </div>
  </div>
</template>

<script>
import BaseCategory from "./BaseCategory.vue";
import categoryList from "../../assets/APIs/categoryList";
import DesktopMenuNav from "./DesktopMenuNav.vue";

export default {
  name: "Menu",
  components: {
    BaseCategory,
    DesktopMenuNav,
  },
  data() {
    return {
      categoryList,
    };
  },
};
</script>

<style >
.side-menu {
  position: fixed;
  top: 0vh;
  left: 0;
  width: 100vw;
  height: 0vh;
  z-index: 90;
  overflow: scroll;
  background-color: blanchedalmond;
  transition: 1s all ease-in;
}

.menus {
  margin-top: 10vh;
}

.tall {
  height: 100vh;
}

@media screen and (min-width: 800px) {
  .side-menu {
    display: grid;
    grid-template-columns: 10% 80%;
    justify-content: center;
    top: 0vh;
    left: 0;
    width: 100vw;
    height: 0vh;
    overflow: hidden;
    z-index: 90;
    background-color: blanchedalmond;
    transition: 1s all ease-in;
  }

  .tall {
    height: 100vh;
  }

  .menus-nav {
    margin-top: 10vh;
    flex-grow: 0;
    position: sticky;
  }

  .menus {
    margin-top: 20vh;
    overflow-y: scroll;
  }
}
</style>
