<template>
  <div>
    <!-- Hero section -->
    <div>
      <div class="d-none d-sm-flex" style="width: 100%">
        <Desktop style="width: 100%" />
      </div>
      <div class="d-flex d-sm-none">
        <Mobile />
      </div>
      <div></div>

      <!-- Why purchase -->
      <Why />
      <!-- Best -->
      <Best />
    </div>

  </div>
</template>

<script>
import Desktop from "./Desktop/hero.desktop.vue";
import Mobile from "./Mobile/hero.mobile.vue";
import Why from "./why.home.vue";
import Best from "./best.home.vue"
// import Tablet from './Tablet/hero.tablet.vue'
export default {
  components: {
    Desktop,
    Mobile,
    // Tablet
    Why,
    Best
  },
};
</script>

<style>
</style>