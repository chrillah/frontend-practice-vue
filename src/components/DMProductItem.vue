<template>
  <div class="item">
    <div class="image-item">
      <img :src="product.image" :alt="product.name">
    </div>
    <div class="graphic-item">
      <svg
        id="Layer_1"
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        width="100"
        height="40"
        viewBox="0 0 80 20"
      >
        <path
          class="bg-detail"
          d="M3.34,4.13s14.52-1.99,21.55-2.75S59.55,0,67.2,0c30.38,0,32.8,4.02,32.8,4.02,0,0-1.08,17.62-1.08,18.54,0,.76.75,19.23,1,25.44.04,1.09-.84,1.99-1.94,1.97l-93.14-1.82c-1.85-.04-3.42-1.36-3.75-3.18-.68-3.68-1.62-9.41-1.09-10.33.78-1.38,1.54-9.32,1.24-11.01S1.58,4.37,3.34,4.13Z"
        />
      </svg>
      <p>unisex</p>
    </div>
    <p class="season">ss/24</p>
    <h1 class="product-name">
      {{ product.name }}
    </h1>
    <p class="old-price">&#8364 {{ product.oldPrice }} eur</p>
    <p class="new-price">&#8364 {{ product.newPrice }} eur</p>
  </div>
</template>

<script setup lang="ts">

export type Product = {
  image: string
  name: string
  oldPrice: number
  newPrice: number
}

defineProps<{ product: Product }>()

</script>

<style scoped>
  p,
  h1{
    margin: 0;
    padding: 0;
  }

  .item {
    border: var(--dm-stroke-weight) solid var(--dm-black);
    background: var(--dm-peach);
    height: 450px;
    width: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .image-item{
    width: 90%;
    height: 45%;
  }

  img {
    width: auto;
    max-width: 100%;
  }

  .graphic-item {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .bg-detail {
    position: absolute;
    fill: var(--dm-black);
    stroke-width: 0px;
  }

  .graphic-item p {
    position: absolute;
    padding-top: 2px;
    font-family: var(--dm-script-font);
    color: var(--dm-peach);
    font-size: 1.7rem;
  }

  .season {
    font-family: var(--dm-sans-font);
    text-transform: uppercase;
    letter-spacing: -1px;
  }

  .product-name{
    line-height: 5rem;
    font-family: var(--dm-display-font);
    font-size: 6rem;
    text-transform: uppercase;
  }

  .old-price,
  .new-price{
    font-family: var(--dm-sans-font);
    font-weight: 600;
    text-transform: uppercase;
  }

  .old-price{
    text-decoration: line-through;
    font-size: 1.2rem;
  }

  .new-price{
    font-size: 1.82rem;
  }
</style>
