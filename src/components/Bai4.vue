<template>
  <div>
    <h1>age: {{ age}}</h1>
    <button @click="handleClick">Increase age</button>
  </div>
</template>

<script  setup>
import { onUpdated, ref } from 'vue';


const age=ref(1)
const handleClick=()=>{
    age.value++;
}
onUpdated(()=>{
    alert("giá trị của biến age đã thay đổi")
})
</script>

<style>

</style>