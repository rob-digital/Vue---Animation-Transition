<template>
  <div>
    <img class="runner first" src="../assets/runner.png" alt="runner" />
    <img class="runner second" src="../assets/runner.png" alt="runner" />
    <img class="runner third" src="../assets/runner.png" alt="runner" />
  </div>
</template>

<script>
import gsap from 'gsap'

export default {
  mounted() {
   let tl = gsap.timeline({repeat: 2, repeatDelay: 1}) // if set to -1 ir gives infinite loop
   tl.to('.first', {x: 700, duration:2, ease: 'expo.out'})
   tl.to('.second', {x: 700, duration:2, ease: 'expo.out'}, 0.5)
   tl.to('.third', {x: 700, duration:2, ease: 'expo.out'}, '<') // < - means start with the previous
  }
}
</script>

<style scoped>
.runner {
  display: block;
  height: 5em;
  width: 5em;
  margin-top: 1.5em;
}
</style>
