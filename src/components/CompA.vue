<script setup>
import { onBeforeUnmount, onUnmounted, ref } from 'vue';
import CompB from './CompB.vue';

const msg = ref('Component A!');

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
    <comp-b></comp-b>
  </div>
</template>

<style scoped>
.wrapper {
  border: solid 1px black;
  padding: 5px;
}
</style>
