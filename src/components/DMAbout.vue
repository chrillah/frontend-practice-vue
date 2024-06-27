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

  .link {
    color: var(--dm-black);
  }

  a {
    text-transform: uppercase;
  }

  h3 {
    font-size: 2.35rem;
  }

  @media (max-width: 868px) {
    h3 {
      font-size: 1.5rem;
    }
  }
</style>
