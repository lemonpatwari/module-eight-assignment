<script setup>

import ChildComponent from "./ChildComponent.vue";
import {ref} from "vue";

const message = ref('Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsam, quia.');

const emittedMessage = ref('');

const handleMessage = (message) => {
  emittedMessage.value = message;
};

</script>

<template>
  <h1>ParentComponent</h1>
  <h1 class="font-bold text-lg">{{ emittedMessage }}</h1>
  <ChildComponent class="" @messageEmitted="handleMessage" :message="message"/>
</template>

<style scoped>

</style>