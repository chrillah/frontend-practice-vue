<template>
  <div class="item-container">
    <div class="image-wrapper">
      <img :src="image" alt="An image" />
    </div>
    <div class="detail-wrapper">
      <p>({{ number }})</p>
      <p>{{ typeOfProduct }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
  defineProps({
    image: String,
    number: String,
    typeOfProduct: String
  })
</script>

<style scoped>
  p {
    margin: 0;
    padding: 0;
    font-family: var(--dm-sans-font);
    text-transform: uppercase;
    font-size: 12px;
  }

  .image-wrapper {
    border: var(--dm-stroke-weight) solid var(--dm-black);
    height: 380px;
    overflow: hidden;
    background-color: var(--dm-peach);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media (min-width: 467px) {
    .image-wrapper {
      height: 490px;
    }
  }

  @media (min-width: 625px) {
    .image-wrapper {
      height: 600px;
    }
  }

  @media (min-width: 680px) {
    .image-wrapper {
      height: 380px;
    }
  }

  @media (min-width: 820px) {
    .image-wrapper {
      height: 550px;
    }
  }

  img {
    width: auto;
    max-width: 100%;
  }

  .detail-wrapper {
    padding-top: 5px;
    display: flex;
    justify-content: space-between;
    width: 50%;
  }
</style>
