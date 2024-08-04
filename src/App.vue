<template>
  <Product :name="product" :prix="1500" />
</template>

<script lang="ts" setup>
  import Product from './components/Product.vue';
  import { ref } from 'vue';

  const product = ref('Voiture');
</script>

<style scoped lang="scss"></style>
