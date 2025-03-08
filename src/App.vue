<template>
  <div id="app">
    <div>
      <h1>{{ message }}</h1>
      <HelloWorld />
      <button @click="increment">Count is: {{ count }}</button>
    </div>
    <div class="contain">
      <span class="first-span">
        <span>{{ counter }} </span>
        * {{ value }} =
        <span>{{ double }}</span>
      </span>
      <div class="btn-div">
        <button @click="inc">+1</button>
        <button @click="counter -= 1">-1</button>
        <button @click="reset">Reset</button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

const message = ref("hello world vue 3");
const count = ref(0);
const counter = ref(1);
const value = 2;
const double = computed(() => counter.value * value);

function inc() {
  counter.value++;
}

function increment() {
  count.value++;
  message.value = `Clicked ${count.value} Times go!`;
}

function reset() {
  count.value = 0;
  counter.value = 1;
  message.value = "hello world vue 3";
}
</script>

<style>
#app {
  font-weight: 500;
  font-size: small;
}
</style>