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
- **Soporte de Scroll Inteligente:** La animación se reinicia automáticamente cuando el componente entra en el campo de visión del usuario mientras navega.
- **Múltiples Shells:** Soporte para `bash`, `powershell`, `cmd`, `node` y `python` con sus respectivos prompts e iconos.
- **Botón de Reinicio:** Un botón interactivo en la esquina superior derecha permite al usuario volver a ver la secuencia manualmente.
- **Feedback Visual:** Muestra un mensaje de éxito (`PROCESS FINISHED`) al finalizar la secuencia.

---

## 📖 Atributos

| Atributo | Descripción |
| -------- | ----------- |
| `shell` | El tipo de terminal: `bash`, `zsh`, `powershell`, `cmd`, `node`, `python`. |
| `title` | (Opcional) El nombre que aparece en la cabecera. Si se omite, se usa el nombre del shell. |
| `staticText` | Un comentario o descripción que aparece fijo al inicio (ej: versión de la herramienta). |
| `commands` | Los comandos a ejecutar. Puedes usar una lista o un string con `\n`. |

---

## 🚀 Ejemplos de Shells

### Bash (Linux/macOS)
Ideal para comandos de sistema y git.

````markdown title="Sintaxis Bash"
:::terminal{shell="bash" staticText="git version 2.34.1" commands="git clone https://github.com/fusiondoc/repo\ncd repo\nls -la"}
:::
````

:::terminal{shell="bash" staticText="git version 2.34.1" commands="git clone https://github.com/user/repo\ncd repo\nls -la"}
:::

### PowerShell (Windows)
Específico para administradores y usuarios de Windows.

````markdown title="Sintaxis PowerShell"
:::terminal{shell="powershell" title="Windows Setup" staticText="Windows 11 Home Edition" commands="Set-ExecutionPolicy RemoteSigned\nGet-Service | Where-Object {$_.Status -eq 'Running'}"}
:::
````

:::terminal{shell="powershell" title="Windows Setup" staticText="Windows 11 Home Edition" commands="Set-ExecutionPolicy RemoteSigned\nGet-Service | Where-Object {$_.Status -eq 'Running'}"}
:::

### Node.js REPL
Para demostrar lógica de JavaScript en el servidor.

````markdown title="Sintaxis Node.js"
:::terminal{shell="node" staticText="Welcome to Node.js v20.11.0" commands="const greeting = 'Hola Fusiondoc';\nconsole.log(greeting.toUpperCase());\n3 * (10 + 5)"}
:::
````

:::terminal{shell="node" staticText="Welcome to Node.js v20.11.0" commands="const greeting = 'Hola Fusiondoc';\nconsole.log(greeting.toUpperCase());\n3 * (10 + 5)"}
:::

### Python REPL
Perfecto para demostraciones de ciencia de datos o scripting.

````markdown title="Sintaxis Python"
:::terminal{shell="python" title="Python Interpreter" staticText="Python 3.12.0 (main, Oct 2 2023)" commands="import math\nmath.sqrt(144)\n[x for x in range(3)]"}
:::
````

:::terminal{shell="python" title="Python Interpreter" staticText="Python 3.12.0 (main, Oct 2 2023)" commands="import math\nmath.sqrt(144)\n[x for x in range(3)]"}
:::

---

## 💡 Comportamiento de Animación

El componente detecta automáticamente cuándo el contenido es visible. Si el usuario hace scroll hacia abajo y luego vuelve a subir, el componente notará que ha vuelto a entrar en el viewport y **reiniciará la escritura**, asegurando que el usuario nunca se pierda la demostración.
