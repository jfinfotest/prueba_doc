---
title: Pasos Personalizados
description: Aprende a crear guías paso a paso interactivas con componentes anidados.
---

# Guía de Instalación Avanzada

En esta sección veremos cómo utilizar el componente para crear flujos de trabajo claros.

::::::steps

:::::step{title="Preparar el entorno"}
Primero, asegúrate de tener todas las dependencias instaladas en tu sistema. Puedes verificar tu versión de Node.js con el siguiente comando:

::terminal{shell="bash" commands="node --version"}

Si no tienes una versión reciente, por favor actualízala antes de continuar.
:::::

:::::step{title="Configurar variables de entorno"}
Crea un archivo `.env` en la raíz de tu proyecto. Puedes elegir entre diferentes entornos usando las pestañas a continuación:

::::tabs

:::tab{title="Desarrollo" icon="mdi:dev-to"}
```env
NEXT_PUBLIC_API_URL=http://localhost:3000
DEBUG=true
```
:::

:::tab{title="Producción" icon="mdi:rocket"}
```env
NEXT_PUBLIC_API_URL=https://api.tuproyecto.com
DEBUG=false
```
:::

::::

:::::

:::::step{title="Ejecutar la aplicación"}
Finalmente, inicia el servidor de desarrollo y abre tu navegador en `http://localhost:3000`.

::terminal{shell="bash" commands="npm run dev"}

¡Listo! Ya tienes tu entorno configurado y funcionando.
:::::

::::::
