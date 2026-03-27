---
title: "Gestión de Temas Personalizados"
order: 2
---

# Gestión de Temas Personalizados

Fusiondoc soporta múltiples temas de color que funcionan de forma independiente al modo claro u oscuro.

## 1. Dónde están los temas
Los temas se encuentran en `src/app/themes/` dentro del proyecto Next.js:
- `default.css`: El tema azulado por defecto.
- `valorant.css`: Un tema inspirado en la estética de Valorant.

## 2. Cómo crear un nuevo tema
1. Crea un archivo `.css` en `src/app/themes/`.
2. Define las variables CSS bajo el atributo `[data-theme='tu-nombre']`.
3. Importa el archivo en `src/app/globals.css`:
   ```css
   @import "./themes/mi-tema.css";
   ```
4. Añádelo al selector en `src/components/ThemeSelector.tsx`.

## 3. Ejemplo de variables de tema
```css
[data-theme='mi-tema'] {
  --background: hsl(0 0% 100%);
  --primary: hsl(200 100% 50%);
  /* ... */
}
```

¡El sistema detectará automáticamente el atributo y aplicará tus colores instantáneamente!
