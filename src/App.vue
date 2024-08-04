<template>
  <Product :name="product" />
</template>

<script lang="ts" setup>
  import Product from './components/Product.vue';

  const product = ref('Voiture');
</script>

<style scoped lang="scss"></style>
