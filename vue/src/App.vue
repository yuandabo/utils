<template>
  <div style="height: 100vh; width: 80vw">
    <VirtualList :listData="data" :itemSize="50" />
  </div>
</template>

<script setup>
import VirtualList from "./components/VisualListAutoHeight.vue";
// import { faker } from "@faker-js/faker";
import { ref } from "vue";

const data = ref([]);
for (let i = 0; i < 1000; i++) {
  data.value.push({
    index: i,
    value: 123,
  });
}
</script>

<style>
html {
  height: 100%;
}

body {
  height: 100%;
  margin: 0;
}

#app {
  height: 100%;
}
</style>
