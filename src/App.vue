<template>
  <h1 v-on:click="userClick">Hello</h1>
  <input type="text" @input="userInput" />
</template>

<script lang="ts" setup>
  function userClick(event: MouseEvent) {
    console.log(event);
  }

  function userInput(event: Event) {
    // on viens préciser qu'on utilise un élément input
    //cela améliorer l'autocomplétion
    const target = event.target as HTMLInputElement;
    console.log(target.value);
  }
</script>

<style></style>
