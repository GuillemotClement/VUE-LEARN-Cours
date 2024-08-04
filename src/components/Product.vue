<template>
  <h3>{{ name }}</h3>
</template>

<script setup lang="ts">
  import { ref } from 'vue';

  defineProps(['name']);
</script>

<style lang="scss" scoped></style>
