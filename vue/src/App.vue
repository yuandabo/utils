<script setup lang="ts">
import VisualList from "./components/VisualList.vue";
import { ref } from "vue";

const data = ref<any[]>([]);
for (let i = 0; i < 1000; i++) {
  data.value.push({ id: i, value: i });
}
</script>

<template>
  <div style="height: 100vh; width: 100vw">
        
    <VisualList :listData="data" :itemSize="100" />
      
  </div>
</template>

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
