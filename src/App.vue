<template>
  테스트다
  <input type="text" @text="setText" :value="text" />
</template>

<script setup>
import { ref } from "vue";

const text = ref("");

const setText = (e) => {
  text.value = e.target.value;
  console.log(text.value);
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
