<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <button @click="count++">Count is: {{ count }}</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const message = "hello this is my first Vue"
    const count = ref(0); 
    return {
      message,
      count
     }; 
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
