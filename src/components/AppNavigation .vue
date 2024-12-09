<script setup></script>

<template>
  <header class="header">
    <nav class="nav">
      <div class="logo">
        <img src="../assets/logo.svg" />
        <span>LOGO MyApp</span>
      </div>
      <ul class="nav-links">
        <li>
          <RouterLink to="/">Home</RouterLink>
        </li>
        <RouterLink to="/about">About</RouterLink>
        <li></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: #f8f9fa;
  padding: 1rem 2rem;
  border-bottom: 1px solid #eaeaea;
}

.nav {
  display: flex;
  align-items: center;
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

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  padding: 0;
  margin: 0;
}

.nav-links a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #007bff;
}
</style>
