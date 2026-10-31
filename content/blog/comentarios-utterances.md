---
title: "Comentarios con Utterances"
description: "Integración de comentarios vinculados a GitHub Issues."
author: "Equipo del blog"
date: 2026-10-16
image: "/images/blog/comentarios-utterances.svg"
tags: ['comentarios', 'github']
---

Utterances es una herramienta que utiliza GitHub Issues para almacenar y mostrar comentarios. El sitio inserta un pequeño widget que se comunica con un repositorio público configurado por quien administra el blog.

La configuración debe señalar el repositorio autorizado y la forma de identificar el hilo. Elegir pathname hace que la ruta de cada artículo corresponda a una conversación independiente.

Como el widget funciona en el navegador, se monta dentro de ClientOnly. También conviene actualizarlo al cambiar de página, para evitar que se muestren comentarios pertenecientes a la entrada anterior.

Una integración correcta debe probarse después de instalar Utterances en el repositorio de GitHub. La prueba final consiste en publicar comentarios en dos entradas y confirmar que se crean y conservan hilos distintos.
