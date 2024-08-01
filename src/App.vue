<template>
  <h1 :style="h1style">Hello</h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  const h1style = ref('color:red;');
</script>

<style scoped></style>
