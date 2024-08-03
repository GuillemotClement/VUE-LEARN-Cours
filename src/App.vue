<template>
  <ul>
    <li v-for="(value, key) of car">{{ key }} : {{ value }}</li>
  </ul>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';
  const car = {
    wheel: 4,
    price: 4000
  };
</script>

<style scoped lang="scss"></style>
