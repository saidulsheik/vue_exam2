<template>
  <div id="app">
    <h1>Calculator</h1>
    <Calculator />
    <h1>Random Anime Quote</h1>
    <AnimeQuote />
  </div>
</template>

<script setup>
import Calculator from './components/Calculator.vue';
import AnimeQuote from './components/AnimeQuote.vue';
</script>


<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
