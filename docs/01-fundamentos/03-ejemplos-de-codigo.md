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

## 2. Dominando el Resaltado de Líneas (Masterclass)

El motor de Fusiondoc permite guiar la atención del lector con precisión quirúrgica. Puedes combinar rangos, líneas individuales y múltiples bloques de resaltado en un mismo bloque de código.

### Sintaxis del Atributo de Resaltado
Usa las llaves `{...}` seguidas de los números de línea o rangos separados por comas:
- **Línea única**: `{5}`
- **Rango**: `{10-15}`
- **Combinación**: `{1,3,10-15,20}`

### Ejemplo: Orquestación Compleja

En este ejemplo de React, resaltamos las importaciones críticas, el estado inicial y el bucle principal de renderizado.

```tsx title="components/ComplexDashboard.tsx" {1,6,12-14,22} showLineNumbers
import { useState, useEffect } from 'react';
import { Card } from '@/components/ui/card';

export default function Dashboard() {
  // 1. Estado inicial resaltado
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch('/api/stats')
      .then(res => res.json())
      .then(json => {
        setData(json);
        setLoading(false);
      });
  }, []);

  if (loading) return <div>Cargando...</div>;

  return (
    <div className="grid gap-4">
      {data.map(item => (
        <Card key={item.id}>{item.title}</Card>
      ))}
    </div>
  );
}
```

> [!TIP]
> Puedes usar el resaltado de líneas en combinación con `showLineNumbers` para crear tutoriales altamente técnicos donde cada línea cuenta.

---

¡Usa los controles ubicados en la parte superior derecha de cada bloque de código para hacer zoom, alternar la numeración, maximizar la pantalla o copiar automáticamente el fragmento!
