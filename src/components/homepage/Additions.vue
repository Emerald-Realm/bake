<template>
  <div class="new H-row" id="new">
    <p class="header-two">Our New Additions</p>
    <div class="additions">
      <BaseMenuCard :List="RecommendedList" />
    </div>
  </div>
</template>

<script>
import BaseMenuCard from "../menu/BaseMenuCard";
import RecommendedList from "../../assets/APIs/RecommendedList";

// animate strip
window.addEventListener( 'scroll', handleScroll)
function handleScroll () {
  let service = document.querySelector('.additions')
  let serviceHeight = service.getBoundingClientRect().top
  let windowHeight = window.innerHeight/1.5

  if ( serviceHeight < windowHeight ) {
    service.classList.add('show')
  } else {
    service.classList.remove('show')
  }
}


export default {
  name: "Additions",
  components: {
    BaseMenuCard,
  },
  data() {
    return {
      RecommendedList,
    };
  },
};
</script>

<style >

.additions {
  margin: 0vw 5vw;
  display: flex;
  align-items: center;
  justify-content: space-around;
  transition: 1s all ease;
  opacity: 0;
  overflow-x: scroll;
}
</style>