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
    @focus="input.focus = true"
    @blur="input.focus = false"
    @click="input.touched = true"
    v-model="input.value"
    class="input"
  />
</template>

<script lang="ts" setup>
  import { computed, reactive } from 'vue';

  // on viens regrouper nos 3 références
  const input = reactive({
    value: '',
    focus: false,
    touched: false
  });

  // si il y a quelque chsose dans le input alors retourne true
  // on ajoute également si focus est true pour ajouter la classe
  // on viens écouter le click sur le input et on change ensuite la valeur de la variable
  const inputOnGoing = computed(() => input.focus && input.value.length);

  // on déclare la constate pour la gestion d'erreur
  // dans la fonction de rappel on définis les règle qui permette d'ajouter la classe
  // si la valeur saisie est inférieur à 5 alors on applique la bordure rouge
  // on vérifie également que l'on as pas le focus pour déclencher la classe erreur
  const inputError = computed(() => input.touched && input.value.length < 5 && !input.focus);

  //gestion si l'input est valide
  // on vérifie qu'il n'y a pas d'erreur avec !inputError.value
  const inputValid = computed(() => input.touched && !inputError.value && !input.focus);
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
