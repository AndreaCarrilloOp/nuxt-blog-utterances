---
title: "Publicaciones con Nuxt Content"
description: "Colecciones y consultas para páginas Markdown."
author: "Equipo del blog"
date: 2026-10-10
image: "/images/blog/nuxt-content.svg"
tags: ['nuxt', 'contenido']
---

Nuxt Content permite que una entrada se redacte como Markdown y se visualice como una página web. Esta separación facilita actualizar textos sin modificar manualmente la plantilla de cada artículo.

El archivo content.config.ts define la colección y sus campos. Por ejemplo, exigir autor, fecha, imagen y etiquetas ayuda a detectar documentos incompletos durante el desarrollo.

La consulta queryCollection obtiene las publicaciones disponibles para el listado. En la página de detalle, la ruta del navegador sirve para recuperar únicamente la entrada seleccionada.

Una ventaja de este diseño es su reutilización: al agregar un nuevo archivo Markdown válido, el listado y la vista de detalle pueden mostrarlo sin escribir una nueva página Vue.
