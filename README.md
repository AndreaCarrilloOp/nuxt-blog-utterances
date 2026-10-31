# Bitácora web

[![Nuxt](https://img.shields.io/badge/Nuxt-4-00DC82?logo=nuxt&logoColor=white)](https://nuxt.com/)
[![Nuxt Content](https://img.shields.io/badge/Nuxt_Content-3-00DC82)](https://content.nuxt.com/)
[![Vue](https://img.shields.io/badge/Vue-3-4FC08D?logo=vuedotjs&logoColor=white)](https://vuejs.org/)
[![Utterances](https://img.shields.io/badge/Comentarios-Utterances-24292F?logo=github&logoColor=white)](https://utteranc.es/)
[![Netlify](https://img.shields.io/badge/Deploy-Netlify-00C7B7?logo=netlify&logoColor=white)](https://www.netlify.com/)

Blog desarrollado con **Nuxt y Nuxt Content**, utilizando publicaciones Markdown, rutas dinámicas y comentarios independientes mediante **Utterances y GitHub Issues**.

## Características

- Seis artículos Markdown con título, descripción, autor, fecha, imagen y etiquetas.
- Listado de artículos en la página principal.
- Páginas dinámicas con contenido e imágenes.
- Comentarios independientes por artículo.
- Diseño CSS sencillo y adaptable a distintos dispositivos.

## Ejecución local

Requiere Node.js y npm.

```bash
npm install
npm run dev
```

Abrir `http://localhost:3000` o la dirección indicada en la terminal.

## Comentarios

Utterances utiliza el repositorio público [comentarios_utterances](https://github.com/AndreaCarrilloOp/comentarios_utterances) para almacenar los comentarios como GitHub Issues.

El componente `app/components/Comentarios.vue` utiliza `issue-term="pathname"` para asociar un hilo independiente a cada artículo. Para comentar, es necesario iniciar sesión con GitHub.

## Verificación

1. Abrir dos artículos diferentes.
2. Publicar un comentario en cada uno.
3. Comprobar que cada artículo conserva su propio hilo.
4. Verificar los comentarios en [GitHub Issues](https://github.com/AndreaCarrilloOp/comentarios_utterances/issues).

## Enlaces

- **Sitio web:** [Bitácora web — Netlify](https://blog-utterances.netlify.app/)
- **Código fuente:** [nuxt-blog-utterances](https://github.com/AndreaCarrilloOp/nuxt-blog-utterances)
- **Repositorio de comentarios:** [comentarios_utterances](https://github.com/AndreaCarrilloOp/comentarios_utterances)
