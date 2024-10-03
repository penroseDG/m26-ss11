<template>
    <div>
      <h1>Current company: {{ currentCompany }}</h1>
      <h1>age:{{ age }}</h1>
      <button @click="handleRandom">Random</button>
    </div>
  </template>
  
  <script setup>
  import { reactive, ref, computed } from 'vue';
  
  const age = ref(1);
  const companies = reactive(["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"]);
  
  const handleRandom = () => {
      age.value = Math.floor(Math.random() * 10) + 1;
  };
  
  const currentCompany = computed(() => {
      // Lấy chỉ số công ty tương ứng với biến age
      const index = (age.value - 1) % companies.length;
      return companies[index];
  });
  </script>
  
  <style>
  </style>