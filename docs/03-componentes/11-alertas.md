---
title: "Alertas"
category: "Componentes"
order: 11
---

# Componente de Alertas

Bloques de notificación modernos con 6 tipos visuales, título opcional, icono personalizable y opción de cierre.

:::alert{type="info" title="Información"}
Esto es una alerta informativa. Usa `type="info"` para mensajes neutros.
:::

:::alert{type="success" title="¡Éxito!"}
Operación completada correctamente. Ideal para confirmaciones.
:::

:::alert{type="warning" title="Atención"}
Revisa esta configuración antes de continuar. Algo podría fallar.
:::

:::alert{type="danger" title="Error crítico"}
Esta acción es irreversible. Usa con cuidado en producción.
:::

:::alert{type="tip" title="Consejo"}
Puedes usar markdown dentro de las alertas: `código`, **negrita**, [enlaces](#).
:::

:::alert{type="note"}
Una nota sin título. El tipo `note` es para comentarios neutrales discretos.
:::

## Uso básico

```md
:::alert{type="info" title="Mi título"}
Contenido de la alerta con **markdown** normal.
:::
```

> **Nota:** Las alertas usan `:::` (3 colons) — son directivas contenedor.

## Tipos disponibles

| Tipo | Color | Uso recomendado |
|---|---|---|
| `info` | 🔵 Azul | Información general |
| `success` | 🟢 Verde | Confirmaciones, logros |
| `warning` | 🟡 Amarillo | Advertencias, cosas a revisar |
| `danger` | 🔴 Rojo | Errores, acciones destructivas |
| `tip` | 🟣 Violeta | Consejos, buenas prácticas |
| `note` | ⚫ Gris | Notas discretas |

## Parámetros

| Parámetro | Tipo | Por defecto | Descripción |
|---|---|---|---|
| `type` | `info` \| `success` \| `warning` \| `danger` \| `tip` \| `note` | `info` | Tipo de alerta |
| `title` | `string` | — | Título en negrita encima del contenido |
| `icon` | `string` | Automático | Emoji o texto para reemplazar el icono |
| `dismissible` | `"true"` | — | Muestra botón ✕ para cerrar la alerta |

## Ejemplos

### Con icono personalizado

```md
:::alert{type="success" title="Deployment exitoso" icon="🚀"}
La aplicación fue desplegada en producción a las 14:32.
:::
```

:::alert{type="success" title="Deployment exitoso" icon="🚀"}
La aplicación fue desplegada en producción a las 14:32.
:::

### Alerta descartable

```md
:::alert{type="warning" title="Sesión por expirar" dismissible="true"}
Tu sesión expirará en 5 minutos. Guarda tu trabajo.
:::
```

:::alert{type="warning" title="Sesión por expirar" dismissible="true"}
Tu sesión expirará en 5 minutos. Guarda tu trabajo.
:::

### Con código inline

```md
:::alert{type="tip" title="Consejo de rendimiento"}
Usa `React.memo()` para evitar re-renders innecesarios en componentes pesados.
:::
```

:::alert{type="tip" title="Consejo de rendimiento"}
Usa `React.memo()` para evitar re-renders innecesarios en componentes pesados.
:::

:::alert{type="danger" title="Importante"}
Nunca expongas tu `API_SECRET` en el código del cliente. Usa variables de entorno en el servidor.
:::
