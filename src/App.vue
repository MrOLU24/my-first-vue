<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <button @click="increment">Count is: {{ count }}</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const message = ref("hello world vue 3");
const count = ref(0);

function increment() {
  count.value++;
  message.value = `Clicked ${count.value} Times!`
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
