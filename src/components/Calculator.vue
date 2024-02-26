<template>
    <div>
      <input type="number" v-model="num1" placeholder="Enter number">
      <select v-model="operator">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
      </select>
      <input type="number" v-model="num2" placeholder="Enter number">
      <button @click="calculate">Calculate</button>
      <div v-if="result !== null">
        Result: {{ result }}
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const num1 = ref(null);
  const num2 = ref(null);
  const operator = ref('+');
  const result = ref(null);
  
  const calculate = () => {
    switch(operator.value) {
      case '+':
        result.value = parseFloat(num1.value) + parseFloat(num2.value);
        break;
      case '-':
        result.value = parseFloat(num1.value) - parseFloat(num2.value);
        break;
      case '*':
        result.value = parseFloat(num1.value) * parseFloat(num2.value);
        break;
      case '/':
        result.value = parseFloat(num1.value) / parseFloat(num2.value);
        break;
      default:
        result.value = null;
    }
  };
  </script>