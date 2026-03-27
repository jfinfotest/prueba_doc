---
title: "Gráficos con Chart.js"
category: "Componentes"
order: 16
---

# Gráficos con Chart.js

El componente `chart` permite integrar gráficos interactivos de [Chart.js](https://www.chartjs.org/) pasando los datos y opciones como strings JSON.

## Gráfico de Barras

```md
::chart{type="bar" title="Ventas Mensuales" data='{"labels":["Ene","Feb","Mar","Abr","May"],"datasets":[{"label":"Ventas 2026","data":[12,19,3,5,2],"backgroundColor":"rgba(59,130,246,0.5)","borderColor":"rgb(59,130,246)","borderWidth":1}]}'}
```

::chart{type="bar" title="Ventas Mensuales" data='{"labels":["Ene","Feb","Mar","Abr","May"],"datasets":[{"label":"Ventas 2026","data":[12,19,3,5,2],"backgroundColor":"rgba(59,130,246,0.5)","borderColor":"rgb(59,130,246)","borderWidth":1}]}'}

---

## Gráfico de Líneas

```md
::chart{type="line" title="Usuarios Activos" data='{"labels":["Semana 1","Semana 2","Semana 3","Semana 4"],"datasets":[{"label":"Usuarios","data":[400,600,800,1200],"fill":true,"borderColor":"rgb(16,185,129)","tension":0.3}]}'}
```

::chart{type="line" title="Usuarios Activos" data='{"labels":["Semana 1","Semana 2","Semana 3","Semana 4"],"datasets":[{"label":"Usuarios","data":[400,600,800,1200],"fill":true,"borderColor":"rgb(16,185,129)","tension":0.3}]}'}

---

## Gráfico Circular (Doughnut)

```md
::chart{type="doughnut" title="Distribución de Navegadores" height="350px" data='{"labels":["Chrome","Firefox","Safari","Edge"],"datasets":[{"label":"Market Share","data":[65,15,12,8],"backgroundColor":["rgba(255,99,132,0.5)","rgba(54,162,235,0.5)","rgba(255,206,86,0.5)","rgba(75,192,192,0.5)"]}]}'}
```

::chart{type="doughnut" title="Distribución de Navegadores" height="350px" data='{"labels":["Chrome","Firefox","Safari","Edge"],"datasets":[{"label":"Market Share","data":[65,15,12,8],"backgroundColor":["rgba(255,99,132,0.5)","rgba(54,162,235,0.5)","rgba(255,206,86,0.5)","rgba(75,192,192,0.5)"]}]}'}

---

## Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `type` | `string` | `"bar"` | bar, line, doughnut, pie, radar, polarArea |
| `data` | `JSON string` | — | Objeto de datos (requerido) |
| `options` | `JSON string` | — | Opciones de Chart.js |
| `title` | `string` | — | Título del gráfico |
| `height` | `string` | `"300px"` | Altura del contenedor |

> [!IMPORTANT]
> Los atributos de directivas (`{data="..."}`) deben estar en una **sola línea** y no contener saltos de línea dentro del valor para evitar errores de parseo en MDX. Usa comillas simples `'` para el atributo si el JSON usa comillas dobles `"`.
