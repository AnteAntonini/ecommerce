<script setup></script>

<template>
  <footer class="footer">
    <div class="footer-links"></div>
    <div class="legal-bar">
      <span>@ 2024</span>
      <ul class="link-container">
        <li class="link">Privacy & Cookies</li>
        <span class="separator">|</span>
        <li class="link">Accessability</li>
      </ul>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #eeeeee;
  color: black;
}

.footer-links {
  height: 120px;
  padding: 1rem 2rem;
}

.legal-bar {
  height: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
  background-color: #dddddd;
  font-size: 0.75rem;
}

.link-container {
  display: flex;
}

.link {
  cursor: pointer;
  list-style: none;

  &:hover {
    color: #007aff;
  }
}

.separator {
  padding: 0 0.75rem;
}
</style>
