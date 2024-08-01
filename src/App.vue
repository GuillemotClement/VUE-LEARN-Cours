<template>
  <h1 :class="h1class">Hello</h1>
  <button @click="h1class = 'red'">Change</button>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const h1class = ref('Bonjour');
</script>

<style scoped>
  .red {
    color: red;
  }
</style>
