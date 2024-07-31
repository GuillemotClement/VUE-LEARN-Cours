<template>
  <h1 v-on:click="userClick">Hello</h1>
</template>

<script lang="ts" setup>
  function userClick(event: MouseEvent) {
    console.log(event);
  }
</script>

<style></style>
