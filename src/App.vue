<template>
  <Blog :fontSize="fontSize" />
  <Blog :fontSize="fontSize" />
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  import Blog from './components/Blog.vue';

  const fontSize = ref(16);
</script>

<style scoped lang="scss"></style>
