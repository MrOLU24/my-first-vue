<script setup>
import { computed,  ref} from "vue";
const message = ref("hello another world vue 3");

</script>

<template>
    <h1>{{ message }}</h1>

</template>