<template>
  <h2>Prix total HT : {{ totalPriceHT }}</h2>
  <h2>Prix total TTC : {{ totalPriceTTC }}</h2>
</template>

<script lang="ts" setup>
  import { reactive, computed } from 'vue';

  const product = reactive({
    name: 'books',
    quantity: 3,
    priceHT: 10
  });

  const totalPriceHT = computed(() => {
    return product.priceHT * product.quantity;
  });

  const totalPriceTTC = computed(() => {
    return product.priceHT * product.quantity * 1.2;
  });
</script>

<style></style>
