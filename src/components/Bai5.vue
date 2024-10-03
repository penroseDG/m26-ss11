<template>
  <div>
    <Bai5chidren v-if="show"></Bai5chidren>
    <button @click="handleclick">Toggle</button>
  </div>
</template>

<script  setup>
import { onBeforeUnmount, onUnmounted, ref } from 'vue';
import Bai5chidren from './Bai5chidren.vue';
const show=ref(false)
const handleclick=()=>{
    show.value=!show.value
}


</script>

<style>

</style>