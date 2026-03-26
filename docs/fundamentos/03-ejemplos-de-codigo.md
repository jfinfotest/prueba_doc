---
title: Ejemplos de Código Completos
description: Demostración técnica de bloques de código en múltiples lenguajes, resaltado de líneas y el componente fusionado avanzado.
---

# Ejemplos de Código (Avanzado)

Esta guía te muestra todo el potencial visual de los nuevos componentes interactivos de Fusiondoc. Todas las características están diseñadas para ofrecer una experiencia estética premium e integrada tanto en Modo Claro como Oscuro.

---

## 1. Bloque de Código Estándar con Título y Resaltado (Highlight)

Usa los atributos \`title="..."\`, \`showLineNumbers\` y una clase de resaltado como \`{4,8-9}\` para crear fragmentos de código profundamente documentados.

```ts title="src/lib/database.ts" {4,8-9,12} showLineNumbers
import { Client } from 'pg';

export async function connectDB() {
  // Configuración resaltada
  const client = new Client({
    connectionString: process.env.DATABASE_URL,
  });

  // La conexión a la base de datos es un paso crítico
  await client.connect();
  
  console.log("Conectado a la db exitosamente");
  
  return client;
}
```

---

## 2. Instalaciones Multientorno (Pestañas Terminales)

Cuando quieras documentar instalaciones complejas, usa la directiva contenedora \`::::tabs\` y \`:::tab\` para mostrar una botonera (píldoras fluidas) con fondo negro continuo.

::::tabs

:::tab{title="npm" value="npm"}
```bash title="Instalación vía NPM" {1,4} showLineNumbers
# Instalar dependencias base
npm install react react-dom next

# Instalar utilidades de diseño
npm install -D tailwindcss postcss autoprefixer
```
:::

:::tab{title="yarn" value="yarn"}
```bash title="Instalación vía Yarn" {1,4} showLineNumbers
# Instalar dependencias base
yarn add react react-dom next

# Instalar utilidades de diseño
yarn add -D tailwindcss postcss autoprefixer
```
:::

:::tab{title="pnpm" value="pnpm"}
```bash title="Instalación vía PNPM" {1,4} showLineNumbers
# Instalar dependencias base
pnpm add react react-dom next

# Instalar utilidades de diseño
pnpm add -D tailwindcss postcss autoprefixer
```
:::

::::

---

## 3. Demostración de Lenguajes Populares

Aprovecha el resaltado semántico impulsado por el motor interno (VS Code themes) para soportar múltiples arquitecturas de código en tus tutoriales.

::::tabs

:::tab{title="Python" value="py"}
```python title="api/routes.py" {3,5} showLineNumbers
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "Fusiondoc"}
```
:::

:::tab{title="Go" value="go"}
```go title="main.go" {5,8-9} showLineNumbers
package main

import "fmt"

func main() {
    // Start of the main execution
    name := "Fusiondoc"
    fmt.Printf("Welcome to %s!\n", name)
}
```
:::

:::tab{title="Rust" value="rs"}
```rust title="src/main.rs" {2,5} showLineNumbers
fn greet(name: &str) {
    println!("Resaltando esta línea en Rust para {}", name);
}

fn main() {
    greet("Fusiondoc");
}
```
:::

:::tab{title="CSS" value="css"}
```css title="styles/globals.css" {2,7} showLineNumbers
@layer utilities {
  .text-balance {
    text-wrap: balance;
  }
  
  .code_block_premium {
    background-color: #0d1117;
    border-radius: 0.5rem;
  }
}
```
:::

::::

¡Usa los controles ubicados en la parte superior derecha de cada bloque de código para hacer zoom, alternar la numeración, maximizar la pantalla o copiar automáticamente el fragmento!
