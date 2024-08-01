<template>
  <h1 :style="h1Style">Hello</h1>
</template>

<script lang="ts" setup>
  import { reactive, ref } from 'vue';

  const h1Style = reactive({
    fontSize: '90px',
    color: 'red'
  });
</script>

<style scoped></style>
