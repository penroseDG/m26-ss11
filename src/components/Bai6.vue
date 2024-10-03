<template>
  <div>
    <h1>count: {{ count }}</h1>
    <button @click="handleclick">Increment</button>
  </div>
</template>

<script  setup>
import { onUpdated, ref } from 'vue';

const count=ref(0)
const handleclick=()=>{
    count.value++;
}
onUpdated(()=>{
    document.title=count.value
})
</script>

<style>

</style>