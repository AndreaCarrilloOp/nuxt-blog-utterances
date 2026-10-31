<script setup lang="ts">
const route = useRoute()
const { data: post } = await useAsyncData(() => route.path, () =>
  queryCollection('blog').path(route.path).first()
)

if (!post.value) {
  throw createError({ statusCode: 404, statusMessage: 'Artículo no encontrado' })
}

useSeoMeta({ title: post.value.title, description: post.value.description })
</script>

<template>
  <main v-if="post" class="container article-page">
    <NuxtLink to="/">← Volver a los artículos</NuxtLink>
    <article>
      <h1>{{ post.title }}</h1>
      <p class="meta">{{ post.author }} · {{ String(post.date).slice(0, 10) }}</p>
      <img :src="post.image" :alt="post.title" class="cover" />
      <p class="tags">{{ post.tags.join(' · ') }}</p>
      <ContentRenderer :value="post" class="article-body" />
    </article>
    <section class="comments">
      <h2>Comentarios</h2>
      <ClientOnly><Comentarios :key="route.path" /></ClientOnly>
    </section>
  </main>
</template>
