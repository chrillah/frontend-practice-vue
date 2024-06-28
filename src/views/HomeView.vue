<template>
  <DMHero />
  <DMTextBar :words="['deplace shop • ', 'do not scroll • ']" />
  <DMAbout />
  <DMItems />
  <DMGibson />
</template>
<script setup lang="ts">
  import DMHero from '../components/DMHero.vue'
  import DMTextBar from '../components/DMTextBar.vue'
  import DMAbout from '../components/DMAbout.vue'
  import DMItems from '../components/DMItems.vue'
  import DMGibson from '../components/DMGibson.vue'
</script>
<style scoped></style>
