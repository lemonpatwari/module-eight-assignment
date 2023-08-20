<script setup>

import {defineProps, defineEmits} from 'vue';
defineProps(['message'])

const emit = defineEmits(['messageEmitted'])

const emitMessage = () => {
  emit('messageEmitted', 'Hello from ChildComponent');
};

</script>

<template>
  <h1>ChildComponent</h1>
  <p class="text-yellow-600">{{ message }}</p>

  <button @click="emitMessage" class="bg-blue-500 hover:bg-blue-700 text-white font-bold my-8 py-2 px-4 rounded">
    Button
  </button>
</template>

<style scoped>

</style>