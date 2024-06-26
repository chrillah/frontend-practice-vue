<template>
  <nav>
    <router-link to="/"><p class="logo">DÉPLACÉ MAISON</p></router-link>
    <div class="link-container">
      <svg
        id="Layer_1"
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        width="80"
        height="35"
        viewBox="0 0 80 10"
      >
        <path
          class="bg-detail"
          d="M3.34,4.13s14.52-1.99,21.55-2.75S59.55,0,67.2,0c30.38,0,32.8,4.02,32.8,4.02,0,0-1.08,17.62-1.08,18.54,0,.76.75,19.23,1,25.44.04,1.09-.84,1.99-1.94,1.97l-93.14-1.82c-1.85-.04-3.42-1.36-3.75-3.18-.68-3.68-1.62-9.41-1.09-10.33.78-1.38,1.54-9.32,1.24-11.01S1.58,4.37,3.34,4.13Z"
        />
      </svg>
      <div class="links">
        <router-link to="/"><p>Home</p></router-link>
        <router-link to="/about"><p>About</p></router-link>
      </div>
    </div>
    <div class="smudge">
      <svg
        id="Layer_1"
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        width="20.7"
        height="14.4"
        viewBox="0 0 20.7 14.4"
      >
        <path
          class="smudge-detail"
          d="M0,3.46c0,4.43,3.17,8.89,8.38,10.57s12.51-2.6,12.31-6.46c-.17-3.47-2.37-5.05-7.58-6.73S0-.02,0,3.46Z"
        />
      </svg>
    </div>
    <DMCart />
  </nav>
</template>
<script setup lang="ts">
  import DMCart from './DMCart.vue'
</script>
<style scoped>
  nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    padding: 0 1rem;
  }

  .logo {
    position: relative;
    top: 50px;
    left: -50px;
    font-family: var(--dm-display-font);
    font-size: 2rem;
    rotate: -90deg;
  }

  .link-container {
    left: 50%;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .links {
    position: absolute;
    top: 7px;
    display: flex;
    justify-content: space-between;
    width: 65px;
  }

  .bg-detail {
    fill: var(--dm-peach);
    stroke-width: 0px;
  }

  .smudge {
    position: absolute;
    top: 0;
    right: 15%;
  }
  .smudge-detail {
    fill: var(--dm-black);
    stroke-width: 0px;
  }

  p {
    font-family: var(--dm-script-font);
  }

  a {
    text-decoration: none;
    color: var(--dm-black);
    font-size: 10px;
  }
</style>
