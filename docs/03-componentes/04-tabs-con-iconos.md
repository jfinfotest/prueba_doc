---
title: Pestañas con Iconos
category: Componentes
order: 1
categoryOrder: 2
description: Guía completa para agrupar fragmentos de código y contenido interactivo mediante el sistema de pestañas premium de Fusiondoc.
---

# Pestañas con Iconos (Tabs)

El componente `:::tabs` es una herramienta fundamental para organizar múltiples variantes de código o configuraciones en un espacio reducido. Su diseño está optimizado para ofrecer una navegación fluida y una estética oscura premium.

---

## 🚀 Características Principales

- **Botonera Fluida**: Interruptores con diseño de "píldora" que resaltan claramente el estado activo.
- **Iconografía Ilimitada**: Integración nativa con el motor **Iconify** para usar cualquier set de iconos (MDI, Logos, VSCode).
- **Contenido Multimodal**: Soporta desde código simple hasta componentes complejos anidados (Terminal, Alertas).
- **Adaptativo**: Funciona perfectamente en dispositivos móviles mediante un sistema de scroll horizontal interno.

---

## 1. Uso Básico y Sintaxis

Para implementar una botonera de pestañas, envuelve tus elementos en el contenedor `::::tabs` y define cada sección con la directiva `:::tab`.

### Ejemplo de Instalación

````markdown title="Sintaxis de instalación"
::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash title="Terminal"
npm install fusiondoc
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash title="Terminal"
pnpm add fusiondoc
```
:::

::::
````

::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash title="Terminal"
npm install fusiondoc
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash title="Terminal"
pnpm add fusiondoc
```
:::

::::

---

## 2. Pestaña de Archivo Individual (Single File)

Puedes usar `::::tabs` con una sola `:::tab` para mostrar un único archivo con su respectivo icono y nombre, manteniendo la consistencia visual sin necesidad de interruptores múltiples.

````markdown title="Sintaxis de archivo único"
::::tabs
:::tab{title="index.js" icon="logos:javascript"}
```js title="src/index.js"
console.log("Visualización de un solo archivo con icono");
```
:::
::::
````

::::tabs
:::tab{title="index.js" icon="logos:javascript"}
```js title="src/index.js"
console.log("Visualización de un solo archivo con icono");
```
:::
::::

---

## 3. Configuración de Atributos

Personaliza cada pestaña utilizando los atributos disponibles en la directiva `:::tab`.

| Atributo | Tipo | Descripción | Ejemplo |
| :--- | :--- | :--- | :--- |
| `title` | `string` | **(Requerido)** El texto visible en el botón de la pestaña. | `title="JavaScript"` |
| `icon` | `string` | Identificador de Iconify para mostrar un icono decorativo. | `icon="logos:python"` |
| `value` | `string` | Identificador interno para la pestaña (útil para persistencia). | `value="python-env"` |

---

## 3. Ejemplos Avanzados

### A. Ecosistema Multi-Lenguaje
Muestra cómo se ve el mismo proceso en diferentes arquitecturas:

````markdown title="Sintaxis multi-lenguaje"
::::tabs

:::tab{title="Python" icon="logos:python"}
```python title="app.py"
def main():
    print("Iniciando con Python...")
```
:::

:::tab{title="Rust" icon="logos:rust"}
```rust title="main.rs"
fn main() {
    println!("Iniciando con Rust...");
}
```
:::

::::
````

::::tabs

:::tab{title="Python" icon="logos:python"}
```python title="app.py"
def main():
    print("Iniciando con Python...")
```
:::

:::tab{title="Rust" icon="logos:rust"}
```rust title="main.rs"
fn main() {
    println!("Iniciando con Rust...");
}
```
:::

::::

### B. Instalaciones Multientorno
Muestra diferentes gestores de paquetes con una estética de terminal integrada:

::::tabs

:::tab{title="npm" icon="logos:npm-icon"}
```bash title="Terminal" {1}
npm install react react-dom next
```
:::

:::tab{title="yarn" icon="logos:yarn"}
```bash title="Terminal" {1}
yarn add react react-dom next
```
:::

:::tab{title="pnpm" icon="logos:pnpm"}
```bash title="Terminal" {1}
pnpm add react react-dom next
```
:::

::::

### C. Contenido Mixto (Código + Terminal)
Puedes guiar al usuario desde la definición del código hasta su ejecución directa.

````markdown title="Sintaxis de contenido mixto"
::::tabs

:::tab{title="Servidor" icon="vscode-icons:file-type-node"}
```js title="server.js"
const http = require('http');
http.createServer((req, res) => res.end('OK')).listen(3000);
```
:::

:::tab{title="Prueba" icon="mdi:play-circle"}
::terminal{shell="bash" staticText="Probando endpoint..." commands="curl http://localhost:3000"}
:::

::::
````

::::tabs

:::tab{title="Servidor" icon="vscode-icons:file-type-node"}
```js title="server.js"
const http = require('http');
http.createServer((req, res) => res.end('OK')).listen(3000);
```
:::

:::tab{title="Prueba" icon="mdi:play-circle"}
::terminal{shell="bash" staticText="Probando endpoint..." commands="curl http://localhost:3000"}
:::

::::

### D. Galería de Lenguajes
Aprovecha el resaltado semántico para múltiples arquitecturas:

````markdown title="Sintaxis de galería"
::::tabs

:::tab{title="Go" icon="logos:go"}
```go title="main.go" {5,8-9} showLineNumbers
package main
import "fmt"
func main() {
    name := "Fusiondoc"
    fmt.Printf("Welcome to %s!\n", name)
}
```
:::

:::tab{title="CSS" icon="vscode-icons:file-type-css"}
```css title="styles/globals.css" {2,7} showLineNumbers
@layer utilities {
  .text-balance {
    text-wrap: balance;
  }
}
```
:::

::::
````

::::tabs

:::tab{title="Go" icon="logos:go"}
```go title="main.go" {5,8-9} showLineNumbers
package main
import "fmt"
func main() {
    name := "Fusiondoc"
    fmt.Printf("Welcome to %s!\n", name)
}
```
:::

:::tab{title="CSS" icon="vscode-icons:file-type-css"}
```css title="styles/globals.css" {2,7} showLineNumbers
@layer utilities {
  .text-balance {
    text-wrap: balance;
  }
}
```
:::

::::

---

## 🎨 Guía de Iconografía (Iconify)

Fusiondoc permite usar cualquier prefijo de Iconify. Aquí tienes los más comunes:

- **Ecosistemas**: `logos:react`, `logos:vue`, `logos:aws`.
- **Archivos**: `vscode-icons:file-type-typescript`, `vscode-icons:file-type-json`.
- **Acciones**: `mdi:check-circle`, `mdi:alert`, `mdi:cog`.

> [!TIP]
> Explora miles de iconos en [icon-sets.iconify.design](https://icon-sets.iconify.design/). Solo necesitas copiar el nombre (ej: `mdi:account`) y pegarlo en el atributo `icon`.

---

## ⚠️ Reglas de Anidamiento

Si necesitas meter Pestañas dentro de Pasos, o Terminales dentro de Pestañas, recuerda la **Jerarquía de Colones** para evitar fugas de sintaxis:

1. **Pasos (Nivel 1)**: `::::::steps`
2. **Pestañas (Nivel 2)**: `::::tabs`
3. **Pestaña (Nivel 3)**: `:::tab`
4. **Terminal (Nivel 4)**: `::terminal`
