---
title: "De Obsidian a la Web: Cómo publicar tu blog automáticamente con Vault CMS y Astro"
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
# De Obsidian a la Web: Cómo publicar tu blog automáticamente con Vault CMS y Astro

Imagina un mundo donde tu blog no requiere lidiar con paneles de administración lentos ni configuraciones técnicas complejas cada vez que quieres compartir una idea. **Este sistema es revolucionario porque te permite escribir en Markdown localmente dentro de Obsidian y publicar tu contenido en la web con un solo clic o atajo de teclado.** Al eliminar la fricción entre la escritura y la publicación, puedes centrarte exclusivamente en crear contenido de calidad mientras la tecnología trabaja para ti en segundo plano.

## ¿Qué hace cada pieza? (El "Dream Team")

Para que esta magia ocurra, necesitamos un equipo de herramientas que trabajen en perfecta sincronía.

### Obsidian

**Es tu entorno de escritura personal y el centro de comando de todo tu conocimiento.** Obsidian no es solo un editor de texto; es donde vive tu "cerebro digital" bajo tu control total. En este flujo, funciona como el lugar donde redactas tus borradores, organizas tus ideas y gestionas tus activos antes de que vean la luz en internet.

### Vault CMS

**Es un conjunto de plugins y configuraciones que transforman tu bóveda de Obsidian en un panel de control de contenido profesional.** No se trata de un software independiente, sino de una optimización de Obsidian mediante plugins clave como **Astro Composer** (que automatiza las propiedades de los archivos y metadatos) y **Bases CMS**, que te ofrece una vista de base de datos tipo grid para gestionar tus posts de forma visual. Además, incluye herramientas de auditoría **SEO** para mejorar el posicionamiento de tus notas antes de publicarlas.

### Astro Modular

**Es el "esqueleto" de tu web que garantiza que tus notas se vean perfectas en el navegador, manteniendo el estilo original de Obsidian.** Astro Modular es un tema diseñado específicamente para usuarios de Obsidian, soportando de forma nativa elementos como los callouts, wikilinks, backlinks y hasta el famoso grafo de notas directamente en la web. Gracias a su **Setup Wizard** integrado, puedes configurar el título, los colores y las fuentes de tu sitio desde Obsidian sin tocar una sola línea de código.

### GitHub

**Es el puente digital que guarda de forma segura y transporta tus notas y el código de tu sitio.** GitHub actúa como un repositorio central donde se sincronizan todos tus cambios. Cada vez que guardas una actualización, este "puente" notifica al servidor que hay contenido nuevo listo para ser procesado.

### Vercel

**Es el motor de alto rendimiento que convierte tus archivos Markdown en una página web rápida y profesional.** Vercel toma la información que llega desde GitHub y, en cuestión de segundos, construye tu sitio utilizando la velocidad de Astro. El resultado es una web extremadamente optimizada para SEO y con tiempos de carga casi instantáneos.

---

## El Flujo de Trabajo (Diagrama Mental)

**El proceso es lineal y sencillo: escribes, sincronizas y visualizas.**

1. **Escribes:** Creas una nueva nota en Obsidian usando **Astro Composer** para generar automáticamente los metadatos necesarios (fecha, etiquetas, slug).
2. **Revisas:** Utilizas el plugin de **SEO** para asegurarte de que los títulos y descripciones sean óptimos para Google.
3. **Publicas:** Presionas un botón (gracias al plugin **Git Sync**) que envía tus cambios a GitHub.
4. **Despliegue Automático:** GitHub activa a Vercel, que reconstruye el sitio con la nueva información.
5. **¡Listo!:** En un par de minutos, tu post está disponible en tu URL para todo el mundo.

---

## Requisitos Previos

Antes de empezar, asegúrate de tener lo siguiente:

- **Obsidian** instalado en tu computadora.
- Una cuenta gratuita en **GitHub** y en **Vercel**.
- **Node.js** (versión 24.13.0 o superior) instalado.
- Un gestor de paquetes como **pnpm** (recomendado) o npm.

---

## Instalación Paso a Paso

### 1. Cómo clonar el repo astro-modular

**Utiliza la terminal para descargar la estructura base de tu nuevo blog de forma automática.** La forma más sencilla es ejecutar el siguiente comando en tu terminal, que descargará el tema y todas sus dependencias:

```
npm create astro-modular my-blog
```

Esto creará una carpeta llamada `my-blog` con todo lo necesario para empezar.

### 2. Cómo integrar Vault CMS en el proyecto

**Transforma la carpeta de contenido de tu web en una bóveda inteligente de Obsidian.** Una vez dentro de la carpeta de tu proyecto, puedes instalar **Vault CMS** ejecutando:

```
npx create-vaultcms
```

El asistente detectará que estás usando Astro y configurará la carpeta `.obsidian` y los archivos necesarios dentro de `src/content` para que puedas abrir esa carpeta directamente en Obsidian como una bóveda.

### 3. Cómo conectar el repositorio a Vercel

**Configura tu plataforma de despliegue una sola vez para que todo funcione en piloto automático.** Dentro de tu proyecto, abre el archivo `src/config.ts` y busca la sección de `deployment.platform`. Cambia el valor a `"vercel"`. Luego, en el panel de Vercel, importa tu repositorio de GitHub y el sistema detectará automáticamente que es un proyecto Astro, encargándose del resto.

> **Pro-tip:** Utiliza el **Setup Wizard** de Astro Modular dentro de Obsidian para validar que todos tus plugins estén correctamente configurados antes de tu primer despliegue.

---

## Estructura de Archivos

**Toda tu creatividad vive dentro de la carpeta `src/content`.** En esta estructura, tus publicaciones suelen organizarse en `src/content/blog`. Una de las grandes ventajas de este sistema es que puedes usar una organización basada en carpetas, donde cada post tiene su propia subcarpeta que contiene tanto el archivo Markdown como todas las imágenes y activos relacionados.

---

## Ventajas y Desventajas

### Ventajas

- **Propiedad total:** Tú eres el dueño de tus archivos Markdown; no dependes de una plataforma cerrada.
- **Velocidad extrema:** Gracias a Astro, tu sitio será increíblemente rápido, lo cual es excelente para la experiencia del usuario y el SEO.
- **Costo $0:** Puedes mantener todo este sistema funcionando gratis usando los niveles gratuitos de GitHub y Vercel.

### Desventajas

- **Curva de aprendizaje:** Al principio, puede ser intimidante usar la terminal o configurar Git.
- **Configuración inicial:** Requiere un poco más de tiempo de preparación que usar una plataforma como Medium o Substack.

---

## Conclusión

Adoptar este flujo de trabajo no es solo una decisión técnica, es un acto de **soberanía digital**. Al escribir localmente y publicar en tu propia infraestructura, recuperas el control sobre tus datos y disfrutas de un minimalismo que te permite concentrarte en lo que realmente importa: tus palabras. ¡Es hora de empezar a construir tu rincón personal en la web!
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