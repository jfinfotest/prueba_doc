---
title: "Multimedia: Video, Imagen con Zoom y Audio"
category: "Componentes"
order: 9
---

# Componentes Multimedia

Fusiondoc incluye tres componentes para enriquecer tu documentación con contenido multimedia interactivo.

---

## Video (`::video`)

Embebe videos de YouTube, Vimeo o archivos `.mp4` directamente en tu documentación.

```md
::video{src="https://www.youtube.com/watch?v=dQw4w9WgXcQ" title="Mi Video"}
```

::video{src="https://www.youtube.com/watch?v=dQw4w9WgXcQ" title="Ejemplo de video embebido"}

### Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `src` | `string` | — | URL de YouTube, Vimeo o `.mp4` |
| `title` | `string` | — | Caption debajo del video |
| `aspect` | `16/9` \| `4/3` \| `1/1` \| `21/9` | `16/9` | Relación de aspecto |
| `autoplay` | `"true"` | — | Autoplay (solo videos directos) |
| `muted` | `"true"` | — | Silenciar al cargar |
| `loop` | `"true"` | — | Repetir en bucle |

```md
# Video con relación 4:3
::video{src="https://vimeo.com/123456789" aspect="4/3"}

# MP4 directo con autoplay
::video{src="/videos/demo.mp4" autoplay="true" muted="true" loop="true"}
```

---

## Imagen con Zoom (`::zoomimage`)

Muestra una imagen que se puede ampliar haciendo clic, abriendo un lightbox.

```md
::zoomimage{src="https://picsum.photos/1200/600" alt="Descripción" caption="Pie de foto"}
```

::zoomimage{src="https://picsum.photos/1200/600" alt="Imagen de ejemplo" caption="Haz clic para ampliar"}

### Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `src` | `string` | — | URL de la imagen |
| `alt` | `string` | `""` | Texto alternativo |
| `caption` | `string` | — | Pie de foto |
| `width` | `string` | `"100%"` | Ancho de la imagen (ej: `"50%"`, `"400px"`) |
| `align` | `left` \| `center` \| `right` | `center` | Alineación |

```md
::zoomimage{src="/img/arquitectura.png" caption="Diagrama de arquitectura" width="80%" align="center"}
```

---

## Audio (`::audio`)

Reproductor de audio personalizado con barra de progreso y control de volumen.

```md
::audio{src="https://samplelib.com/lib/preview/mp3/sample-3s.mp3" title="Episodio 1" artist="Mi Podcast"}
```

**Ejemplo en vivo:**

::audio{src="https://www.w3schools.com/html/horse.mp3" title="Ejemplo de audio" artist="W3Schools Sample" }

### Parámetros

| Parámetro | Tipo | Descripción |
|---|---|---|
| `src` | `string` | URL del archivo de audio (mp3, ogg, wav…) |
| `title` | `string` | Nombre del audio |
| `artist` | `string` | Artista o fuente |
| `cover` | `string` | URL de imagen de portada |

```md
::audio{src="/audio/intro.mp3" title="Introducción al Curso" artist="Fusiondoc" cover="/img/cover.png"}
```
