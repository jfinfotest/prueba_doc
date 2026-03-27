---
title: Configuración Local
category: Fundamentos
order: 7
---

# Configuración Local

Para agilizar el desarrollo de tus contenidos, Fusiondoc permite previsualizar los archivos `.md` de tu disco local directamente en el motor Next.js, sin necesidad de subirlos a GitHub.

---

## 🛠️ Requisitos

Debes tener el proyecto del motor (`fusiondoc-next`) y tu repositorio de documentación en la misma máquina.

## 🚀 Cómo activarlo

1. Ve a la carpeta raíz de `fusiondoc-next`.
2. Abre o crea el archivo `.env.local`.
3. Añade la variable `LOCAL_DOCS_PATH` apuntando a la carpeta de tus documentos:

```bash title=".env.local"
LOCAL_DOCS_PATH=C:\Ruta\A\Tu\Proyecto-Documentacion\docs
```

4. Reinicia el servidor de desarrollo (`npm run dev`).

## ✨ Beneficios

- **Previsualización Instantánea:** Los cambios en tus archivos Markdown se reflejan al recargar la página.
- **Depuración de Componentes:** Es ideal para probar que los componentes complejos (como `Steps` o `Terminal`) se renderizan exactamente como deseas antes de publicarlos.
- **Sin Límites de API:** Evitas el límite de peticiones de la API de GitHub durante sesiones largas de edición.

---

> [!IMPORTANT]
> Asegúrate de que la ruta sea absoluta y use barras invertidas (`\`) en Windows o barras diagonales (`/`) en Linux/macOS.
