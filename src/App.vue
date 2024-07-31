<template>
  <!-- On vient afficher le nom de l'user dans le h1 -->
  <h1>Bonjour {{ state.user.name }}</h1>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';

  // on déclare un objet user
  const user = {
    name: 'Tintin',
    age: 15
  };

  //on rends cette objet reactive en le passant à la fonction reactive()
  const state = reactive({
    user
  });

  // au bout de 2s on vient modifier la valeur name de l'objet user
  // on viens rendre de nouveau le template pour afficher la mise à jour
  setTimeout(() => {
    state.user.name = 'Leo';
  }, 2000);

</script>

<style></style>
