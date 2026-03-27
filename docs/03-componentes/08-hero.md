---
title: "Hero"
category: "Componentes"
order: 8
---

# Componente Hero

Bloque visual de encabezado de sección. Soporta imagen de fondo, color sólido, badge, botones CTA, y alineación personalizable.

:::hero{title="Fusiondoc" subtitle="Documentación poderosa y moderna, generada desde archivos Markdown." badge="Componente Hero" cta="Comenzar" ctahref="#uso-basico" cta2="Ver ejemplos" cta2href="#ejemplos"}
:::

## Uso básico

```md
:::hero{title="Mi Título" subtitle="Una descripción breve"}
:::
```

## Con imagen de fondo

```md
:::hero{title="Bienvenido" subtitle="Documentación poderosa" bg="https://mi-sitio.com/imagen.jpg"}
:::
```

## Parámetros disponibles

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `title` | `string` | — | Título principal |
| `subtitle` | `string` | — | Subtítulo o descripción |
| `bg` | `string` | — | URL de imagen de fondo |
| `color` | `string` | — | Color CSS de fondo sólido |
| `height` | `string` | `"300px"` | Altura del hero (px, vh, rem…) |
| `align` | `left` \| `center` \| `right` | `"left"` | Alineación del contenido |
| `badge` | `string` | — | Etiqueta/badge sobre el título |
| `cta` | `string` | — | Texto del botón primario |
| `ctahref` | `string` | `"#"` | URL del botón primario |
| `cta2` | `string` | — | Texto del botón secundario |
| `cta2href` | `string` | `"#"` | URL del botón secundario |

## Ejemplos

### Con imagen de fondo y botones

```md
:::hero{title="Empieza hoy" subtitle="La forma más sencilla de documentar." bg="https://images.unsplash.com/photo-1518770660439-4636190af475?w=1200" badge="Nuevo" cta="Ver guía" ctahref="/01-fundamentos" cta2="GitHub"}
:::
```

:::hero{title="Empieza hoy" subtitle="La forma más sencilla de documentar." bg="https://images.unsplash.com/photo-1518770660439-4636190af475?w=1200" badge="Nuevo" cta="Ver guía" ctahref="/01-fundamentos" cta2="GitHub"}
:::

### Con color sólido y centrado

```md
:::hero{title="Componentes" subtitle="Bloques interactivos para tu documentación." color="#0f172a" align="center" cta="Explorar" badge="v2.0"}
:::
```

:::hero{title="Componentes" subtitle="Bloques interactivos para tu documentación." color="#0f172a" align="center" cta="Explorar" badge="v2.0"}
:::

### Sin imagen (usa el tema actual)

:::hero{title="Tema Automático" subtitle="Si no especificas bg ni color, el Hero usa los colores del tema activo." badge="Adaptable"}
:::
