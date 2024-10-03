<template>
  <div>
    <h1>Counter: {{ count }}</h1>
    <button @click="handleclick">count</button>
  </div>
</template>

<script setup>
import {  onUpdated, ref } from 'vue';

const count=ref(0)
const handleclick=()=>{
    count.value++;
}
onUpdated(()=>{
    console.log("dữ liệu đã thay đổi");
    
})
</script>

<style>

</style>