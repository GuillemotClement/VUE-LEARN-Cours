<template></template>

<script lang="ts" setup>
  //on importe la fonction ref()
  import { ref } from 'vue';
  // permet d'importer des types
  import type { Ref } from 'vue';

  const count = ref(0);


  // cette fonction récupère une référence en paramètre
  function getRef(num: Ref<number>) {
    num.value++
  }

  getRef(count);
</script>

<style></style>
