<template>
  <h2>Prix total HT : {{ totalPriceHT() }}</h2>
  <h2>Prix total TTC : {{ totalPriceTTC() }}</h2>
</template>

<script lang="ts" setup>
  import { reactive, ref } from 'vue';

  const product = reactive({
    name: 'books',
    quantity: 3,
    priceHT: 10
  });

  const totalPriceHT = () => {
    return product.priceHT * product.quantity;
  };

  const totalPriceTTC = () => {
    return product.priceHT * product.quantity * 1.2;
  };
</script>

<style></style>
