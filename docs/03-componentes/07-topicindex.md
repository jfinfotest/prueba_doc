---
title: "Índice de Tópico Automático"
category: "Componentes"
order: 7
---

# Índice de Tópico Automático (`::topicindex`)

El componente `TopicIndex` genera automáticamente un índice visual con enlaces a todas las páginas de un tópico. Es ideal para usar en las páginas `index.md` de cada sección.

## Uso básico

```md
::topicindex{topic="01-fundamentos"}
```

## Parámetros disponibles

| Parámetro | Tipo | Requerido | Descripción |
|---|---|---|---|
| `topic` | `string` | ✅ | Nombre de la carpeta del tópico (incluido el prefijo numérico) |
| `title` | `string` | ❌ | Título del bloque de índice |
| `description` | `string` | ❌ | Descripción corta debajo del título |

## Ejemplo completo

```md
::topicindex{topic="01-fundamentos" title="Contenido de esta sección" description="Todo lo que necesitas para comenzar"}
```

Esto generará tarjetas con enlaces a todos los archivos dentro de `01-fundamentos/`, excluyendo el `index.md` propio.

## Comportamiento

- **Automático**: Lee la navegación en tiempo real, no requiere mantenimiento manual.
- **Agrupado por categoría**: Si el tópico tiene subcategorías, los enlaces se etiquetan con su categoría.
- **Filtrado inteligente**: Excluye automáticamente la propia página `index.md` para evitar bucles.
- **Responsivo**: Se muestra en una cuadrícula de 1 o 2 columnas según el ancho de pantalla.

## Resultado esperado

::topicindex{topic="03-componentes" title="Otros componentes disponibles" description="Explora más componentes de Fusiondoc"}
