<template>
    <div>
      <button @click="fetchQuote">Get Random Anime Quote</button>
      <div v-if="quote">
        <p>{{ quote.quote }}</p>
        <p>- {{ quote.character }}, {{ quote.anime }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const quote = ref(null);
  
  const fetchQuote = async () => {
    try {
      const response = await fetch('https://animechan.xyz/api/random');
      const data = await response.json();
      quote.value = data;
    } catch (error) {
      console.error('Error fetching quote:', error);
    }
  };
  </script>
  