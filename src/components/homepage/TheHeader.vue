<template>
  <div class="the-header">
    <div class="desktop">
      <DesktopHeader />
    </div>
    <div class="mobile">
      <MobileHeader />
    </div>
  </div>
</template>

<script>
import DesktopHeader from "./DesktopHeader";
import MobileHeader from "./MobileHeader";

export default {
  components: { DesktopHeader, MobileHeader },
  name: "TheHeader",
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

@media screen and (max-width: 799px) {
  .the-header {
    height: 5vh;
  }
}

@media screen and (min-width: 800px) {
  .desktop {
    display: block;
  }
  .mobile {
    display: none;
  }
}
</style>