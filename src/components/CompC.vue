<script setup>
import { onBeforeUnmount, onUnmounted, ref } from 'vue';

const msg = ref('Component C!');

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
  </div>
</template>

<style scoped>
.wrapper {
  border: solid 1px var(--border-color);
  padding: 5px;
}
</style>
