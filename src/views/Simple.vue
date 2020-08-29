
<template>
  <transition :css="false">
    <div class="card"></div>
  </transition>
</template>

<script>
import gsap from 'gsap'
export default {
  mounted() {
    gsap.from('.card', {
      duration: 1,
      opacity: 0,
      scale: 0,
      ease: 'bounce.outut',
    })
  }
}
</script>

<style scoped>
.card {
  display: block;
  margin: 0 auto 0 auto;
  height: 6.5em;
  width: 6.5em;
  border-radius: 1%;
  background-color: #16c0b0;
  box-shadow: 0.08em 0.03em 0.4em #ababab;
}
</style>