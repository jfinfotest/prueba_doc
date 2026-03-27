---
title: "Estructura y Organización"
order: 1
---

# Estructura y Organización

Fusiondoc utiliza tu sistema de carpetas y el **Frontmatter** de tus archivos para construir la navegación del sitio.

## 1. Tópicos (Barra Superior)

Los tópicos se definen por las carpetas en el primer nivel del directorio `docs/`.

### Cómo controlar el orden de los Tópicos:
- **Prefijos Numéricos**: Si una carpeta se llama `01-fundamentos`, aparecerá en la primera posición pero se mostrará como "Fundamentos" en la interfaz.
- **topicOrder**: También puedes añadirlo en el Frontmatter de cualquier archivo:
  ```markdown
  ---
  topicOrder: 1
  ---
  ```

## 2. Categorías (Sidebar)

Las categorías se definen por las carpetas en el segundo nivel o mediante el campo `category` en el Frontmatter.

### Cómo controlar el orden de las Categorías:
- **Prefijos Numéricos**: Al igual que los tópicos, las subcarpetas con número (ej. `01-intro`) definen el orden.
- **categoryOrder**: Field opcional en el Frontmatter.

## 3. Páginas Individuales

El orden de las páginas dentro de una categoría se controla con el campo `order`:

```markdown
---
title: "Mi Página"
order: 1
---
```
*(Nota: Las páginas con `order: 0` o con nombre `index.md` se consideran páginas principales del tópico)*
