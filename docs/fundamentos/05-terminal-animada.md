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
- **Múltiples Shells:** Soporte para `bash`, `powershell`, `cmd`, `node` y `python` con sus respectivos prompts e iconos.
- **Botón de Reinicio:** Permite al usuario volver a ver la secuencia en cualquier momento.
- **Feedback Visual:** Muestra un mensaje de éxito al finalizar la secuencia.

---

## 📖 Cómo configurarlo

Se utiliza mediante la directiva `:::terminal` con los siguientes atributos:

| Atributo | Descripción |
| -------- | ----------- |
| `shell` | El tipo de terminal: `bash`, `zsh`, `powershell`, `cmd`, `node`, `python`. |
| `title` | (Opcional) El nombre que aparece en la cabecera. Si se omite, se usa el nombre del shell. |
| `staticText` | Un comentario o descripción que aparece fijo al inicio. |
| `commands` | Los comandos a ejecutar, separados por `\\n` o saltos de línea. |

### Ejemplo de PowerShell

```markdown
:::terminal{shell="powershell" staticText="Instalando dependencias de Windows..." commands="Set-ExecutionPolicy RemoteSigned\nnpm install"}
:::
```

:::terminal{shell="powershell" staticText="Configurando entorno de desarrollo..." commands="Set-ExecutionPolicy Bypass -Scope Process\nGet-ChildItem -Path ./docs"}
:::

### Ejemplo de Python REPL

```markdown
:::terminal{shell="python" title="Python Interpreter" staticText="Probando lógica..." commands="print('Hola Mundo')\n[x * 2 for x in range(5)]"}
:::
```

:::terminal{shell="python" title="Python Interpreter" staticText="Debug de variables..." commands="import os\nos.name\nprint('Finalizado')"}
:::

---

## 💡 Casos de Uso

1. **Guías Multiplataforma:** Muestra comandos específicos para Windows (PowerShell) o Linux (Bash).
2. **Tutoriales de Lenguaje:** Simula el uso de consolas interactivas de Node.js o Python.
3. **Instalación de CLI:** Visualizar procesos complejos de configuración.
