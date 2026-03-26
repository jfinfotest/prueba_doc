---
title: Terminal Animada
category: Componentes
order: 2
categoryOrder: 2
---

# Terminal Animada

El componente `:::terminal` proporciona una consola visual interactiva que simula la escritura de comandos en tiempo real. Es ideal para guías de instalación y tutoriales paso a paso.

---

## ✨ Características

- **Animación de Digitación:** Simula que un usuario real está escribiendo los comandos.
- **Personalización Total:** Cambia el título de la ventana y añade texto explicativo.
- **Multicomando:** Ejecuta una secuencia de comandos uno tras otro.
- **Feedback Visual:** Muestra un mensaje de éxito al finalizar la secuencia.

---

## 📖 Cómo configurarlo

Se utiliza mediante la directiva `:::terminal` con los siguientes atributos:

| Atributo | Descripción |
| -------- | ----------- |
| `title` | El nombre que aparece en la cabecera de la terminal (ej: `bash`, `powershell`). |
| `staticText` | Un comentario o descripción que aparece fijo al inicio. |
| `commands` | Los comandos a ejecutar, separados por `\n`. |

### Ejemplo de Markdown

```markdown
:::terminal{title="PowerShell" staticText="Setup inicial..." commands="npm install\nnpm run dev"}
:::
```

### Ejemplo en Vivo

:::terminal{title="Zsh" staticText="Desplegando aplicación en producción..." commands="npm run build\nnpm run start"}
:::

---

## 💡 Casos de Uso

1. **Guías de Inicio Rápido:** Para que el usuario vea exactamente qué escribir.
2. **Ejemplos de CLI:** Demostrar cómo interactúa tu herramienta de línea de comandos.
3. **Automatización:** Visualizar procesos complejos de CI/CD.
