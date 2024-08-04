<template>
  <h3>{{ title }}</h3>
</template>

<script setup lang="ts">
  import { computed } from 'vue';

  const props = defineProps(['name']);

  const title = computed(() => props.name.toUpperCase());
</script>

<style lang="scss" scoped></style>
