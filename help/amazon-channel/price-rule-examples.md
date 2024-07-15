---
title: 'Canal de ventas de Amazon: ejemplos de reglas de precios'
description: Para diseñar las reglas de asignación de precios de los anuncios de Amazon, revisa estos ejemplos en función de escenarios comunes.
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# Ejemplos de reglas de precios

## Ejemplos de reglas de precios estándar

### Descartar reglas subsiguientes

La capacidad de descartar las reglas subsiguientes es una función muy útil dentro de las reglas de precios que evita que se apilen varias reglas de precios y proporciona descuentos adicionales no deseados. Para descartar reglas subsiguientes, una regla de asignación de precios debe usar las prioridades establecidas en la sección _[!UICONTROL Priority]_de [Configuración general de regla de asignación de precios](./pricing-rule-general-settings.md).

Si **[!UICONTROL Discard Subsequent Rules]** se establece en `Yes`, las reglas con prioridad inferior (números más altos) no se aplican a los productos aptos.

Por ejemplo, supongamos que hay tres reglas de precios:

| Ejemplo | Nombre de regla | Prioridad | Descartar regla posterior |
|---------|-----------------------|----------|-------------------------|
| 1 | 10% de descuento en productos de venta | 1 | No |
| 2 | $2 productos de descuento | 2 | Sí |
| 3 | 5% de descuento en todos los productos | 3 | No |

En esta situación, las #1 de reglas y #2 se aplican a los productos aptos. La regla #3 solo se aplica a los productos aptos que no están incluidos en la regla #2 porque tiene una prioridad inferior a la del ejemplo #2 y **[!UICONTROL Discard Subsequent Rules]** está establecido en `Yes`. Por lo tanto, los productos aptos de la categoría de venta recibirán un 10% de descuento y 2 dólares de descuento sobre el precio de venta de Amazon.

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

### Precio de Buy Box con precio mínimo Source = Precio

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

Como el precio de [Buy Box](./buy-box-competitor-pricing.md) es menor que el precio original, el producto se muestra al precio original.

El precio final después de aplicar la regla: 15 $

#### Product 2

Precio: 5 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $10

Como el precio de [Buy Box](./buy-box-competitor-pricing.md) es mayor que el precio original, el producto se muestra al precio de [Buy Box](./buy-box-competitor-pricing.md).

El precio final después de aplicar la regla: 10 $

### Precio de Buy Box con precio mínimo Source = Precio y un descenso del 20 %

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

Dado que el precio de [Buy Box](./buy-box-competitor-pricing.md) es menor que el [Precio mínimo](./floor-price.md) calculado, el producto se muestra en el [Precio mínimo calculado](./floor-price.md).

El precio final después de aplicar la regla: 16 $

#### Product 2

Precio: 15 $

[Precio mínimo](./floor-price.md) calculado: 12 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $15

Dado que el precio de [Buy Box](./buy-box-competitor-pricing.md) es mayor que el [precio mínimo](./floor-price.md) calculado, el producto se muestra al precio de [Buy Box](./buy-box-competitor-pricing.md).

El precio final después de aplicar la regla: 15 $

#### Product 3

Precio: 17 $

Precio mínimo calculado: 13,60 $

[Buy Box](./buy-box-competitor-pricing.md) precio de Amazon: $15

Dado que el precio de [Buy Box](./buy-box-competitor-pricing.md) es mayor que el [precio mínimo](./floor-price.md) calculado, el producto se muestra al precio de [Buy Box](./buy-box-competitor-pricing.md).

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
| 17 $ | Nuevo |
| 15 $ | Nuevo |
| 14 $ | Usado; Muy bueno |
| 13 $ | Usado; bueno |

#### Product 1

Precio: 10 $

Condición: nueva

Como el precio más bajo de la competencia para la condición Nueva es de 15 $, el producto aparece en 15 $.

El precio final después de aplicar la regla: 15 $

#### Product 2

Precio: 10 $

Condición: usado, aceptable

Como el [precio más bajo para la competencia](./lowest-competitor-pricing.md) de la condición Usada es de 13 $, el producto se muestra en 13 $.

El precio final después de aplicar la regla: 13 $

### Regla de reasignación de precios inteligente que combina precio máximo, conversión de divisa e IVA

| Campo | Configuración |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10 % |
| [!UICONTROL Ceiling price source] | 10 $ |
| [!UICONTROL Currency conversion] | 1,25 euros:1 USD |

[Precio de techo](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 dólares x 1,25 = 12,50 dólares

Cuando se alcanza el [precio máximo](./optional-ceiling-price.md) en el mercado europeo (IVA), se calcula y se agrega el IVA.

Precio final después del IVA: 12,50 $ x (1,1) = 13,75 $

### Combinación de varias reglas de precios, precio máximo, conversión de divisa e IVA

#### Regla de precios inteligente (del ejemplo anterior)

| Campo | Configuración |
|----------------------|---------------|
| Prioridad | 1 |
| IVA | 10 % |
| Fuente de precio de techo | 10 $ |
| Conversión de moneda | 1,25 euros:1 USD |

[Precio de techo](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 dólares x 1,25 = 12,50 dólares

Precio final después del IVA: 12,50 $ x (1,1) = 13,75 $

#### Regla de precios estándar

| Campo | Configuración |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Aumentar en |
| [!UICONTROL Apply] | Aplicar como cantidad fija |
| [!UICONTROL Adjustment Amount] | 5,00 USD |

Cuando se alcanza el [precio máximo](./optional-ceiling-price.md), la regla de precios estándar se aplica sobre la regla de precios inteligente.

Precio final después de aplicar la regla de precios estándar: 13,75 $ + 5 $ = 18,75 $

### Ajuste de precio

En este ejemplo, el precio más competitivo se define mirando el precio más bajo de la competencia [de Amazon](./lowest-competitor-pricing.md) con un 95% de comentarios positivos y un recuento mínimo de 1000 reseñas de comerciantes.

![Ejemplo de ajuste de precio](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

Después de realizar esta búsqueda en función de estos parámetros, el precio competitivo regresa a 25 $.

A partir de aquí, hay tres opciones diferentes de [acción de regla de precio](./pricing-rule-actions.md) basadas en el precio más bajo.

| Campo | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]**: esta opción reduce el precio del anuncio en relación con el [precio más bajo de la competencia](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]**: esta opción aumenta el precio del anuncio en relación con el [precio más bajo de la competencia](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]**: esta opción cambia el precio del anuncio de Amazon para que coincida con el precio más bajo en función de los parámetros. En el ejemplo, el precio de venta de Amazon es de 25 $.</li></ul> |
| [!UICONTROL Apply] | Opciones: Aplicar como porcentaje / Aplicar como importe fijo |
| [!UICONTROL Adjustment Amount] | Valor numérico para definir el porcentaje o el importe fijo del descuento que se va a aplicar. <br>Estas selecciones resultan en tomar el precio más bajo y establecerlo en $0.01 menos. |

### Precio mínimo

| Campo | Configuración |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | Costo = 5 $ |
| [!UICONTROL Floor Price Action] | Aumentar en |
| [!UICONTROL Apply] | Aplicar como porcentaje |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Cálculo del precio mínimo](./floor-price.md) = Source del precio mínimo `$5` x Importe de ajuste de piso `5%` = 5,25 $

Cuando se aplica la regla de precios inteligente, permite que el precio de la lista sea inferior a 5,25 $ para este producto específico cuando el coste es de 5 $.
