<script setup>
import AppLink from './AppLink.vue'
import SearchComponent from './SearchComponent.vue'
import { filename } from 'pathe/utils'

const leftNavLinks = [
  {
    name: 'women',
    title: 'Women',
  },
  {
    name: 'men',
    title: 'Men',
  },
]

const rightNavLinks = [
  {
    name: 'profile',
    title: 'Profile',
    icon: 'profile-icon',
  },
  {
    name: 'favorite',
    title: 'Favorite',
    icon: 'favorite-icon',
  },
  {
    name: 'shopping-cart',
    title: 'Shopping cart',
    icon: 'shopping-cart-icon',
  },
]

const glob = import.meta.glob('@/assets/icons/*.svg', { eager: true })

const icons = Object.fromEntries(
  Object.entries(glob).map(([key, value]) => [filename(key), value.default]),
)
</script>

<template>
  <header class="header">
    <nav class="nav">
      <div class="logo">
        <AppLink src="/women" name="women">
          <img src="../assets/logo.svg" />
        </AppLink>
      </div>
      <div class="left-nav">
        <ul class="nav-links">
          <li v-for="link in leftNavLinks" :key="link.name">
            <AppLink :src="link.name" :aria-label="link.title">
              <span>{{ link.title }}</span>
            </AppLink>
          </li>
        </ul>
        <div class="search"><SearchComponent /></div>
      </div>
      <ul class="nav-links">
        <li v-for="link in rightNavLinks" :key="link.name">
          <AppLink :src="link.name" :aria-label="link.title">
            <img :src="icons[link.icon]" :alt="link.name" />
          </AppLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: #2d2d2d;
  padding: 1rem 2rem;
  border-bottom: 1px solid #2d2d2d;
}

.nav {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: nowrap;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.logo img {
  height: 40px;
  width: 40px;
}

.left-nav {
  display: flex;
  width: 100%;
}

.nav-links {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 1.5rem;
  padding: 0;
  margin: 0;
  cursor: pointer;
}

.search {
  width: 100%;
  padding: 0 1rem;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #007bff;
}
</style>
