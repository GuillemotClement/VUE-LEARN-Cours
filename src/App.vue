<template>
  <h2>Count : {{ count }}</h2>
  <button @click="addCount">Add</button>
</template>

<script lang="ts" setup>
  //on importe la fonction ref() 
  import { ref } from 'vue';

  //on délcare une nouvelle variable et on rend reactif la valeur avec ref()
  const count = ref(0);

  // la fonction viens incrémenter le count
  function addCount() {
    count.value++;
  }
</script>

<style></style>
