<template>
  <div class="carousel">
    <DMProductItem v-for="product in products" :product="product" />
  </div>
</template>

<script setup lang="ts">
  import DMProductItem from './DMProductItem.vue'

  export type Product = {
    image: string
    name: string
    oldPrice: number
    newPrice: number
  }

  const products: Product[] = [
    {
      image: '/frontend-practice-misc_cactus.png',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '/frontend-practice-misc_duran.png',
      name: 'Duran',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_the-eye.png',
      name: 'The eye',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_carnera.png',
      name: 'Carnera',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_cactus.png',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '/frontend-practice-misc_duran.png',
      name: 'Duran',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_the-eye.png',
      name: 'The eye',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_carnera.png',
      name: 'Carnera',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_cactus.png',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '/frontend-practice-misc_duran.png',
      name: 'Duran',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_the-eye.png',
      name: 'The eye',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_carnera.png',
      name: 'Carnera',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_cactus.png',
      name: 'Cactus',
      oldPrice: 300,
      newPrice: 180
    },
    {
      image: '/frontend-practice-misc_duran.png',
      name: 'Duran',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_the-eye.png',
      name: 'The eye',
      oldPrice: 240,
      newPrice: 144
    },
    {
      image: '/frontend-practice-misc_carnera.png',
      name: 'Carnera',
      oldPrice: 240,
      newPrice: 144
    }
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
