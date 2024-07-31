<template>
  <!-- On vient afficher le nom de l'user dans le h1 -->
  <h1>Bonjour {{ user.name }}</h1>
  <h2>Count : {{ state.count }}</h2>
  <!-- on the flight -->
  <!-- <button @click="state.count++">Add</button> -->
  <!-- en utilisant une fonction -->
  <button @click="addCount">Add</button>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';

  //on rends cette objet reactive en le passant à la fonction reactive()
  const state = reactive({
    // on déclare un objet user directement dans la fonction reactive
    user: {
      name: 'Tintin',
      age: 15
    },
    count: 0
  });

  const { user, count } = state;
  // la fonction viens incrémenter le count
  function addCount() {
    state.count++;
  }

  // au bout de 2s on vient modifier la valeur name de l'objet user
  // on viens rendre de nouveau le template pour afficher la mise à jour
  setTimeout(() => {
    state.user.name = 'Leo';
  }, 2000);
</script>

<style></style>
