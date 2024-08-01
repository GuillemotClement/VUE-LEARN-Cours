<template>
  <!-- on lui passe la référence -->
  <input type="text" v-model="text" />
  <!-- on affichage la valeur saisis par l'user -->
  <h1>{{ text }}</h1>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';

  // création de la référence initialiser avec une chaîne vide.
  const text = ref('');
</script>

<style></style>
