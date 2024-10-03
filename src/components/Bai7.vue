<template>
  <div>
    <input type="text" v-model="inputvalue">
  </div>
</template>

<script  setup>
import { onUpdated, ref } from 'vue';
const inputvalue=ref('')
onUpdated(()=>{
    document.title=inputvalue.value
})
</script>

<style>

</style>