<template>
  <Blog :fontSize="fontSize" @bigger="fontSize++" />
  <Blog :fontSize="fontSize" @bigger="fontSize++" />
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  import Blog from './components/Blog.vue';

  const fontSize = ref(16);
</script>

<style scoped lang="scss"></style>
