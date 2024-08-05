<template>
  <button @click="">+</button>
  <p :style="{ fontSize: props.fontSize + 'px' }">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quas quisquam id molestiae, vitae
    recusandae ut qui alias nobis repellendus officia. Vero labore in quidem temporibus eaque non.
    Praesentium ea corporis dolores dolorum deserunt dolor ex reiciendis repudiandae, aspernatur,
    eaque vero perspiciatis sit ab, nihil nemo a corrupti consequatur molestias soluta.
  </p>
</template>

<script setup lang="ts">
  const props = defineProps<{
    fontSize: number;
  }>();
</script>

<style lang="scss" scoped></style>
