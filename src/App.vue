<template>
  <!-- on affiche la liste que si on as récupérer les éléments -->
  <h1>Profil</h1>
  <!-- avec le v-if, on affiche les éléments une fois récupéré -->
  <ul v-if="state.user">
    <!-- on viens protéger avec le ? -->
    <li>Name : {{ state.user?.name }}</li>
    <li>Age : {{ state.user?.age }}</li>
  </ul>
  <h2 v-else>Chargement des données en cours ...</h2>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';

  const state = reactive<any>({});

  setTimeout(() => {
    state.user = {
      name: 'Jean',
      age: 17
    };
  }, 3000);
</script>

<style scoped lang="scss"></style>
