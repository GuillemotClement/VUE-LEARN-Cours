<template>
  <h3>{{ title }}</h3>
  <p>Disponible au prix de : {{ props.product.prix }}</p>
  <p>Ici le boolean est : {{ props.product.available }}</p>
</template>

<script setup lang="ts">
  import type { ProductInterface } from '@/interface/product.interface';
  import { computed } from 'vue';

  const props = defineProps<{
    product: ProductInterface;
  }>();

  const title = computed(() => props.product.name.toUpperCase());
</script>

<style lang="scss" scoped></style>
