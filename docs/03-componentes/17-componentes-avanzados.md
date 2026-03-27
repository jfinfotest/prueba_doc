---
title: "Componentes Avanzados"
category: "Componentes"
order: 17
---

# Componentes Avanzados

Añade interactividad y un diseño premium a tu documentación con estos componentes especializados, inspirados en los estándares de **Stripe**, **Vercel** y **GitHub**.

## Equipo / Colaboradores

Muestra a los miembros de tu proyecto con una grilla elegante y enlaces sociales dinámicos.

```md
::team{members='[
  {"name":"Juan Pérez","role":"Lead Developer","avatar":"https://i.pravatar.cc/150?u=1","github":"#","twitter":"#"},
  {"name":"Ana Gómez","role":"UI/UX Designer","avatar":"https://i.pravatar.cc/150?u=2","linkedin":"#"},
  {"name":"Carlos Ruiz","role":"Technical Writer","avatar":"https://i.pravatar.cc/150?u=3","website":"#"}
]'}
```

::team{members='[{"name":"Juan Pérez","role":"Lead Developer","avatar":"https://i.pravatar.cc/150?u=1","github":"#","twitter":"#"},{"name":"Ana Gómez","role":"UI/UX Designer","avatar":"https://i.pravatar.cc/150?u=2","linkedin":"#"},{"name":"Carlos Ruiz","role":"Technical Writer","avatar":"https://i.pravatar.cc/150?u=3","website":"#"}]'}

---

## Referencia de API (Cards)

Ideal para documentar objetos complejos como respuestas de API o esquemas de base de datos. Ejemplo inspirado en el objeto **PaymentIntent** de Stripe.

```md
::::propertylist
:::property{name="id" type="string" required="true"}
Identificador único para el objeto. Todos los identificadores de PaymentIntent comienzan con el prefijo `pi_`.
:::
:::property{name="amount" type="integer" required="true" default="0"}
Cantidad positiva que representa cuánto se cobrará en la unidad de moneda más pequeña (ej: 100 para $1.00 USD).
:::
:::property{name="status" type="string" added="2.1.0"}
El estado de este PaymentIntent. Valores posibles: `requires_payment_method`, `requires_confirmation`, `requires_action`, `processing`, `succeeded`, `canceled`.
:::
:::property{name="metadata" type="object"}
Conjunto de pares clave-valor que puedes adjuntar a un objeto. Es útil para almacenar información adicional sobre el objeto en un formato estructurado.
:::
::::
```

::::propertylist
:::property{name="id" type="string" required="true"}
Identificador único para el objeto. Todos los identificadores de PaymentIntent comienzan con el prefijo `pi_`.
:::
:::property{name="amount" type="integer" required="true" default="0"}
Cantidad positiva que representa cuánto se cobrará en la unidad de moneda más pequeña (ej: 100 para $1.00 USD).
:::
:::property{name="status" type="string" added="2.1.0"}
El estado de este PaymentIntent. Valores posibles: `requires_payment_method`, `requires_confirmation`, `requires_action`, `processing`, `succeeded`, `canceled`.
:::
:::property{name="metadata" type="object"}
Conjunto de pares clave-valor que puedes adjuntar a un objeto. Es útil para almacenar información adicional sobre el objeto en un formato estructurado.
:::
::::

---

## Tooltips / Glosario (Contexto Inteligente)

Utiliza tooltips para explicar conceptos técnicos sin obligar al usuario a navegar fuera de la página. Ideal para términos que pueden ser ambiguos para principiantes.

```md
Fusiondoc Next utiliza :tooltip{text="Hydration" hover="El proceso en React donde el JavaScript del lado del cliente se une al HTML generado en el servidor para hacerlo interactivo."} para ofrecer una experiencia fluida. 
Nuestra arquitectura se basa en :tooltip{text="Edge Computing" hover="Ejecución de código en servidores geográficamente cercanos al usuario para reducir la latencia al mínimo."} para una velocidad relámpago.
```

Fusiondoc Next utiliza :tooltip{text="Hydration" hover="El proceso en React donde el JavaScript del lado del cliente se une al HTML generado en el servidor para hacerlo interactivo."} para ofrecer una experiencia fluida. 
Nuestra arquitectura se basa en :tooltip{text="Edge Computing" hover="Ejecución de código en servidores geográficamente cercanos al usuario para reducir la latencia al mínimo."} para una velocidad relámpago.

---

## GitHub Card

Perfecto para enlazar librerías externas o repositorios de ejemplo.

```md
::github{repo="facebook/react" title="React Engine" description="A JavaScript library for building user interfaces."}
```

::github{repo="facebook/react" title="React Engine" description="A JavaScript library for building user interfaces."}

---

## Tabla Comparativa (Pricing / Features)

Compara planes o configuraciones de forma visual. Ejemplo de una comparativa de despliegue.

```md
::::comparison{headers='["Cloud Starter", "Enterprise"]'}
:::comparerow{title="Ubicaciones de Red" values='["10", "Global (100+)"]'}
:::
:::comparerow{title="SLA de Disponibilidad" values='["99.9%", "99.99% Garantizado"]'}
:::
:::comparerow{title="SSO / SAML" values='["X", "Check"]'}
:::
:::comparerow{title="Dominios Personalizados" values='["1", "Ilimitados"]'}
:::
::::
```

::::comparison{headers='["Cloud Starter", "Enterprise"]'}
:::comparerow{title="Ubicaciones de Red" values='["10", "Global (100+)"]'}
:::
:::comparerow{title="SLA de Disponibilidad" values='["99.9%", "99.99% Garantizado"]'}
:::
:::comparerow{title="SSO / SAML" values='["X", "Check"]'}
:::
:::comparerow{title="Dominios Personalizados" values='["1", "Ilimitados"]'}
:::
::::
