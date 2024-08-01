<template>
  <input type="text" v-model="letter" />

  <h1 v-if="letter === 'A'">A</h1>
  <h1 v-else-if="letter === 'B'">B</h1>
  <h1 v-else-if="letter === 'C'">C</h1>
  <h1 v-else>Autre</h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const letter = ref('');
</script>

<style scoped lang="scss"></style>
