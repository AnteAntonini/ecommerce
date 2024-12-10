<script setup>
import SearchComponent from './SearchComponent.vue'
</script>

<template>
  <header class="header">
    <nav class="nav">
      <div class="logo">
        <img src="../assets/logo.svg" />
      </div>
      <div class="left-nav">
        <ul class="nav-links">
          <li>
            <RouterLink to="/women">Women</RouterLink>
          </li>
          <li>
            <RouterLink to="/Men">Men</RouterLink>
          </li>
        </ul>

        <div class="search"><SearchComponent /></div>
      </div>
      <ul class="nav-links">
        <li>
          <img src="../assets/icons/profile-icon.svg" />
        </li>
        <li>
          <img src="../assets/icons/favorite-icon.svg" />
        </li>
        <li>
          <img src="../assets/icons/shopping-cart-icon.svg" />
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
