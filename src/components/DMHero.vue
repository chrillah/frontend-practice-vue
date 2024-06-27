<template>
  <div class="hero-wrapper grid-container">
    <div></div>
    <div class="hero grid-item">
      <div class="title-wrapper">
        <div class="top">
          <h1>SPRING,</h1>
        </div>
        <div class="bottom">
          <h1>SUMMER</h1>
          <div>
            <h2>COLL.</h2>
            <h2>24</h2>
          </div>
        </div>
      </div>

      <div class="image-wrapper">
        <DMHeroImage
          image="/hero-image-2.png"
          number="01"
          typeOfProduct="man"
        />
        <DMHeroImage
          image="/hero-image-1.png"
          number="02"
          typeOfProduct="wmns"
        />
      </div>

      <button class="button-wrapper">
        <p>explore</p>
        <svg
          id="Layer_1"
          data-name="Layer 1"
          xmlns="http://www.w3.org/2000/svg"
          width="40"
          height="40"
          viewBox="0 0 40 40"
        >
          <path
            class="button-detail"
            d="M33.95,6.11C28.79.26,21.28-1.58,13.87,1.2,5.79,4.22.32,11.82.26,20.12H.26c.22,8.21,5.42,15.44,13.24,18.41,2.33.88,4.68,1.32,6.98,1.32,5.04,0,9.84-2.08,13.57-6.06,3.87-3.77,5.98-8.71,5.95-13.92-.03-5.18-2.18-10.07-6.05-13.76ZM20.02,1.9c.11,0,.22,0,.33,0,4.11,0,8.54,2.03,12.2,5.6,3.85,3.53,6.08,8.39,6.11,13.32.03,4.62-1.87,8.96-5.36,12.23-4.79,5.02-12.31,6.39-19.61,3.58C6.13,33.71,1.12,27.23.93,20.12.91,10.19,10.79,2.68,20.02,1.9Z"
          />
          <polygon
            class="button-detail"
            points="10.29 21.15 28.45 21.33 25.72 23.66 20.31 27.92 21.59 29.54 22.5 28.82 22.66 29 27.07 25.23 33.08 20.5 32.83 20.3 33.03 20.12 23.18 11.65 22.97 11.88 21.62 10.73 20.28 12.29 28.45 19.27 12.01 19.11 9.9 19.01 9.88 19.53 10.31 19.55 10.29 21.15"
          />
        </svg>
      </button>
    </div>
  </div>
</template>
<script setup lang="ts">
  import DMHeroImage from './DMHeroImage.vue'
</script>
<style scoped>
  .hero-wrapper {
    margin-top: 6rem;
  }
  .hero {
    width: 100%;
    display: grid;
    gap: 1rem;
  }

  .image-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  h1 {
    margin: 0;
    padding: 0;
    font-family: var(--dm-sans-font);
    font-size: 7rem;
    text-align: right;
    line-height: 5.5rem;
    color: var(--dm-black);
  }

  h2 {
    margin: 0;
    padding: 0;
    font-family: var(--dm-script-font);
    text-align: center;
    line-height: 3rem;
    font-size: 3rem;
    color: var(--dm-black);
  }

  .bottom {
    display: flex;
    gap: 1rem;
  }

  .bottom div {
    padding-top: 1rem;
  }

  p {
    margin: 0;
    padding: 0;
    font-family: var(--dm-sans-font);
    text-transform: uppercase;
    color: var(--dm-black);
  }

  .button-detail {
    fill: var(--dm-black);
    stroke-width: 0px;
  }

  button {
    background: none;
    border: none;
    cursor: pointer;
  }

  .button-wrapper {
    margin-left: auto;
    display: flex;
    align-items: center;
    gap: 8px;
  }
</style>
