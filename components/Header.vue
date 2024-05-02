
<template>
  <header class="header">
    <div class="container">
      <nav>
        <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/blog">Blog</NuxtLink></li>
          <li><NuxtLink to="/blog">Blog</NuxtLink></li>
          <li><NuxtLink to="/blog">Blog</NuxtLink></li>
          <!-- Add more navigation links as needed -->
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup>
// No script needed for this example
</script>

<style scoped>
.header {
  background-color: #333;
  color: #fff;
  padding: 1rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: right;
}

nav li {
  margin-right: 20px;
}

nav a {
  color: #fff;
  text-decoration: none;
}
</style>