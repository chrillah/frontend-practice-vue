<template>
  <div class="container">
    <div class="extra"></div>
    <div class="item">
      <div class="gibson">
        <svg
          id="Layer_1"
          data-name="Layer 1"
          xmlns="http://www.w3.org/2000/svg"
          width="144.01"
          height="113.73"
          viewBox="0 0 144.01 113.73"
        >
          <path
            class="plate-detail"
            d="M1.96,93.59s3.06-14.33,4.73-21.21,10.47-33.07,13.06-40.26C30.07,3.54,34.67,2.63,34.67,2.63c0,0,16.2,4,17.07,4.31.72.26,22.35,2.83,28.27,4.69,1.04.33,1.59,1.47,1.2,2.49l-36.33,84.99c-.66,1.72-2.44,2.75-4.26,2.45-3.69-.61-9.4,1.32-10.09.52-1.03-1.2-9.25.38-10.93.1S1.59,95.33,1.96,93.59Z"
          />
          <path
            class="plate-detail"
            d="M61.28,100.8s3.06-14.33,4.73-21.21,10.47-33.07,13.06-40.26c10.31-28.58,14.92-29.49,14.92-29.49,0,0,16.2,4,17.07,4.31.72.26,22.35,2.83,28.27,4.69,1.04.33,1.59,1.47,1.2,2.49l-36.33,84.99c-.66,1.72-2.44,2.75-4.26,2.45-3.69-.61-11.03-8.49-12.09-8.48-10.77.14-7.25,5.38-8.93,5.1s-17.99-2.86-17.62-4.59Z"
          />
        </svg>
        <p>{{ text1 }}</p>
      </div>
      <p class="text2">{{ text2 }}</p>
    </div>
  </div>
</template>
<script setup lang="ts">
  const text1: string = 'William Gibson'
  const text2: string = `Good things come to
  those who wait - Déplacé Maison is what has been missing
  in the modern fashion industry for years.
  Buy a shoe of high quality and design it finally happened`
</script>
<style scoped>
  p {
    margin: 0;
    padding: 0;
  }

  .container,
  .item {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .extra{
    display: none;
  }
  .gibson {
    position: relative;
    display: flex;
    align-items: center;
  }

  .plate-detail {
    fill: none;
    stroke: var(--dm-black);
    stroke-width: 1px;
  }

  .gibson p {
    position: absolute;
    padding-left: 4rem;
    font-family: var(--dm-script-font);
    font-size: 2rem;
  }

  .text2 {
    font-family: var(--dm-sans-font);
  }
</style>
