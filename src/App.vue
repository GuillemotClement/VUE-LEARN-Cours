<template>
  <h1 :class="[h1class, h1class2]">Bonjour</h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const h1class = ref('hello');
  const h1class2 = ref('world');
</script>

<style scoped>
  .red {
    color: red;
  }
</style>
