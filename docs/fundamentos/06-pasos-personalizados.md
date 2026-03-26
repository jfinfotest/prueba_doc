---
title: Pasos Personalizados
description: Aprende a usar el componente de pasos para tus guías.
---

# Guía Paso a Paso

Aquí tienes un ejemplo de cómo usar el componente `steps` con componentes anidados.

:::steps
:::step{title="Primer Paso: Instalación"}
Lo primero que debes hacer es instalar las dependencias necesarias:

:::terminal{shell="bash" commands="npm install fusiondoc-utils\nnpm install framer-motion"}
:::
:::

:::step{title="Segundo Paso: Configuración"}
Configura tu archivo `fusion.config.js`:

```javascript
module.exports = {
  theme: 'dark',
  plugins: ['steps', 'terminal']
}
```
:::

:::step{title="Tercer Paso: ¡Listo!"}
Ya puedes empezar a usar los componentes en tus archivos Markdown.
:::
:::
