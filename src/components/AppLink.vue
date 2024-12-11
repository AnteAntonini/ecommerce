<template>
  <RouterLink :to="src" :aria-label="name">
    <slot />
  </RouterLink>
</template>

<script setup>
defineProps({
  src: String,
  name: String,
})
</script>
