---
title: "Fórmulas Vivas"
category: "Componentes"
order: 19
---

# Fórmulas Vivas (Interactive Math)

Convierte fórmulas matemáticas estáticas en exploradores interactivos. Ideal para educación, finanzas y explicaciones científicas.

## Explorador de Ecuación Cuadrática

Ajusta los coeficientes para ver cómo cambia la parábola y el resultado de la función.

```md
::math{
  title="Función Cuadrática"
  formula="f(x) = {a}x^2 + {b}x + {c}"
  expression="a*1**2 + b*1 + c"
  variables='{
    "a": {"min": -10, "max": 10, "step": 0.5, "value": 1, "label": "Coeficiente A"},
    "b": {"min": -10, "max": 10, "step": 0.5, "value": 2, "label": "Coeficiente B"},
    "c": {"min": -10, "max": 10, "step": 1, "value": 1, "label": "Constante C"}
  }'
}
```

::math{title="Explorador de Parábola (en x=1)" formula="f(1) = {a}(1)^2 + {b}(1) + {c}" expression="a*1^2 + b*1 + c" variables='{"a": {"min": -10, "max": 10, "step": 0.5, "value": 1, "label": "Coeficiente A"}, "b": {"min": -10, "max": 10, "step": 0.5, "value": 2, "label": "Coeficiente B"}, "c": {"min": -10, "max": 10, "step": 1, "value": 1, "label": "Constante C"}}'}

---

## Teorema de Pitágoras

Visualiza la relación entre los catetos y la hipotenusa.

```md
::math{
  title="Teorema de Pitágoras"
  formula="h = \sqrt{ {a}^2 + {b}^2 }"
  expression="sqrt(a^2 + b^2)"
  variables='{
    "a": {"min": 1, "max": 50, "step": 1, "value": 3, "label": "Cateto A", "unit": "cm"},
    "b": {"min": 1, "max": 50, "step": 1, "value": 4, "label": "Cateto B", "unit": "cm"}
  }'
}
```

::math{title="Calculadora de Hipotenusa" formula="h = \sqrt{ {a}^2 + {b}^2 }" expression="sqrt(a^2 + b^2)" variables='{"a": {"min": 1, "max": 50, "step": 1, "value": 3, "label": "Cateto A", "unit": "cm"}, "b": {"min": 1, "max": 50, "step": 1, "value": 4, "label": "Cateto B", "unit": "cm"}}'}

---

## Atributos del Componente

| Atributo | Tipo | Descripción |
| :--- | :--- | :--- |
| `formula` | `string` | Plantilla LaTeX con variables en `{var}`. |
| `expression`| `string` | Expresión matemática para evaluar (sintaxis `mathjs`). |
| `variables` | `JSON` | Configuración de sliders (min, max, step, value, label, unit). |
| `title` | `string` | Título opcional del panel. |

> [!TIP]
> Puedes usar cualquier función de calculo soportada por `mathjs` en el atributo `expression`, como `sqrt()`, `pow()`, `sin()`, `log()`, etc.
