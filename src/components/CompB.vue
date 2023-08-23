<script setup>
import { onBeforeUnmount, onUnmounted, ref } from 'vue';
import CompC from './CompC.vue';

const msg = ref('Component B!');

onBeforeUnmount(() => {
  console.log(msg.value, ' before unmounted');
});

onUnmounted(() => {
  console.log(msg.value, ' unmounted');
});
</script>

<template>
  <div class="wrapper">
    <h1>{{ msg }}</h1>
    <comp-c></comp-c>
  </div>
</template>

<style scoped>
.wrapper {
  border: solid 1px black;
  padding: 5px;
}
</style>
