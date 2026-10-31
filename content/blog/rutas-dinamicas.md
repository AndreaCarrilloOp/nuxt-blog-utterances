---
title: "Rutas dinámicas del blog"
description: "Una sola plantilla para múltiples artículos."
author: "Equipo del blog"
date: 2026-10-13
image: "/images/blog/rutas-dinamicas.svg"
tags: ['nuxt', 'rutas']
---

En un blog, cada publicación necesita una URL propia. Crear un archivo Vue diferente para cada artículo dificultaría mantener un diseño consistente conforme aumenta el número de entradas.

La ruta dinámica [...slug].vue recibe las direcciones dentro de la sección del blog. Luego usa el path completo para buscar el documento correcto dentro de la colección.

Esa misma dirección funciona como identificador para los comentarios. Utterances asocia cada path con un Issue diferente y evita mezclar conversaciones de publicaciones distintas.

Para comprobarlo, basta abrir dos artículos, dejar un comentario de prueba en uno y navegar al otro. Cada página debe mantener su propio hilo cuando se regresa a ella.
