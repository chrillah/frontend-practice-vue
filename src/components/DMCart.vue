<template>
  <div>
    <p>cart</p>
    <p>{{ numberOfItems }}</p>
  </div>
</template>
<script setup lang="ts">
  import { ref } from 'vue'

  const numberOfItems = ref(0)
</script>
<style scoped>
  div {
    display: flex;
    justify-content: space-between;
    width: 50px;
  }

  p {
    font-family: var(--dm-sans-font);
    font-weight: 600;
    text-transform: uppercase;
    font-size: 12px;
  }

  p:last-of-type {
    padding-top: 1px;
  }
</style>
