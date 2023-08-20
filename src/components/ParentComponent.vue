<script setup>

import ChildComponent from "./ChildComponent.vue";
import {ref} from "vue";

const message = ref('Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsam, quia.');

const emittedMessage = ref('');

const handleMessage = (message) => {
  console.log(message);
  emittedMessage.value = message;
};

</script>

<template>
  <h1>ParentComponent</h1>
  <h1>{{ emittedMessage }}</h1>
  <ChildComponent @messageEmitted="handleMessage" :message="message"/>
</template>

<style scoped>

</style>