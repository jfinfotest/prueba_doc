---
title: "Introducción a Fusiondoc"
category: "Fundamentos"
order: 1
categoryOrder: 1
author: "midudev"
date: "2026-03-25"
---

# Bienvenido a Fusiondoc JF

Este es el primer archivo de tu nueva documentación generada estáticamente, hosteada en GitHub. 

## ¿Por qué Fusiondoc?
Como puedes ver en el **Frontmatter** de arriba, hemos personalizado nuevas propiedades:
- `title`: El título de la página
- `author`: El autor del post que se muestra debajo del título.
- `date`: La fecha de publicación.
- `draft`: Usado en otras páginas para ocultarlas si no están listas.

### Ventajas de usar Markdown puro
1. No necesitas una base de datos.
2. Todo vive en Git, lo que significa control de versiones gratuito.
3. Se compila súper rápido con Next.js App Router y Tailwind.

## Componentes de UI Automáticos

Al usar React Markdown y Tailwind Typography, todos tus elementos se estilizan sin configuración extra.

### Bloques de Código

Por ejemplo, un bloque de código en TypeScript:

```typescript
function saludar(nombre: string) {
  return `Hola ${nombre}`;
}
```

### Tablas

| Característica | Soporte |
| -------------- | ------- |
| Modo Oscuro    | Sí      |
| Frontmatter    | Sí      |
| Búsqueda       | Próximamente |
