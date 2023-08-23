<script setup>
import { ref } from 'vue';
import CompA from './CompA.vue';

const msg = ref('Hello World!');

const show = ref(true);
</script>

<template>
  <h1>{{ msg }}</h1>
  <comp-a v-if="show"></comp-a>
  <button
    @click="
      () => {
        show = false;
      }
    "
  >
    Destroy
  </button>
</template>
