<template>
  <!-- on lui passe la référence -->
  <input type="text" v-model="text">
</template>

<script lang="ts" setup> 
import { ref } from 'vue';

// création de la référence initialiser avec une chaîne vide.
const text = ref('');
 
</script>

<style></style>
