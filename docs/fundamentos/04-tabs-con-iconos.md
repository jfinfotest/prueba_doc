---
title: Pestañas con Iconos
category: Componentes
order: 1
categoryOrder: 2
---

# Pestañas de Código (Code Tabs)

El componente `:::tabs` permite agrupar múltiples fragmentos de código o contenido interactivo en una interfaz de pestañas elegante y moderna.

---

## 🚀 Características

- **Iconos Dinámicos:** Integración total con **Iconify**, permitiendo usar miles de iconos de diferentes sets (`mdi`, `logos`, `vscode-icons`, etc.).
- **Diseño Premium:** Estética oscura con estados activos resaltados y transición suave entre pestañas.
- **Soporte de Contenido Mixto:** Puedes incluir bloques de código, texto plano o incluso otros componentes como la **Terminal** dentro de una pestaña.

---

## 📖 Uso Avanzado

### Atributos de Pestaña (`:::tab`)

| Atributo | Descripción |
| -------- | ----------- |
| `title` | El texto que aparecerá en el botón de la pestaña. |
| `icon` | (Opcional) El identificador del icono de Iconify (ej: `logos:npm-icon`). |
| `value` | (Opcional) Un identificador único para la pestaña. Si se omite, se usa el título. |

### Ejemplo: Contenido Mixto (Código + Terminal)

A veces necesitas mostrar el código y luego cómo se ejecuta. Puedes hacerlo anidando una Terminal:

::::tabs

:::tab{title="Instalación" icon="logos:npm-icon"}
```bash
npm install fusiondoc
```
:::

:::tab{title="Ejecución" icon="mdi:play-circle"}
::terminal{shell="bash" commands="npm run start"}
:::

::::

---

## 🎨 Guía de Iconos

Fusiondoc utiliza la librería **Iconify**, lo que te da acceso a más de 200,000 iconos. Algunos de los sets más recomendados son:

| Set | Prefijo | Ejemplo |
| --- | ------- | ------- |
| **Material Design Icons** | `mdi:` | `mdi:github`, `mdi:react` |
| **Programming Logos** | `logos:` | `logos:typescript-icon`, `logos:python` |
| **VS Code Icons** | `vscode-icons:` | `vscode-icons:file-type-js-official` |
| **Simple Icons** | `simple-icons:` | `simple-icons:tailwindcss` |

> [!TIP]
> Puedes buscar cualquier icono en [icon-sets.iconify.design](https://icon-sets.iconify.design/) y copiar su nombre para usarlo en el atributo `icon`.

---

## ⚠️ Reglas de Anidamiento

Cuando anides componentes (ej: una Terminal dentro de una Pestaña), recuerda usar un número diferente de colones (`:`) para que el procesador MDX no se confunda:

```markdown
::::tabs (4 colones para el contenedor)
  :::tab (3 colones para la pestaña)
    ::terminal (2 colones para la terminal)
  :::
::::
```
