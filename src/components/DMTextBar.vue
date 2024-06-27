<template>
  <div class="text-bar">
    <h2 v-for="(word, index) in repeatedWords" :key="index">{{ word }}</h2>
  </div>
</template>

<script setup lang="ts">
  // reactive gör en vanlig JavaScript-variabel reaktiv,
  // vilket betyder att Vue automatiskt spårar ändringar i den
  // och uppdaterar DOM när värdet ändras.
  import { reactive } from 'vue'

  // Här definierar vi en typ för props som vår komponent kommer att ta emot.
  // I detta fall är words en array av strängar.
  type Props = {
    words: string[]
  }

  // Här använder vi defineProps för att deklarera att vår komponent
  // kommer att ta emot props av typen Props. Detta gör props-objektet
  // tillgängligt för att använda de data som skickas in i komponenten.
  // defineProps är en funktion i Vue 3 som används för att deklarera props i
  // <script setup> blocket.
  const props = defineProps<Props>()

  // Vi skapar en reaktiv array repeatedWords som är av typen string[]
  // (en array av strängar).
  // Genom att använda reactive gör vi arrayen reaktiv,
  // vilket innebär att Vue automatiskt kommer att spåra och reagera
  // på förändringar i arrayen.
  const repeatedWords = reactive<string[]>([])

  for (let i = 0; i < 100; i++) {
    // ... (spridningsoperatorn) används för att lägga till varje element i
    // props.words som separata element i repeatedWords.
    repeatedWords.push(...props.words)
  }
</script>

<style scoped>
  .text-bar {
    background: var(--dm-yellow);
    border-top: var(--dm-stroke-weight) solid var(--dm-black);
    border-bottom: var(--dm-stroke-weight) solid var(--dm-black);
    display: grid;
    grid-auto-flow: column;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
    margin: 7rem 0;
  }

  h2 {
    margin: 0;
    padding: 0;
    font-family: var(--dm-sans-font);
    text-transform: uppercase;
    line-height: 0.5rem;
    margin-left: 1rem;
    white-space: nowrap;
    padding: 1rem 0.5rem;
  }
</style>
