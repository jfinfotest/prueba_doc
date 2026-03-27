---
title: "Timeline"
category: "Componentes"
order: 12
---

# Componente Timeline

Línea de tiempo vertical para changelogs, historial de versiones, procesos paso a paso, o cualquier secuencia cronológica.

::::timeline{title="Changelog del proyecto"}
:::timelineitem{title="Lanzamiento v2.0" date="Mar 2026" tag="v2.0" tagtype="success" status="active" icon="🚀"}
Rediseño completo del sistema de temas y nuevos componentes MDX: Hero, Carousel, Alert, Timeline.
:::
:::timelineitem{title="Sistema de temas" date="Feb 2026" tag="v1.5" tagtype="default" status="done"}
Implementación de CSS themes con soporte para Valorant, Spotify y modo oscuro/claro independiente.
:::
:::timelineitem{title="Navegación por tópicos" date="Ene 2026" tag="v1.2" tagtype="default" status="done"}
Topic Bar sticky, sidebar filtrado por tópico y control de orden por prefijos numéricos.
:::
:::timelineitem{title="Migración a Next.js" date="Dic 2025" tag="v1.0" tagtype="info" status="done"}
Primera versión estable con App Router, MDX desde GitHub y autocompletado de navegación.
:::
:::timelineitem{title="Soporte multi-idioma" date="Próx." tag="Planeado" tagtype="warning" status="pending"}
Traducción automática y selector de idioma en el header.
:::
::::

## Sintaxis

```md
::::timeline
:::timelineitem{title="Mi evento" date="2026-03-20" status="done"}
Descripción del evento con **markdown** normal.
:::
:::timelineitem{title="En progreso" status="active"}
Este está en curso actualmente.
:::
::::
```

> Usa `::::timeline` (4 colons) y `:::timelineitem` (3 colons) para el anidamiento correcto.

## Parámetros del Timeline

| Parámetro | Tipo | Descripción |
|---|---|---|
| `title` | `string` | Título encima de la línea de tiempo |

## Parámetros de TimelineItem

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `title` | `string` | — | Título del evento |
| `date` | `string` | — | Fecha o período (texto libre) |
| `tag` | `string` | — | Etiqueta badge (ej: `"v1.0"`, `"Nuevo"`) |
| `tagtype` | `default` \| `success` \| `warning` \| `danger` \| `info` | `default` | Color del badge |
| `status` | `done` \| `active` \| `pending` \| `warning` \| `danger` | `done` | Estado del nodo |
| `icon` | `string` | Automático | Emoji o texto para el nodo |

## Estados disponibles

| Status | Visual |
|---|---|
| `done` | ✓ verde — completado |
| `active` | ● verde animado (ping) — en progreso |
| `pending` | ○ gris — pendiente |
| `warning` | ! amarillo — alerta |
| `danger` | ✕ rojo — error/cancelado |

## Ejemplos

### Proceso de instalación

```md
::::timeline{title="Pasos de instalación"}
:::timelineitem{title="Clonar el repositorio" status="done" icon="📁"}
`git clone https://github.com/usuario/proyecto`
:::
:::timelineitem{title="Instalar dependencias" status="done" icon="📦"}
Ejecuta `npm install` en la raíz del proyecto.
:::
:::timelineitem{title="Configurar variables" status="active" icon="⚙️"}
Copia `.env.example` a `.env.local` y completa los valores.
:::
:::timelineitem{title="Iniciar servidor" status="pending" icon="▶"}
Ejecuta `npm run dev` para iniciar en modo desarrollo.
:::
::::
```

::::timeline{title="Pasos de instalación"}
:::timelineitem{title="Clonar el repositorio" status="done" icon="📁"}
`git clone https://github.com/usuario/proyecto`
:::
:::timelineitem{title="Instalar dependencias" status="done" icon="📦"}
Ejecuta `npm install` en la raíz del proyecto.
:::
:::timelineitem{title="Configurar variables de entorno" status="active" icon="⚙️"}
Copia `.env.example` a `.env.local` y completa los valores requeridos.
:::
:::timelineitem{title="Iniciar servidor de desarrollo" status="pending" icon="▶"}
Ejecuta `npm run dev` para iniciar en modo desarrollo.
:::
::::

### Historial con badges de versión

::::timeline
:::timelineitem{title="Corrección crítica" date="26 Mar" tag="v2.0.1" tagtype="danger" status="done" icon="🔥"}
Resuelto bug que bloqueaba la hidratación en SSR con componentes cliente.
:::
:::timelineitem{title="Nueva función" date="20 Mar" tag="v2.0" tagtype="success" status="done"}
Componentes multimedia: **Video**, **ZoomImage**, **Audio** y **Carousel**.
:::
:::timelineitem{title="Deprecación" date="15 Mar" tag="v1.9" tagtype="warning" status="warning"}
El componente `LegacyCode` será eliminado en la próxima versión mayor.
:::
::::
