<template>
  <!-- <h1 v-bind:class="h1title">Bonjour</h1> -->
  <!-- <h1 :class="h1title">Bonjour</h1> -->
  <!-- <h1 :[key]="h1title">Bonjour</h1> -->
  <h1 v-bind="obj">Bonjour</h1>
</template>
<script lang="ts" setup>
  const h1title = 'monTitre';
  const key = 'class';
  const h1id = 'monSuperTitle';
  const obj = {
    class: h1title,
    id: h1id
  };
</script>
<style></style>
