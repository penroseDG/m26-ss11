<template>
  <div>
    <h1>Parent Component</h1>
    <button @click="handleClick">chidren  </button>
    <div v-if="click">
        <ChildrenComponent/>
        <Time></Time>
    </div>
  </div>
</template>

<script  setup>
import { ref } from 'vue';
import ChildrenComponent from './ChildrenComponent.vue';
import Time from './Time.vue';

const click=ref(false)
const handleClick=()=>{
    click.value=!click.value

}
</script>

<style>

</style>