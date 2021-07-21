<template>
  <div class="philosophy H-row" id="philosophy">
    <div class="philosophy-context">
      <p class="p-content">Eating that brings Happiness</p>
      <cite class="p-cite">by ceo</cite>
    </div>
  </div>
</template>

<script>
export default {
  name: "Philosophy",
};
</script>

<style scoped>
.philosophy {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.background-gif {
  position: relative;
  width: 90vw;
}
video {
  width: 100%;
  z-index: -1;
}

@media (min-aspect-ratio: 16/9) {
  video {
    width: 100%;
  }
}

@media (max-aspect-ratio: 16/9) {
  video {
    width: 100%;
  }
}

.philosophy-context {
  position: absolute;
  color: whitesmoke;
}
.p-content {
  font-size: 5vw;
}

.p-cite {
  font-size: 2vw;
}
</style>
