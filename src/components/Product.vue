<template>
  <h3>{{ title }}</h3>
  <p>Disponible au prix de : {{ prix }}</p>
  <p>Ici le boolean est : {{ available }}</p>
</template>

<script setup lang="ts">
  import { computed } from 'vue';

  const props = defineProps<{
    prix: number;
    name: string;
    available: boolean;
  }>();

  const title = computed(() => props.name.toUpperCase());
</script>

<style lang="scss" scoped></style>
