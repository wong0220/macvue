<template>
  테스트다
  <input type="text" @input="setText" :value="text" />
  <div>
    <div v-if="comput" style="font-size: 50px">
      {{ Math.random() * 10 }}
    </div>
    짠박스
  </div>
</template>

<script setup>
import { computed } from "@vue/reactivity";
import { ref } from "vue";

const text = ref("");

const setText = (e) => {
  text.value = e.target.value;
};

const comput = computed(() => {
  return text.value.length > 0;
});
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
