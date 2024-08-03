<template>
  <ul>
    <li v-for="(fruit, index) of fruits">Name: {{ fruit }} à l'index {{ index }}</li>
  </ul>
  <ul>
    <li v-for="{ name, grades } of users">
      {{ name }} :<span v-for="grade in grades">{{ grade }}, </span>
    </li>
  </ul>
</template>

<script lang="ts" setup>
  import { reactive } from 'vue';
  const fruits = reactive(['Fraises', 'Banane', 'Orange']);
  const users = reactive([
    { name: 'Jean', grades: [12, 13, 15] },
    { name: 'Emma', grades: [12, 13, 15] },
    { name: 'Eric', grades: [12, 13, 15] },
    { name: 'Eva', grades: [12, 13, 15] }
  ]);
</script>

<style scoped lang="scss"></style>
