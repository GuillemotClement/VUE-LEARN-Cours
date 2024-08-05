<template>
  <Product :product="product" />
</template>

<script lang="ts" setup>
  import Product from './components/Product.vue';
  import { ref, reactive } from 'vue';
  import type { ProductInterface } from './interface/product.interface';

  const product = reactive<ProductInterface>({
    available: true,
    prix: 1500,
    name: 'Moto'
  });
</script>

<style scoped lang="scss"></style>
