---
title: "Map, CodePen, Kbd y Badge"
category: "Componentes"
order: 14
---

# Map, CodePen, Kbd y Badge

---

## Map (`::map`)

Incrusta un mapa de Google Maps u OpenStreetMap directamente en la documentación.

```md
::map{src="URL_DEL_EMBED" height="350px" title="Medellín, Colombia"}
```

> **Cómo obtener la URL de Google Maps:** Busca el lugar → Compartir → Insertar mapa → Copia la URL del `src` del `<iframe>`.

::map{src="https://www.openstreetmap.org/export/embed.html?bbox=-75.6298%2C6.1987%2C-75.5298%2C6.2987&layer=mapnik" height="300px" title="Medellín"}

### Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `src` | `string` | — | URL del embed de Google Maps u OpenStreetMap |
| `height` | `string` | `"400px"` | Altura del mapa |
| `title` | `string` | `"Mapa"` | Título accesible del iframe |
| `rounded` | `"true"` \| `"false"` | `"true"` | Bordes redondeados |

---

## CodePen (`::codepen`)

Embebe demos de CodePen con barra de navegación personalizada.

```md
::codepen{id="YzBxBPe" user="alvaromontoro" title="CSS Button" theme="dark" tab="result" height="400px"}
```

::codepen{id="rNXEpbK" user="jhon-valencia-the-encoder" title="Media Queries CSS" theme="dark" tab="result" height="380px"}

### Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `id` | `string` | — | ID del pen en CodePen |
| `user` | `string` | `"anon"` | Username de CodePen |
| `height` | `string` | `"400px"` | Altura del embed |
| `theme` | `"dark"` \| `"light"` \| `"default"` | `"dark"` | Tema del editor |
| `tab` | `string` | `"result"` | Pestaña visible: `result`, `html,css,js`, etc. |
| `title` | `string` | `"CodePen Demo"` | Texto en la barra superior |

---

## Kbd (`:kbd`)

Renderiza atajos de teclado como teclas físicas. Es un **directivo de texto** (colon simple `:`) para usar **inline** dentro de párrafos.

```md
Presiona :kbd{keys="Ctrl+K"} para abrir la búsqueda.
Abre el terminal con :kbd{keys="Ctrl+Shift+P"}.
En Mac usa :kbd{keys="Cmd+K" os="mac"}.
```

Presiona :kbd{keys="Ctrl+K"} para abrir la búsqueda.

Abre el terminal con :kbd{keys="Ctrl+Shift+P"}.

En Mac usa :kbd{keys="Cmd+K" os="mac"}.

Navega con :kbd{keys="Up"} :kbd{keys="Down"} :kbd{keys="Enter"}.

> **Nota:** Usa `:kbd{...}` con **un colon** — es un elemento inline. `::kbd` (doble colon) es un bloque y no funcionará dentro de texto.

### Parámetros

| Parámetro | Tipo | Descripción |
|---|---|---|
| `keys` | `string` | Combinación separada por `+` (ej: `"Ctrl+Shift+P"`) |
| `os` | `"mac"` | Convierte: `Ctrl→⌘`, `Alt→⌥`, `Shift→⇧` |

### Teclas reconocidas

`Ctrl` `Shift` `Alt` `Enter` `Tab` `Esc` `Backspace` `Delete` `Space` `Up` `Down` `Left` `Right`

---

## Badge (`:badge`)

Etiqueta de estado inline para versiones, categorías y estados. También es un **directivo de texto** (`:` simple).

```md
Disponible desde la versión :badge{text="v2.0" type="success"} del sistema.
Estado: :badge{text="Estable" type="default" dot="true"}
Requiere :badge{text="Node 18+" type="warning"} o superior.
```

Disponible desde la versión :badge{text="v2.0" type="success"} del sistema.

Estado: :badge{text="Estable" type="default" dot="true"}

Requiere :badge{text="Node 18+" type="warning"} o superior.

:badge{text="Nuevo" type="info" icon="✨"} :badge{text="Deprecado" type="danger"} :badge{text="Beta" type="outline"} :badge{text="Activo" type="success" dot="true"}

> **Nota:** Usa `:badge{...}` con **un colon** para uso inline. Doble colon `::badge` no funcionará dentro de párrafos de texto.

### Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `text` | `string` | — | Texto del badge |
| `type` | `default` \| `success` \| `warning` \| `danger` \| `info` \| `outline` | `default` | Color del badge |
| `dot` | `"true"` | — | Muestra un punto de estado |
| `icon` | `string` | — | Emoji antes del texto |
