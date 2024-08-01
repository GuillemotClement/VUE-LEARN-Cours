<template>
  <h1
    :class="{
      red: h1class
    }"
  >
    Hello
  </h1>
  <button @click="h1class = !h1class">Change</button>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const h1class = ref(true);
</script>

<style scoped>
  .red {
    color: red;
  }
</style>
