<template>
  <h3>Voiture</h3>
  <ul>
    <li>Prix : 10 000$</li>
    <li>Roues : 4</li>
    <li>Places : 5</li>
  </ul>
  <button @click="count++">Acheter</button>
  <p>Vous avez acheter {{ count }} voitures</p>
</template>

<script setup lang="ts">
  import { ref } from 'vue';

  const count = ref(0);
</script>

<style lang="scss" scoped></style>
