<template>
  <div class="about-us H-row" id="about">
    <p class="header-two">About Us</p>
    <div class="About">
      <img
        src="../../assets/media/hand1xx.jpg"
        alt="about us"
        class="about-img"
      />
      <p class="about-context">
        In our pursuit of the ultimate limit of a perfect baking product, we
        ventuered into the kitchen to communicate our desire to the oven, also
        to offer you our discoveries and progress.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.About {
  margin: 2vw 10vw;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10vw;
}

img {
  order: 2;
  width: 40vw;
  flex-grow: 0;
  border-radius: 2%;
}

.about-context {
  text-align: left;
}

@media screen and (max-width: 799px) {
  .About {
    flex-direction: column;
    gap: 0vw;
  }
  img {
    order: 0;
    width: 80vw;
  }
}
</style>