<template>
  <input type="number" v-model="product.quantity" />
  <input type="number" v-model="price" />
  <h2>Prix total HT : {{ totalPriceHT }}</h2>
  <h2>Prix total TTC : {{ totalPriceTTC }}</h2>
  <p>{{ product.nbrModification }}</p>
</template>

<script lang="ts" setup>
  import { reactive, computed, watch, ref } from 'vue';

  const product = reactive({
    name: 'books',
    quantity: 3,
    priceHT: 10,
    nbrModification: 0
  });

  const price = ref(0);

  const totalPriceHT = computed(() => {
    return product.priceHT * product.quantity;
  });
  const totalPriceTTC = computed(() => {
    return product.priceHT * product.quantity * 1.2;
  });

  watch(
    // on viens surveiller la propriété + la ref
    //le watch s'execute si la quantity change ou bien le price
    [() => product.quantity, price],
    (newValue, oldValue) => {
      // lors d'une modification de cette propriété on incrémente la valeur
      product.nbrModification++;
    }
  );
</script>

<style></style>
