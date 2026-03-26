---
title: Pestañas con Iconos
category: Componentes
order: 1
categoryOrder: 2
---

# Pestañas de Código (Code Tabs)

El componente `:::tabs` te permite agrupar múltiples fragmentos de código o contenido en una interfaz de pestañas elegante y moderna.

---

## 🚀 Características

- **Iconos Dinámicos:** Soporte para miles de iconos mediante la integración con **Iconify**.
- **Diseño Premium:** Estética oscura optimizada para legibilidad de código.
- **Interactividad Suave:** Cambios instantáneos y estados activos resaltados.

---

## 📖 Uso Básico

Para crear un grupo de pestañas, usa la directiva de contenedor `::::tabs` (con 4 puntos) y envuelve cada pestaña en una directiva `:::tab`.

### Sintaxis en Markdown

```markdown
::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
`npm install`
:::

:::tab{title="yarn" icon="logos:yarn"}
`yarn add`
:::

::::
```

### Ejemplo en Vivo

::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash
npm install fusiondoc-next
```
:::

:::tab{title="yarn" icon="logos:yarn"}
```bash
yarn add fusiondoc-next
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash
pnpm add fusiondoc-next
```
:::

::::

---

## 🎨 Iconos Disponibles

Puedes usar cualquier icono de los sets populares como:
- `logos:typescript-icon`
- `logos:python`
- `logos:rust`
- `mdi:github`
- `vscode-icons:file-type-js-official`

Busca más en: [icon-sets.iconify.design](https://icon-sets.iconify.design/)
