<template>
  <h1
    :style="{
      fontSize: fontSize + 'px'
    }"
  >
    Hello
  </h1>
  <button @click="fontSize += 5">+</button>
  <button @click="fontSize -= 5">-</button>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const fontSize = ref(15);
</script>

<style scoped></style>
