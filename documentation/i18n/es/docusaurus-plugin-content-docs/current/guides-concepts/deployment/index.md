---
title: "Guía de despliegue | Buenas prácticas en Refine v5"
display_title: "Despliegue"
sidebar_label: "Despliegue"
description: "Despliega aplicaciones Refine v5 sobre Vite, Next.js o Remix con procesos seguros y reproducibles."
---

Como meta-framework, Refine no impone una configuración de despliegue específica por sí sola.

Las aplicaciones de Refine suelen construirse sobre alguno de los siguientes frameworks, así que puedes seguir sus guías oficiales para desplegar tu aplicación:

- [Guía de despliegue de Vite](https://vitejs.dev/guide/static-deploy.html)
- [Guía de despliegue de Next.js](https://nextjs.org/docs/deployment)
- [Guía de despliegue de Remix](https://remix.run/docs/en/main/guides/deployment)

Para simplificar este proceso, mantenemos el repositorio de GitHub [refinedev/Dockerfiles](https://github.com/refinedev/dockerfiles), que contiene Dockerfiles para cada uno de los frameworks anteriores.

Estos Dockerfiles parten de los ejemplos oficiales de cada framework y usan [refinedev/node](https://hub.docker.com/r/refinedev/node) como imagen base, con el usuario `non-root` `refine:nodejs`.

La etapa final ejecuta la aplicación con el usuario `non-root` `refine:nodejs` para mejorar la **seguridad** e incluye solo las dependencias de producción necesarias para reducir el tamaño de la imagen.
