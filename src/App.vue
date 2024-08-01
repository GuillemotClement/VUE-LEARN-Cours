<template>
  <h1
    :style="{
      fontSize,
      color
    }"
  >
    Hello
  </h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const fontSize = ref('130px');
  const color = ref('red');
</script>

<style scoped></style>
