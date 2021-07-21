<template>
  <div class="contact H-row" id="contact">
    <p class="header-two">Contact Us</p>
    <div class="desktop-contact-us">
      <ul class="contact-one">
        <li class="contact-one-item item">Address</li>
        <li class="contact-one-item item">Email</li>
        <li class="contact-one-item item">Whatsapp</li>
      </ul>
      <ul class="contact-two">
        <li class="contact-two-item item">BakerExampleaddress</li>
        <li class="contact-two-item item">Bakerabc@example.com</li>
        <li class="contact-two-item item">0123456789</li>
      </ul>
    </div>
    <div class="mobile-contact-us">
      <ul class="contact-three">
        <li class="contact-three-item item">Address</li>
        <li class="contact-three-item item">BakerExampleaddress</li>
        <li class="contact-three-item item">Email</li>
        <li class="contact-three-item item">Bakerabc@example.com</li>
        <li class="contact-three-item item">Whatsapp</li>
        <li class="contact-three-item item">0123456789</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style scoped>
.mobile-contact-us {
  display: none;
}

/* .contact {
  margin: 0vw 5vw;
} */

.desktop-contact-us {
  display: flex;
  align-items: center;
  justify-content: center;
}

.contact-one,
.contact-two {
  width: 30vw;
  list-style: none;
  text-align: left;
  padding: 2vw 2vw;
}

.contact-one {
  list-style: none;
  text-align: right;
  border-right: solid 2px burlywood;
}
.item {
  margin: 0.5vw 0.5vw;
}

@media screen and (max-width: 799px) {
  .mobile-contact-us {
    display: block;
  }

  .desktop-contact-us {
    display: none;
  }

  .contact-three {
    display: grid;
    grid-template-columns: 1fr 1fr;
    list-style: none;
    text-align: left;
    padding: 0vw;
    margin: 0vw;
  }

  .item:nth-child(even) {
    padding-left: 4vw;
  }

  .item:nth-child(odd) {
    border-right: 2px solid burlywood;
    padding-right: 4vw;
    text-align: right;
  }
}
</style>
