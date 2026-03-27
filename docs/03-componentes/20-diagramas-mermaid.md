---
title: "Diagramas Mermaid"
category: "Componentes"
order: 20
---

# Diagramas Mermaid (Text-to-Diagram)

Crea diagramas complejos (flujos, secuencias, gantt) usando una sintaxis de texto simple e intuitiva.

## Diagrama de Flujo

Perfecto para explicar procesos y toma de decisiones.

```md
::mermaid{content="
graph TD
    A[Inicio] --> B{¿Es usuario?}
    B -- Sí --> C[Cargar Dashboard]
    B -- No --> D[Página de Login]
    C --> E[Fin]
    D --> E
"}
```

::mermaid{content="graph TD; A[Inicio] --> B{¿Es usuario?}; B -- Sí --> C[Cargar Dashboard]; B -- No --> D[Página de Login]; C --> E[Fin]; D --> E"}

---

## Personalización de Colores

Puedes cambiar el color principal del diagrama o usar variables de tema avanzadas.

```md
::mermaid{
  primaryColor="#8b5cf6"
  content="
graph LR
    A[Idea] --> B(Proceso)
    B --> C{Éxito}
    C -->|Sí| D[Lanzamiento]
"
}
```

::mermaid{primaryColor="#8b5cf6" content="graph LR; A[Idea] --> B(Proceso); B --> C{Éxito}; C -->|Sí| D[Lanzamiento]"}

---

## Diagrama de Secuencia

Ideal para visualizar interacciones entre componentes o APIs.

```md
::mermaid{content="
sequenceDiagram
    participant U as Usuario
    participant A as App
    participant S as Servidor
    U->>A: Abre App
    A->>S: Petición de Datos
    S-->>A: JSON Response
    A-->>U: Muestra Información
"}
```

::mermaid{content="sequenceDiagram; participant U as Usuario; participant A as App; participant S as Servidor; U->>A: Abre App; A->>S: Petición de Datos; S-->>A: JSON Response; A-->>U: Muestra Información"}

---

## Atributos del Componente

| Atributo | Tipo | Descripción |
| :--- | :--- | :--- |
| `content` | `string` | Definición del diagrama en sintaxis Mermaid. |
| `theme` | `string` | Tema del diagrama (`default`, `dark`, `forest`, `neutral`, `base`). |
| `primaryColor` | `string` | Color HEX principal para el diagrama (ej: `#ff0000`). |
| `themeVariables` | `JSON` | Configuración avanzada de colores (JSON string). |

> [!TIP]
> Mermaid soporta muchísimos más tipos de diagramas, incluyendo **Diagramas de Entidad-Relación (ER)**, **Diagramas de Clase**, **Gráficos de Gantt** y **Mapas Mentales**.
