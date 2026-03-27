---
title: "ApiTable, Stat y Progress"
category: "Componentes"
order: 15
---

# ApiTable, Stat y Progress

---

## ApiTable (`:::apitable` + `:::apirow`)

Tabla de referencia de API con columnas tipadas, requerimiento y valores por defecto.

```md
::::apitable{title="Parámetros del componente Hero"}
:::apirow{name="title" type="string" required="true"}
Título principal del hero. Acepta texto plano con saltos de línea.
:::
:::apirow{name="subtitle" type="string"}
Texto secundario bajo el título.
:::
:::apirow{name="bg" type="string" default="none"}
URL de imagen de fondo. Acepta cualquier imagen pública.
:::
:::apirow{name="height" type="string" default="\"420px\""}
Altura del componente hero.
:::
::::
```

::::apitable{title="Parámetros del componente Hero"}
:::apirow{name="title" type="string" required="true"}
Título principal del hero. Acepta texto plano.
:::
:::apirow{name="subtitle" type="string"}
Texto secundario bajo el título.
:::
:::apirow{name="bg" type="string" default="none"}
URL de imagen de fondo. Acepta cualquier URL pública.
:::
:::apirow{name="height" type="string" default="420px"}
Altura del componente.
:::
:::apirow{name="align" type="left|center|right" default="center"}
Alineación del contenido del hero.
:::
:::apirow{name="cta" type="string"}
Texto e URL del botón principal en formato `Texto|/url`.
:::
::::

### Parámetros de `:::apitable`

| Parámetro | Descripción |
|---|---|
| `title` | Título del encabezado de la tabla |

### Parámetros de `:::apirow`

| Parámetro | Tipo | Descripción |
|---|---|---|
| `name` | `string` | Nombre del parámetro |
| `type` | `string` | Tipo TypeScript del parámetro |
| `required` | `"true"` | Marca el campo como requerido |
| `default` | `string` | Valor por defecto |

---

## Stat (`::stat` + `:::statgroup`)

Métricas tipo dashboard con valor grande, etiqueta y tendencia.

```md
:::statgroup{cols="4"}
::stat{value="14" label="Componentes" icon="🧩" color="primary"}
::stat{value="99.9%" label="Uptime" icon="⚡" color="success" trend="+0.1%" trendtype="up"}
::stat{value="3" label="Temas" icon="🎨" color="info"}
::stat{value="12ms" label="TTI" icon="🚀" color="warning" trend="-8ms" trendtype="up"}
:::
```

:::statgroup{cols="4"}
::stat{value="14" label="Componentes MDX" icon="🧩" color="primary"}
::stat{value="99.9%" label="Uptime" icon="⚡" color="success" trend="+0.1%" trendtype="up" description="vs mes anterior"}
::stat{value="3" label="Temas disponibles" icon="🎨" color="info"}
::stat{value="12ms" label="Tiempo de carga" icon="🚀" color="warning" trend="-8ms" trendtype="up" description="mejora"}
:::

### Parámetros de `:::statgroup`

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `cols` | `"1"` \| `"2"` \| `"3"` \| `"4"` | `"3"` | Columnas del grid |

### Parámetros de `::stat`

| Parámetro | Tipo | Descripción |
|---|---|---|
| `value` | `string` | Valor principal grande |
| `label` | `string` | Etiqueta descriptiva |
| `description` | `string` | Texto pequeño debajo de la tendencia |
| `icon` | `string` | Emoji en la esquina superior derecha |
| `trend` | `string` | Cambio porcentual (ej: `"+12%"`) |
| `trendtype` | `up` \| `down` \| `neutral` | Color de la tendencia |
| `color` | `primary` \| `success` \| `warning` \| `danger` | Color del valor principal |

---

## Progress (`::progress` + `:::progressgroup`)

Barras de progreso animadas con porcentaje, etiqueta y descripción.

```md
:::progressgroup{title="Progreso del curso"}
::progress{value="100" label="Módulo 1: Fundamentos" color="success"}
::progress{value="75" label="Módulo 2: Componentes" color="primary"}
::progress{value="30" label="Módulo 3: Avanzado" color="warning" description="En desarrollo"}
::progress{value="0" label="Módulo 4: Deploy" color="danger" showvalue="false"}
:::
```

:::progressgroup{title="Progreso del curso"}
::progress{value="100" label="Módulo 1: Fundamentos" color="success"}
::progress{value="75" label="Módulo 2: Componentes" color="primary"}
::progress{value="30" label="Módulo 3: Avanzado" color="warning" description="En desarrollo activo"}
::progress{value="0" label="Módulo 4: Deploy" color="danger" showvalue="false"}
:::

### Barra individual

```md
::progress{value="65" label="Completado" color="primary" size="lg" description="65 de 100 tareas"}
```

::progress{value="65" label="Completado" color="primary" size="lg" description="65 de 100 tareas completadas"}

### Parámetros de `:::progressgroup`

| Parámetro | Descripción |
|---|---|
| `title` | Título encima del grupo |

### Parámetros de `::progress`

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `value` | `string` | — | Valor de 0 a 100 |
| `label` | `string` | — | Etiqueta a la izquierda |
| `description` | `string` | — | Texto pequeño debajo de la barra |
| `color` | `primary` \| `success` \| `warning` \| `danger` \| `info` | `primary` | Color de la barra |
| `size` | `sm` \| `md` \| `lg` | `md` | Grosor de la barra |
| `animated` | `"true"` \| `"false"` | `"true"` | Animación de entrada |
| `showvalue` | `"true"` \| `"false"` | `"true"` | Muestra el % a la derecha |
