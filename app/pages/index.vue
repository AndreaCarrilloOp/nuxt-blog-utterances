<script setup lang="ts">
const { data: posts } = await useAsyncData('blog', () =>
  queryCollection('blog').order('date', 'DESC').all()
)
</script>

<template>
  <main class="container">
    <h1>Artículos del blog</h1>
    <p>Lecturas sobre desarrollo web y organización del contenido.</p>

    <ul class="posts">
      <li v-for="post in posts" :key="post.path" class="card">
        <h2><NuxtLink :to="post.path">{{ post.title }}</NuxtLink></h2>
        <p>{{ post.description }}</p>
        <small>{{ post.author }} · {{ String(post.date).slice(0, 10) }}</small>
      </li>
    </ul>
  </main>
</template>
