<template>
  <div v-memo="[title]">
    <h1>{{ title }}</h1>
    <p></p>
    <p></p>
  </div>
</template>

<script lang="ts" setup>
  import { reactive, ref } from 'vue';

  const title = ref('Ma super app');
</script>

<style scoped lang="scss"></style>
