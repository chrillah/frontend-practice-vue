<template>
  <div class="grid-container">
    <div></div>
    <div class="wrapper grid-item">
      <div class="top">
        <a href="#">{{ linkText }}</a>
        <h3 v-html="topText"></h3>
      </div>
      <div class="bottom">
        <h3>{{ bottomText }}</h3>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  const linkText = 'who we are'
  const topText: string = 'An independent <a href="#" class="link">brand</a> of'
  const bottomText: string =
    'urban trekking shoes and accessories that comes from a convergence of arts and personalities'
</script>

<style scoped>
  .wrapper {
    display: grid;
    grid-template-rows: auto auto;
  }

  .top {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  a,
  h3 {
    margin: 0;
    padding: 0;
    color: var(--dm-black);
    font-family: var(--dm-sans-font);
  }

  h3{
    text-align: right;
  }

  .link {
    color: var(--dm-black);
  }

  a {
    text-transform: uppercase;
  }

  h3 {
    font-size: 1rem;
    /* font-size: 1.3rem; */
  }

  @media (max-width: 630px) {
    .grid-container {
      grid-template-columns: 1fr;
    }
  }

  @media (min-width: 420px) {
    h3 {
      font-size: 1rem;
      text-align: left;
    }
  }

  @media (min-width: 450px) {
    h3 {
      font-size: 1.3rem;
    }
  }

  @media (min-width: 550px) {
    h3 {
      font-size: 1.8rem;
    }
  }

  @media (min-width: 630px) {
    h3 {
      font-size: 1rem;
    }
  }

  @media (min-width: 700px) {
    h3 {
      font-size: 1.3rem;
    }
  }

  @media (min-width: 840px) {
    h3 {
      font-size: 1.8rem;
    }
  }

  @media (min-width: 1012px) {
    h3 {
      font-size: 2.35rem;
    }
  }
</style>
