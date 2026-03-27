---
title: Pasos Personalizados
category: Componentes
order: 3
categoryOrder: 2
description: Aprende a crear guías paso a paso interactivas con componentes anidados y jerarquías seguras.
---

# Guía de Pasos (Steps)

El componente `::::::steps` permite organizar contenido secuencial en una línea de tiempo vertical elegante. Es el contenedor ideal para tutoriales complejos que requieren múltiples tipos de interacción.

---

## ✨ Características

- **Numeración Automática:** Los pasos se numeran solos usando contadores CSS, eliminando errores manuales al reorganizar.
- **Línea de Tiempo Visual:** Una línea vertical conecta visualmente el progreso de la guía.
- **Anidamiento Ilimitado:** Diseñado para contener cualquier otro componente (`Terminal`, `Tabs`, `Código`).

---

## 🏗️ Jerarquía de Colones (Regla de Oro)

Para que el motor de Fusiondoc pueda procesar correctamente componentes uno dentro de otro, debes usar un número distinto de colones (`:`) en cada nivel de profundidad. La estructura recomendada por seguridad es:

- **Nivel 1 (Contenedor de Pasos):** 6 colones (`::::::steps`)
- **Nivel 2 (Paso Individual):** 5 colones (`:::::step`)
- **Nivel 3 (Grupos de Pestañas):** 4 colones (`::::tabs`)
- **Nivel 4 (Pestaña Individual):** 3 colones (`:::tab`)
- **Nivel 5 (Terminal/Leaf):** 2 colones (`::terminal`)

---

## 📖 Ejemplo de Orquestación

Aquí tienes un ejemplo que combina todas las funcionalidades en un solo flujo:

````markdown title="Sintaxis de orquestación"
::::::steps

:::::step{title="1. Iniciando el proyecto"}
Primero, clonamos el repositorio y entramos en la carpeta:

::terminal{shell="bash" commands="git clone https://github.com/fusiondoc/next-starter\ncd next-starter"}
:::::

:::::step{title="2. Instalación de dependencias"}
Selecciona tu gestor de paquetes favorito:

::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash
npm install
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash
pnpm install
```
:::

::::

:::::

:::::step{title="3. Verificación"}
Verifica que todo funciona correctamente:

::terminal{shell="bash" commands="npm run dev"}

> [!NOTE]
> Si la terminal no arranca, revisa tu versión de Node.js.
:::::

::::::
````

::::::steps

:::::step{title="1. Iniciando el proyecto"}
Primero, clonamos el repositorio y entramos en la carpeta:

::terminal{shell="bash" commands="git clone https://github.com/fusiondoc/next-starter\ncd next-starter"}
:::::

:::::step{title="2. Instalación de dependencias"}
Selecciona tu gestor de paquetes favorito:

::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash
npm install
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash
pnpm install
```
:::

::::

:::::

:::::step{title="3. Verificación"}
Verifica que todo funciona correctamente:

::terminal{shell="bash" commands="npm run dev"}

> [!NOTE]
> Si la terminal no arranca, revisa tu versión de Node.js.
:::::

::::::

---

## 💡 Consejos de Diseño

1. **Títulos Descriptivos:** Usa el atributo `title` en cada `:::::step` para guiar al usuario.
2. **Espaciado:** Deja siempre una línea en blanco entre el inicio de un componente y su contenido para asegurar que el procesador MDX lea los bloques correctamente.
3. **Contexto:** Usa alertas (`> [!TIP]`) dentro de los pasos para dar información adicional sin saturar la línea principal.
