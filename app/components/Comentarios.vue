<script setup lang="ts">
const contenedor = ref<HTMLElement | null>(null)

onMounted(() => {
  const script = document.createElement('script')
  script.src = 'https://utteranc.es/client.js'
  script.async = true
  script.crossOrigin = 'anonymous'
  script.setAttribute('repo', 'AndreaCarrilloOp/comentarios_utterances')
  script.setAttribute('issue-term', 'pathname')
  script.setAttribute('theme', 'github-light')
  contenedor.value?.appendChild(script)
})
</script>

<template><div ref="contenedor" /></template>
