---
title: "Diagramas de Flujo"
category: "Componentes"
order: 18
---

# Diagramas de Flujo (ReactFlow)

Crea diagramas interactivos, flujos de datos y visualizaciones de arquitectura directamente en tus archivos MDX.

## Ejemplo Básico

Un flujo simple para demostrar la conexión entre nodos.

```md
::flow{nodes='[
  {"id":"1","data":{"label":"Inicio"},"position":{"x":250,"y":5},"type":"input"},
  {"id":"2","data":{"label":"Procesando..."},"position":{"x":100,"y":100}},
  {"id":"3","data":{"label":"Validación"},"position":{"x":400,"y":100}},
  {"id":"4","data":{"label":"Fin"},"position":{"x":250,"y":200},"type":"output"}
]' edges='[
  {"id":"e1-2","source":"1","target":"2","animated":true},
  {"id":"e1-3","source":"1","target":"3"},
  {"id":"e2-4","source":"2","target":"4"},
  {"id":"e3-4","source":"3","target":"4"}
]'}
```

::flow{nodes='[{"id":"1","data":{"label":"Inicio"},"position":{"x":250,"y":5},"type":"input"},{"id":"2","data":{"label":"Procesando..."},"position":{"x":100,"y":100}},{"id":"3","data":{"label":"Validación"},"position":{"x":400,"y":100}},{"id":"4","data":{"label":"Fin"},"position":{"x":250,"y":200},"type":"output"}]' edges='[{"id":"e1-2","source":"1","target":"2","animated":true},{"id":"e1-3","source":"1","target":"3"},{"id":"e2-4","source":"2","target":"4"},{"id":"e3-4","source":"3","target":"4"}]'}

---

## Arquitectura de Aplicación

Puedes usar diagramas para explicar cómo se comunican los componentes de tu sistema.

```md
::flow{height="500px" nodes='[
  {"id":"client","data":{"label":"Client (Next.js)"},"position":{"x":0,"y":150}},
  {"id":"api","data":{"label":"API Gateway"},"position":{"x":250,"y":150}},
  {"id":"auth","data":{"label":"Auth Service"},"position":{"x":500,"y":50}},
  {"id":"db","data":{"label":"Database (PostgreSQL)"},"position":{"x":500,"y":250}}
]' edges='[
  {"id":"c-a","source":"client","target":"api","label":"HTTP Request","animated":true},
  {"id":"a-au","source":"api","target":"auth","label":"Verify Token"},
  {"id":"a-db","source":"api","target":"db","label":"Query Data"}
]'}
```

::flow{height="500px" nodes='[{"id":"client","data":{"label":"Client (Next.js)"},"position":{"x":0,"y":150}},{"id":"api","data":{"label":"API Gateway"},"position":{"x":250,"y":150}},{"id":"auth","data":{"label":"Auth Service"},"position":{"x":500,"y":50}},{"id":"db","data":{"label":"Database (PostgreSQL)"},"position":{"x":500,"y":250}}]' edges='[{"id":"c-a","source":"client","target":"api","label":"HTTP Request","animated":true},{"id":"a-au","source":"api","target":"auth","label":"Verify Token"},{"id":"a-db","source":"api","target":"db","label":"Query Data"}]'}

---

## Atributos del Componente

| Atributo | Tipo | Descripción |
| :--- | :--- | :--- |
| `nodes` | `JSON` | Arreglo de nodos (id, label, position, type). |
| `edges` | `JSON` | Arreglo de conexiones (id, source, target, label, animated). |
| `height` | `string` | Altura del contenedor (ej: `500px`). Por defecto `400px`. |

> [!TIP]
> Puedes arrastrar los nodos, hacer zoom con la rueda del ratón y mover el lienzo libremente.
