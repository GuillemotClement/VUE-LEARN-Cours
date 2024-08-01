<template>
  <input
    type="text"
    :class="{
      // si l'user saiais quelque chose on ajoute la classe
      inputOnGoing: inputOnGoing
    }"
    @focus="focus = true"
    @blur="focus = false"
    v-model="input"
    class="input"
  />
</template>

<script lang="ts" setup>
  import { computed, ref } from 'vue';

  const input = ref('');

  const focus = ref(false);
  // @focus permet d'écouter l'event focus
  // @blur permet d'écouter si on part du focus

  // si il y a quelque chsose dans le input alors retourne true
  // on ajoute également si focus est true pour ajouter la classe
  const inputOnGoing = computed(() => focus.value && input.value.length);
</script>

<style scoped>
  .input {
    outline: 0;
    border: 2px solid black;
    border-radius: 10px;
  }

  .inputOnGoing {
    border-color: blue;
  }
</style>
