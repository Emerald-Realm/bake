<template>
  <div class="the-header">
    <div class="desktop">
      <DesktopMenuNav />
    </div>
  </div>
</template>

<script>
import DesktopMenuNav from "./DesktopMenuNav";

export default {
  components: { DesktopMenuNav },
  name: "MenuNav",
};
</script>

<style>
.the-header {
  position: sticky;
  z-index: 100;
  top: 0;
  left: 0;
  margin: 0vw 5vw;
}

.desktop {
  display: none;
}

.close-menu {
  width: 50vw;
  padding: 2vw;
  position: sticky;
}

@media screen and (min-width: 800px) {
  .desktop {
    display: block;
  }
}
</style>