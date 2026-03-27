---
title: "Accordion, CardGrid y FileTree"
category: "Componentes"
order: 13
---

# Accordion, CardGrid y FileTree

---

## Accordion (`:::accordion`)

Preguntas y respuestas colapsables. Cada ítem se abre y cierra con clic.

```md
::::accordion{title="Preguntas frecuentes"}
:::accordionitem{title="¿Qué es Fusiondoc?" icon="❓"}
Es un sistema de documentación basado en Next.js con soporte MDX.
:::
:::accordionitem{title="¿Puedo usar temas?" icon="🎨" open="true"}
Sí, incluye temas: Default, Valorant y Spotify.
:::
::::
```

::::accordion{title="Preguntas frecuentes"}
:::accordionitem{title="¿Qué es Fusiondoc?" icon="❓"}
Es un sistema de documentación basado en **Next.js** con soporte MDX y componentes personalizados.
:::
:::accordionitem{title="¿Puedo usar temas?" icon="🎨" open="true"}
Sí, incluye 3 temas: `Default`, `Valorant` y `Spotify`. Cambia en tiempo real sin recargar la página.
:::
:::accordionitem{title="¿Cómo agrego una nueva página?" icon="📄"}
Crea un archivo `.md` en la carpeta de tu tópico con el prefijo numérico correcto: `03-mi-pagina.md`.
:::
:::accordionitem{title="¿Soporta búsqueda?" icon="🔍"}
Actualmente no, pero la estructura está preparada para integrar [Pagefind](https://pagefind.app) o Algolia.
:::
::::

### Parámetros de `:::accordion`

| Parámetro | Descripción |
|---|---|
| `title` | Título en el encabezado del bloque |

### Parámetros de `:::accordionitem`

| Parámetro | Tipo | Descripción |
|---|---|---|
| `title` | `string` | Texto del ítem |
| `icon` | `string` | Emoji/icono al inicio |
| `open` | `"true"` | Abierto por defecto |

---

## CardGrid (`:::cardgrid` + `:::card`)

Grid responsivo de tarjetas con icono, badge y enlace opcional.

```md
::::cardgrid{cols="3"}
:::card{title="Componentes" icon="🧩" href="/03-componentes"}
Más de 15 componentes MDX listos para usar.
:::
:::card{title="Temas" icon="🎨" badge="3 incluidos" badgetype="success"}
Sistema de temas con variables CSS globales.
:::
:::card{title="Tutorial" icon="📚" badge="Nuevo" badgetype="info"}
Guía paso a paso desde cero.
:::
::::
```

::::cardgrid{cols="3"}
:::card{title="Componentes" icon="🧩" href="/03-componentes"}
Más de 15 componentes MDX listos para usar en tu documentación.
:::
:::card{title="Temas" icon="🎨" badge="3 incluidos" badgetype="success"}
Sistema de temas modulares con variables CSS globales.
:::
:::card{title="Tutorial" icon="📚" badge="Nuevo" badgetype="info"}
Guía paso a paso para crear tu primera documentación.
:::
:::card{title="API Reference" icon="⚙️" badge="Estable" badgetype="default"}
Tabla de API con tipos, valores por defecto y requeridos.
:::
:::card{title="Deploy" icon="🚀" badge="CI/CD" badgetype="warning"}
Configuración para Vercel, Netlify y GitHub Pages.
:::
:::card{title="GitHub" icon="💻" href="https://github.com"}
Código fuente del proyecto y guía de contribución.
:::
::::

### Parámetros de `:::cardgrid`

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `cols` | `"1"` \| `"2"` \| `"3"` \| `"4"` | `"3"` | Columnas del grid |

### Parámetros de `:::card`

| Parámetro | Tipo | Descripción |
|---|---|---|
| `title` | `string` | Título de la tarjeta |
| `icon` | `string` | Emoji |
| `href` | `string` | URL de enlace (hace la tarjeta clicable) |
| `badge` | `string` | Texto del badge |
| `badgetype` | `default` \| `success` \| `warning` \| `danger` \| `info` | Color del badge |

---

## FileTree (`:::filetree`)

Visualización de árbol de carpetas y archivos con íconos automáticos por extensión.

```md
:::filetree{title="Estructura del repositorio"}
src/
  app/
    layout.tsx
    page.tsx
    globals.css
  components/
    mdx/
      Hero.tsx
      Alert.tsx
    MarkdownRenderer.tsx
  lib/
    github.ts
docs/
  01-fundamentos/
    index.md
  03-componentes/
    01-accordion.md
:::
```

:::filetree{title="Estructura del repositorio"}
src/
  app/
    layout.tsx
    page.tsx
    globals.css
  components/
    mdx/
      Hero.tsx
      Alert.tsx
    MarkdownRenderer.tsx
  lib/
    github.ts
docs/
  01-fundamentos/
    index.md
  03-componentes/
    01-accordion.md
:::

> **Nota:** Indenta con 2 espacios por nivel. Las carpetas terminar en `/`.

### Parámetros de `:::filetree`

| Parámetro | Tipo | Descripción |
|---|---|---|
| `title` | `string` | Título del encabezado |

### Íconos automáticos por extensión

| Extensión | Ícono |
|---|---|
| `.tsx` `.ts` | ⚛ / 🔷 |
| `.js` `.jsx` | 🟡 / ⚛ |
| `.css` | 🎨 |
| `.json` | 📋 |
| `.md` `.mdx` | 📝 |
| `.png` `.jpg` `.svg` | 🖼 |
| `.env` | 🔑 |
| `.gitignore` | 🚫 |
