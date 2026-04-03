---
title: TEST 06
date: 2026-04-01
description: Print(Blog Alive)
tags:
  - tutorial
  - reference
  - blog
image: "[[attachments/mountains.png]]"
imageAlt: Mountains and water.
imageOG: false
hideCoverImage: false
hideTOC: false
targetKeyword:
draft: false
---

# Test 06

Testing...

# TEST 06

6. vercel crear cuenta, no se puede vincular a el email, si se puede vincular a github
7. cambiar theme
	1. ir a src/config.ts
	2.  // [CONFIG:THEME]
	3. theme: "oxygen" cambiar a "minimal"

```ts
export const siteConfig: SiteConfig = {

  // Site Information

  // [CONFIG:SITE_URL]

  site: "https://astro-modular.netlify.app",

  // [CONFIG:SITE_TITLE]

  title: "Astro Modular", // cambiar a Martin
```



---

Un **CMS** (Content Management System o Sistema de Gestión de Contenidos) ==es una aplicación de software que permite crear, administrar, modificar y publicar contenido digital en un sitio web sin necesidad de tener conocimientos avanzados de programación==. Facilita la gestión de páginas, imágenes y texto mediante una interfaz gráfica amigable.

**Aspectos clave de un CMS:**

- **Gestión sin código:** Permite a los usuarios crear sitios web y actualizar contenido sin saber HTML o CSS.
- **Colaboración:** Múltiples usuarios pueden trabajar simultáneamente con diferentes roles (autores, editores, administradores).
- **Diseño personalizado:**
    
     Se pueden utilizar plantillas y temas preconstruidos para definir la apariencia del sitio.
    

- **Funcionalidades extendidas:** Mediante plugins o extensiones, se pueden añadir funciones como formularios de contacto, tiendas online (e-commerce) o SEO. !

**Ejemplos Populares:**

- **WordPress:** El más utilizado a nivel mundial para blogs y sitios web.
- **Magento:** Enfocado en tiendas electrónicas (e-commerce).
- **Drupal** y **Joomla:** Plataformas robustas para sitios complejos. 

**Tipos de CMS:**

1. **CMS Tradicional (Acoplado):** La gestión de contenido y la visualización final están unidas.
2. **Headless CMS (Desacoplado):** El contenido se gestiona por separado y se distribuye a través de una API a cualquier dispositivo. 

En resumen, un CMS es una herramienta esencial para gestionar la presencia web de manera rápida, rentable y organizada, eliminando la necesidad de un equipo de desarrollo constante.




---



Astro es un ==framework web moderno de código abierto, diseñado para crear sitios web rápidos, centrados en el contenido (blogs, portafolios, landing pages) utilizando JavaScript, HTML y CSS==. Destaca por su arquitectura basada en componentes y "arquitectura de islas" (_Island Architecture_), que envía HTML puro al navegador y carga JavaScript solo cuando es necesario, optimizando el SEO y el rendimiento. 

**Ejemplos de Uso y Características de Astro Programación:**

- **Generación de Sitios Estáticos (SSG):** Ideal para sitios rápidos y seguros.
- **Desarrollo Basado en Componentes:** Uso de archivos `.astro` (similares a JSX) para estructurar la interfaz.
- **UI Agnostic:** Permite importar y usar componentes de otros frameworks como React, Vue, Svelte, Preact o Solid.
- **Integración con Markdown/MDX:** Perfecto para documentación o blogs.
- **Soporte de tecnologías:** Compatible con TypeScript, Tailwind CSS y componentes web.
- **Integración con Headless CMS:** Facilita la conexión con gestores de contenido como Sanity o WordPress. 

**Sinónimos y Términos Relacionados:**

- Generador de sitios estáticos (Static Site Generator).
- Framework frontend.
- Astro JS.
- Herramienta de desarrollo web. 

Astro es elogiado por su simplicidad y alta velocidad de carga, convirtiéndose en una alternativa popular para sitios web que no requieren una aplicación web de una sola página (SPA) compleja.