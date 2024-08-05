<template>
  <Product :name="product" :prix="3200" available />
</template>

<script lang="ts" setup>
  import Product from './components/Product.vue';
  import { ref } from 'vue';

  const product = ref('Bite');
</script>

<style scoped lang="scss"></style>
