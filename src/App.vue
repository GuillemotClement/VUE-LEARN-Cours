<template>
  <input
    type="text"
    :class="{
      // si l'user saiais quelque chose on ajoute la classe
      // on utilise la notation raccourcie
      inputOnGoing,
      inputError,
      inputValid
    }"
    @focus="focus = true"
    @blur="focus = false"
    @click="touched = true"
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

  // on ajoute une propriété pour savoir si l'user à cliqué au moins une fois sur l'input
  // on initialise à false car au début l'user n'as pas touché
  const touched = ref(false);

  // si il y a quelque chsose dans le input alors retourne true
  // on ajoute également si focus est true pour ajouter la classe
  // on viens écouter le click sur le input et on change ensuite la valeur de la variable
  const inputOnGoing = computed(() => focus.value && input.value.length);

  // on déclare la constate pour la gestion d'erreur
  // dans la fonction de rappel on définis les règle qui permette d'ajouter la classe
  // si la valeur saisie est inférieur à 5 alors on applique la bordure rouge
  // on vérifie également que l'on as pas le focus pour déclencher la classe erreur
  const inputError = computed(() => touched.value && input.value.length < 5 && !focus.value);

  //gestion si l'input est valide
  // on vérifie qu'il n'y a pas d'erreur avec !inputError.value
  const inputValid = computed(() => touched.value && !inputError.value && !focus.value);
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

  .inputError {
    border-color: red;
  }

  .inputValid {
    border-color: green;
  }
</style>
