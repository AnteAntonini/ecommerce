<template>
  <button>
    {{ iconSrc }}
  </button>
</template>

<script setup>
defineProps({
  label: String,
  iconSrc: String,
})
</script>
