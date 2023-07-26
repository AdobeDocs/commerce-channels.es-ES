---
title: 'Canal de ventas de Amazon: ejemplos de reglas de precios'
description: Para diseñar las reglas de asignación de precios de los anuncios de Amazon, revisa estos ejemplos en función de escenarios comunes.
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 2%

---

# Ejemplos de reglas de precios

## Ejemplos de reglas de precios estándar

### Descartar reglas subsiguientes

La posibilidad de descartar las reglas subsiguientes es una buena función dentro de las reglas de precios que evita que se apilen varias reglas de precios y proporcione descuentos adicionales no deseados. Para descartar reglas subsiguientes, una regla de asignación de precios debe utilizar las prioridades establecidas en la _[!UICONTROL Priority]_sección de [Configuración general de reglas de precios](./pricing-rule-general-settings.md).

If **[!UICONTROL Discard Subsequent Rules]** se establece en `Yes`Sin embargo, las reglas con prioridad inferior (números más altos) no se aplican a los productos aptos.

Por ejemplo, supongamos que hay tres reglas de precios:

| Ejemplo | Nombre de regla | Prioridad | Descartar regla posterior |
|---------|-----------------------|----------|-------------------------|
| 1 | 10% de descuento en productos de venta | 1 | No |
| 2 | $2 productos de descuento | 2 | Sí |
| 3 | 5% de descuento en todos los productos | 3 | No |

En esta situación, las #1 de reglas y #2 se aplican a los productos aptos. La regla #3 solo se aplica a los productos aptos que no están incluidos en la regla #2 porque tiene una prioridad inferior a la del ejemplo #2 y **[!UICONTROL Discard Subsequent Rules]** se establece en `Yes`. Por lo tanto, los productos aptos de la categoría de venta recibirán un 10% de descuento y 2 dólares de descuento sobre el precio de venta de Amazon.

### Aplicación de dos reglas de precios estándar

| Campo | Configuración - Regla 1 | Configuración - Regla 2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | Regla-1 | Regla-2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Regla de precio estándar | Regla de precio estándar |
| [!UICONTROL Price action] | Disminuir en | Disminuir en |
| [!UICONTROL Apply] | Aplicar como porcentaje | Aplicar como cantidad fija |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### Product 1

Precio: 45,49 $

Regla 1 aplicada: 45,49 $ x (0,9) = 40,94 $

Regla 2 aplicada: 40,94 $ - 10,00 $ = 30,94 $

Se aplica el precio final después de la Regla 1 y la Regla 2: $30.94

#### Product 2

Precio: 47,76 $

Regla 1 aplicada: 47,76 $ x (0,9) = 42,98 $

Regla 2 aplicada: 42,98 $ - 10,00 $ = 32,98 $

Se aplica el precio final después de la regla 1 y la regla 2: $32.98

## Ejemplos de reglas de reasignación de precios inteligentes

### Precio de Buy Box con Origen de Precio de Planta = Precio

| Campo | Configuración |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regla-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reasignación de precios inteligente |
| [!UICONTROL Competitor Price Source] | Utilizar precio de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Igualar precio del competidor |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Coincidencia |

#### Product 1

Precio: 15 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $10

Debido a que el [Buy Box](./buy-box-competitor-pricing.md) el precio es menor que el precio original, el producto se enumera en el precio original.

El precio final después de aplicar la regla: 15 $

#### Product 2

Precio: 5 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $10

Debido a que el [Buy Box](./buy-box-competitor-pricing.md) el precio es bueno que el precio original, el producto se enumera en el [Buy Box](./buy-box-competitor-pricing.md) precio.

El precio final después de aplicar la regla: 10 $

### Precio de Buy Box con Origen de Precio de Planta = Precio y un descenso de precio del 20%

| Campo | Configuración |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regla-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reasignación de precios inteligente |
| [!UICONTROL Competitor Price Source] | Utilizar precio de &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Igualar precio del competidor |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Disminuir en |
| [!UICONTROL Apply] | Aplicar como porcentaje |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Product 1

Precio: 20 $

Precio mínimo calculado: 16 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $15

Debido a que el [Buy Box](./buy-box-competitor-pricing.md) el precio es menor que el calculado [Precio mínimo](./floor-price.md), el producto aparece en la lista Calculado [Precio mínimo](./floor-price.md).

El precio final después de aplicar la regla: 16 $

#### Product 2

Precio: 15 $

Calculado [Precio mínimo](./floor-price.md): 12 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $15

Debido a que el [Buy Box](./buy-box-competitor-pricing.md) el precio es bueno que el calculado [Precio mínimo](./floor-price.md), el producto se enumera en la [Buy Box](./buy-box-competitor-pricing.md) precio.

El precio final después de aplicar la regla: 15 $

#### Product 3

Precio: 17 $

Precio mínimo calculado: 13,60 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $15

Debido a que el [Buy Box](./buy-box-competitor-pricing.md) el precio es bueno que el calculado [Precio mínimo](./floor-price.md), el producto se enumera en la [Buy Box](./buy-box-competitor-pricing.md) precio.

El precio final después de aplicar la regla: 15 $

### Precio más bajo con todos los precios de la competencia y usar todas las condiciones de producto de la competencia

| Campo | Configuración |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | Regla-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reasignación de precios inteligente |
| [!UICONTROL Competitor Price Source] | Utilizar el precio más bajo de competidor |
| [!UICONTROL Minimum Positive Feedback] | Precios de todos los competidores |
| [!UICONTROL Conditional Variance] | Usar todas las condiciones de producto de la competencia |
| [!UICONTROL Price Action] | Igualar precio del competidor |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Coincidencia |

| Precio | Condición |
|-------|-----------------|
| $17 | Nuevo |
| $15 | Nuevo |
| $14 | Usado; Muy bueno |
| $13 | Usado; bueno |

#### Product 1

Precio: 10 $

Condición: nueva

Como el precio más bajo de la competencia para la condición Nueva es de 15 $, el producto aparece en 15 $.

El precio final después de aplicar la regla: 15 $

#### Product 2

Precio: 10 $

Condición: usado, aceptable

Debido a que el [precio más bajo de competidor](./lowest-competitor-pricing.md) para la condición Usado es de $13, el producto se enumera en $13.

El precio final después de aplicar la regla: 13 $

### Regla de reasignación de precios inteligente que combina precio máximo, conversión de divisa e IVA

| Campo | Configuración |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1,25 euros:1 USD |

[Precio de techo](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 $ x 1,25 = 12,50 $

Si la variable [precio máximo](./optional-ceiling-price.md) en el mercado europeo (IVA), el IVA se calcula y se añade.

Precio final después del IVA: 12,50 $ x (1,1) = 13,75 $

### Combinación de varias reglas de precios, precio máximo, conversión de divisa e IVA

#### Regla de precios inteligente (del ejemplo anterior)

| Campo | Configuración |
|----------------------|---------------|
| Prioridad | 1 |
| IVA | 10% |
| Fuente de precio de techo | $10 |
| Conversión de moneda | 1,25 euros:1 USD |

[Precio de techo](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 $ x 1,25 = 12,50 $

Precio final después del IVA: 12,50 $ x (1,1) = 13,75 $

#### Regla de precios estándar

| Campo | Configuración |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Aumentar en |
| [!UICONTROL Apply] | Aplicar como cantidad fija |
| [!UICONTROL Adjustment Amount] | $5.00 |

Si la variable [precio máximo](./optional-ceiling-price.md) se visita, la regla de precios estándar se aplica sobre la regla de precios inteligente.

Precio final después de aplicar la regla de precios estándar: 13,75 $ + 5 $ = 18,75 $

### Ajuste de precio

En este ejemplo, el precio más competitivo se define mirando el Amazon [precio más bajo de la competencia](./lowest-competitor-pricing.md) con un 95% de votos positivos y un recuento mínimo de votos de 1.000 reseñas de comerciantes.

![Ejemplo de ajuste de precio](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

Después de realizar esta búsqueda en función de estos parámetros, el precio competitivo regresa a 25 $.

A partir de aquí, hay tres diferentes [acción de regla de precios](./pricing-rule-actions.md) opciones basadas en este precio más bajo.

| Campo | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]** - Esta opción reduce el precio de tu anuncio en relación con el [precio más bajo de competidor](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** : Esta opción aumenta el precio del anuncio en relación con la [precio más bajo de competidor](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** : Esta opción cambia el precio del anuncio de Amazon para que coincida con el precio más bajo en función de los parámetros. En el ejemplo, el precio de venta de Amazon es de 25 $.</li></ul> |
| [!UICONTROL Apply] | Opciones: Aplicar como porcentaje / Aplicar como importe fijo |
| [!UICONTROL Adjustment Amount] | Valor numérico para definir el porcentaje o el importe fijo del descuento que se va a aplicar. <br>Estas selecciones resultan en tomar el precio más bajo y establecerlo en $0.01 menos. |

### Precio mínimo

| Campo | Configuración |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | Costo = 5 $ |
| [!UICONTROL Floor Price Action] | Aumentar en |
| [!UICONTROL Apply] | Aplicar como porcentaje |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Precio mínimo](./floor-price.md) calculation = Origen de precio mínimo `$5` x Importe de Ajuste de Plano `5%` = 5,25 $

Cuando se aplica la regla de precios inteligente, permite que el precio de la lista sea inferior a 5,25 $ para este producto específico cuando el coste es de 5 $.
