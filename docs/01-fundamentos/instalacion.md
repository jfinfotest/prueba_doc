---
title: "Guía de Instalación"
category: "Fundamentos"
order: 2
categoryOrder: 1
---

# Instalación de Fusiondoc

Configurar tu sitio de documentación es increíblemente sencillo. Sigue estos pasos para ponerlo en marcha en menos de 5 minutos.

---

## 🏗️ Requisitos Previos

Asegúrate de tener instalado **Node.js 18+** y un repositorio de GitHub preparado para tus archivos `.md`.

---

## 🔥 Instalación Rápida

Ejecuta los siguientes comandos en tu terminal preferida para clonar y configurar el proyecto base:

:::terminal{title="PowerShell" staticText="Iniciando setup del entorno de documentación..." commands="git clone https://github.com/jfinfotest/prueba_doc\ncd prueba_doc\nnpm install\nnpm run dev"}
:::

---

## 🛠️ Configuración (src/config.ts)

Abre el archivo `src/config.ts` y actualiza los campos con la información de tu repositorio:

```ts
export const GITHUB_CONFIG = {
  owner: 'tu-usuario',
  repo: 'tu-repositorio',
  branch: 'main',
  docsPath: 'docs',
};
```

---

¡Y eso es todo! Ahora puedes empezar a redactar tus guías y docs.
Una vez que el servidor inicie en `http://localhost:3000`, la aplicación leerá los documentos directamente desde este repositorio usando la API de GitHub.
