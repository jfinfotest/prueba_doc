---
title: Ejemplos de Código
description: Demostración de bloques de código avanzados y funcionalidad de pestañas.
---

# Ejemplos de Código

En esta página demostraremos las nuevas funciones avanzadas de los bloques de código: control de zoom, modo pantalla completa, numeración de líneas que se puede encender y apagar, y pestañas de código perfectas.

## Bloque de Código con Numeración Resaltado

Aquí hay un bloque de código estándar que muestra las características. Puedes encender la configuración de numeración de líneas o resaltar código específico:

```ts {2,6} showLineNumbers
// src/utils/math.ts
export function sumar(a: number, b: number): number {
  return a + b;
}

console.log(sumar(5, 10)); // La línea 2 y 6 están resaltadas!
```

## Pestañas de Código Limpias (Code Tabs)

Gracias a `remark-directive`, ahora podemos escribir pestañas nativas sin ensuciar nuestro markdown con HTML, asegurando que el código interno se formatee de manera impecable! (Usa 4 dos puntos para el contenedor principal y 3 para las pestañas).

::::tabs

:::tab{title="npm" value="npm"}
```bash showLineNumbers
npm install react react-dom
npm run dev
```
:::

:::tab{title="yarn" value="yarn"}
```bash showLineNumbers
yarn add react react-dom
yarn dev
```
:::

:::tab{title="pnpm" value="pnpm"}
```bash showLineNumbers
pnpm add react react-dom
pnpm dev
```
:::

::::

### Diferentes Lenguajes en Pestañas

::::tabs

:::tab{title="Python" value="py"}
```python showLineNumbers
def greet(name: str):
    print(f"Hello, {name}!")

greet("World")
```
:::

:::tab{title="JavaScript" value="js"}
```javascript showLineNumbers
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("World");
```
:::

:::tab{title="Rust" value="rs"}
```rust showLineNumbers
fn greet(name: &str) {
    println!("Hello, {}!", name);
}

fn main() {
    greet("World");
}
```
:::

::::

¡Usa los controles ubicados en la parte superior derecha de cada bloque de código para hacer zoom, alternar la numeración o maximizar la pantalla!
