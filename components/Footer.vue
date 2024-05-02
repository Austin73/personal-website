<template>
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-column">
            <h3>About Us</h3>
            <p>This is a personal blog website created using Nuxt 3. Here you can find articles and tutorials on various topics related to web development and programming.</p>
          </div>
          <div class="footer-column">
            <h3>Recent Posts</h3>
            <ul>
              <li v-for="post in recentPosts" :key="post.id">
                <NuxtLink :to="'/blog/' + post.slug">{{ post.title }}</NuxtLink>
              </li>
            </ul>
          </div>
          <div class="footer-column">
            <h3>Follow Us</h3>
            <ul>
              <li><a href="https://twitter.com/yourtwitterhandle" target="_blank" rel="noopener noreferrer">Twitter</a></li>
              <li><a href="https://www.facebook.com/yourfacebookpage" target="_blank" rel="noopener noreferrer">Facebook</a></li>
              <li><a href="https://www.instagram.com/yourinstagramhandle" target="_blank" rel="noopener noreferrer">Instagram</a></li>
              <li><a href="https://www.linkedin.com/company/yourlinkedincompany" target="_blank" rel="noopener noreferrer">LinkedIn</a></li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  import { ref } from 'vue';
 const recentPosts= ref([
          { id: 1, title: 'Introduction to Nuxt 3', slug: 'introduction-to-nuxt-3' },
          { id: 2, title: 'Building a Blog with Nuxt 3', slug: 'building-a-blog-with-nuxt-3' },
          { id: 3, title: 'Deploying a Nuxt 3 App to Vercel', slug: 'deploying-a-nuxt-3-app-to-vercel' },
        ])
  
  </script>
  
  <style scoped>
  .footer {
    background-color: #333;
    color: #fff;
    padding: 2rem 0;
    /* margin-top: 1rem; */
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    z-index: 10;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-between;
  }
  
  .footer-column {
    width: 33.333%;
  }
  
  .footer-column h3 {
    margin-bottom: 1rem;
  }
  
  .footer-column ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .footer-column li {
    margin-bottom: 0.5rem;
  }
  
  .footer-column a {
    color: #fff;
    text-decoration: none;
  }
  </style>