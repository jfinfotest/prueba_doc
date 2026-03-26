---
title: Ejemplos de Código
description: Demostración de bloques de código y pestañas con Shiki
---

# Ejemplos de Código

En esta página demostraremos cómo se ven los bloques de código y la funcionalidad de las pestañas de código gracias a la integración con **Shiki**, `rehype-pretty-code` y los componentes personalizados de **Shadcn UI**.

## Bloque de Código Simple

Aquí hay un bloque de código estándar en TypeScript:

```ts
// src/utils/math.ts
export function sumar(a: number, b: number): number {
  return a + b;
}

console.log(sumar(5, 10)); // Output: 15
```

## Pestañas de Código (Code Tabs)

Es muy común querer mostrar el mismo código o comandos en diferentes contextos, como administradores de paquetes o diferentes lenguajes.

<tabs>

<tab title="npm" value="npm">

```bash
npm install react react-dom
npm run dev
```

</tab>

<tab title="yarn" value="yarn">

```bash
yarn add react react-dom
yarn dev
```

</tab>

<tab title="pnpm" value="pnpm">

```bash
pnpm add react react-dom
pnpm dev
```

</tab>

</tabs>

### Diferentes Lenguajes

También podemos usarlo para mostrar implementaciones en diferentes lenguajes:

<tabs>

<tab title="Python" value="py">

```python
def greet(name: str):
    print(f"Hello, {name}!")

greet("World")
```

</tab>

<tab title="JavaScript" value="js">

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet("World");
```

</tab>

<tab title="Rust" value="rs">

```rust
fn greet(name: &str) {
    println!("Hello, {}!", name);
}

fn main() {
    greet("World");
}
```

</tab>

</tabs>

## Características Adicionales

1. Resaltado de sintaxis súper rápido y preciso (basado en TextMate grammars igual que VS Code).
2. Botón de **Copiar a Portapapeles** integrado al pasar el mouse sobre el bloque.
3. Soporte para temas oscuro y claro mediante clases de Tailwind.
