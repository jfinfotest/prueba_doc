---
title: "Carrusel"
category: "Componentes"
order: 10
---

# Componente Carrusel

Crea presentaciones deslizables con diapositivas de contenido, imágenes de fondo y transiciones animadas.

::::carousel{height="280px" autoplay="4000"}
:::slide{bg="https://images.unsplash.com/photo-1518770660439-4636190af475?w=1200&q=80"}
## 🚀 Texto en la parte inferior
El texto aparece con overlay sobre la imagen.
:::
:::slide{color="#1a1a2e"}
## 💡 Color sólido
Con fondo oscuro personalizable.
:::
:::slide{bg="https://images.unsplash.com/photo-1461749280684-dccba630e2f6?w=1200&q=80" empty="true"}
:::
::::

**Galería solo imágenes** (sin texto, con `empty="true"`):

::::carousel{height="240px" autoplay="2500" dots="true"}
:::slide{bg="https://picsum.photos/seed/a/1200/600" empty="true"}
:::
:::slide{bg="https://picsum.photos/seed/b/1200/600" empty="true"}
:::
:::slide{bg="https://picsum.photos/seed/c/1200/600" empty="true"}
:::
::::


## Sintaxis

> **Importante:** El carrusel usa **`::::` (4 colons)** como contenedor exterior, y cada slide usa **`:::` (3 colons)**. Esto evita que el cierre de un slide cierre también el carrusel.

```md
::::carousel
:::slide
## Título de la diapositiva
Contenido en markdown normal.
:::
:::slide{bg="https://mi-imagen.com/foto.jpg"}
## Segunda slide con imagen de fondo
:::
::::
```

## Parámetros del Carrusel

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `height` | `string` | `"320px"` | Altura de cada diapositiva |
| `autoplay` | `string` | — | Intervalo en ms (ej: `"3000"`) |
| `loop` | `"true"` \| `"false"` | `"true"` | Volver al inicio al llegar al final |
| `dots` | `"true"` \| `"false"` | `"true"` | Mostrar indicadores de puntos |
| `arrows` | `"true"` \| `"false"` | `"true"` | Mostrar flechas de navegación |
| `title` | `string` | — | Título encima del carrusel |

## Parámetros de cada Slide

| Parámetro | Tipo | Descripción |
|---|---|---|
| `bg` | `string` | URL de imagen de fondo |
| `color` | `string` | Color de fondo sólido (ej: `"#1a1a2e"`) |
| `caption` | `string` | Texto de pie simple sobre la imagen |
| `empty` | `"true"` | Oculta el overlay de texto — slide solo visual |

**Ejemplo de slide solo imagen** (sin texto):

```md
::::carousel{height="260px"}
:::slide{bg="https://picsum.photos/1200/600" empty="true"}
:::
:::slide{bg="https://picsum.photos/seed/x/1200/600" empty="true"}
:::
::::
```


## Ejemplos

### Sin dots, solo flechas

```md
::::carousel{dots="false" height="200px"}
:::slide{color="#0f172a"}
## Slide A
:::
:::slide{color="#1e293b"}
## Slide B
:::
::::
```

::::carousel{dots="false" height="200px"}
:::slide{color="#0f172a"}
## Slide A
Sin puntos de navegación, solo flechas.
:::
:::slide{color="#1e293b"}
## Slide B
Usa las flechas para navegar.
:::
::::

### Galería con autoplay

```md
::::carousel{autoplay="2000" title="Galería de imágenes" height="260px"}
:::slide{bg="https://picsum.photos/seed/a/1200/600"}
## Imagen 1
:::
:::slide{bg="https://picsum.photos/seed/b/1200/600"}
## Imagen 2
:::
:::slide{bg="https://picsum.photos/seed/c/1200/600"}
## Imagen 3
:::
::::
```

::::carousel{autoplay="2000" title="Galería de imágenes" height="260px"}
:::slide{bg="https://picsum.photos/seed/a/1200/600"}
## Imagen 1
Avanza automáticamente cada 2 segundos.
:::
:::slide{bg="https://picsum.photos/seed/b/1200/600"}
## Imagen 2
:::
:::slide{bg="https://picsum.photos/seed/c/1200/600"}
## Imagen 3
:::
::::
