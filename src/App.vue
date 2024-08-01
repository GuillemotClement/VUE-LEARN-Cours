<template>
  <button @click="myVal = !myVal">Afficher</button>
  <h1 v-if="myVal">Hello</h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  const myVal = ref(true);
</script>

<style scoped lang="scss"></style>
