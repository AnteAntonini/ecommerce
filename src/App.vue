<script setup>
import { RouterView } from 'vue-router'
import AppNavigation from './components/AppNavigation .vue'
import AppFooter from './components/AppFooter.vue'
</script>

<template>
  <AppNavigation />
  <main>
    <RouterView />
  </main>
  <AppFooter />
</template>

<style scoped>
main {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow: auto;
}
</style>
