<template>
  <input type="number" v-model="product.quantity" />
  <input type="number" v-model="price" />
  <h2>Prix total HT : {{ totalPriceHT }}</h2>
  <h2>Prix total TTC : {{ totalPriceTTC }}</h2>
  <p>{{ product.nbrModification }}</p>
</template>

<script lang="ts" setup>
  import { reactive, computed, watch, ref, watchEffect } from 'vue';

  // on vient utiliser une interface pour résoudre le problème de type de la propriété lastModification
  // on viens créer généralement les interfaces dans un fichier externe
  interface Product {
    name: string;
    quantity: number;
    priceHT: number;
    nbrModification: number;
    lastModification?: number | null;
  }

  //on précise le nom de l'interface
  const product = reactive<Product>({
    name: 'books',
    quantity: 3,
    priceHT: 10,
    nbrModification: 0,
    lastModification: null
  });

  const price = ref(0);

  const totalPriceHT = computed(() => {
    return product.priceHT * product.quantity;
  });
  const totalPriceTTC = computed(() => {
    return product.priceHT * product.quantity * 1.2;
  });

  //on pourras utiliser cette variable pour couper le watch
  const unwatch = watch(
    // on viens surveiller la propriété + la ref
    //le watch s'execute si la quantity change ou bien le price
    [() => product.quantity, price],
    (newValue, oldValue) => {
      // lors d'une modification de cette propriété on incrémente la valeur
      product.nbrModification++;
      // on viens couper le watch au premier déclenchement
      unwatch();
    }
  );

  watchEffect(() => {
    //on créer une dépendance
    product.priceHT = price.value;
    // on viens exécuter directement la fonction
    // Date.now() retourne le timestamps du moment ou la méthode est invoqué
    product.lastModification = Date.now();
  });
</script>

<style></style>
