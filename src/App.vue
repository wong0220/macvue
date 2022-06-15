<template>
  테스트다
  <input type="text" @input="setText" :value="text" />
  <div>
    <div v-if="text.length > 0" style="font-size: 50px">왕 짠짠</div>
    짠박스
  </div>
</template>

<script setup>
import { ref } from "vue";

const text = ref("");

const setText = (e) => {
  text.value = e.target.value;
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
