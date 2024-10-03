<template>
  <div>
    <h1>Children component</h1>
    <h2>count: {{ count }}</h2>
    <input type="text" v-model="inputvalue">
    <button @click="handleClick">count</button>
  </div>
</template>

<script  setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUpdated, ref } from 'vue';
const count = ref(0)
const inputvalue=ref("")
//  các phương thức trong giai đoạn khởi tạo (createtion)
onBeforeMount(()=>{
    console.log("component before mount");
    
})

onMounted(()=>{
    console.log("component mounted");
    // count.value=2
})

onBeforeUpdate(()=>{
    console.log("before update");
    document.title=inputvalue.value
    
})
onUpdated(()=>{

})
const handleClick=()=>{
    count.value++;

}
// các phương thức trong giai đoạn unmount
onBeforeUnmount(()=>{
    
})
</script>

<style>

</style>