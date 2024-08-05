<template>
  <h3>{{ title }}</h3>
  <p>Disponible au prix de : {{ prix }}</p>
</template>

<script setup lang="ts">
  import { computed } from 'vue';

  const props = defineProps({
    name: {
      type: String,
      required: true,
      default: 'Maison',
      validator(value: string): boolean {
        if (value.length < 10) {
          return false;
        } else {
          return true;
        }
      }
    },
    prix: {
      type: Number,
      required: true,
      default: 0
    }
  });

  const title = computed(() => props.name.toUpperCase());
</script>

<style lang="scss" scoped></style>
