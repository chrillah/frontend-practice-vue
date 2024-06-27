<template>
  <div class="carousel">
    <DMProductItem v-for="product in products" :product="product" />
  </div>
</template>

<script setup lang="ts">
  import DMProductItem from './DMProductItem.vue'

  type Product = {
    image: string
    name: string
    oldPrice: number
    newPrice: number
  }

  const products: Product[] = [
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
  ]
</script>

<style scoped>
  .carousel {
    display: grid;
    grid-auto-flow: column;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
    gap: 1rem;
    padding-bottom: 4rem;
  }
</style>
