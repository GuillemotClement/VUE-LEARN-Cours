<template>
  <input type="number" v-model="product.quantity" />
  <h2>Prix total HT : {{ totalPriceHT }}</h2>
  <h2>Prix total TTC : {{ totalPriceTTC }}</h2>
  <p>{{ product.nbrModification }}</p>
</template>

<script lang="ts" setup>
  import { reactive, computed, watch } from 'vue';

  const product = reactive({
    name: 'books',
    quantity: 3,
    priceHT: 10,
    nbrModification: 0
  });

  const totalPriceHT = computed(() => {
    return product.priceHT * product.quantity;
  });
  const totalPriceTTC = computed(() => {
    return product.priceHT * product.quantity * 1.2;
  });

  watch(
    // on viens surveiller la propriété
    () => product.quantity,
    (newValue, oldValue) => {
      // lors d'une modification de cette propriété on incrémente la valeur
      product.nbrModification++;
    }
  );
</script>

<style></style>
