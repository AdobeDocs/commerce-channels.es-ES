---
title: Ejemplos de reglas de precio
description: Para ayudarle a diseñar sus reglas de precios para los anuncios de Amazon, revise estos ejemplos en función de escenarios comunes.
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# Ejemplos de reglas de precio

## Ejemplos de reglas de precio estándar

### Descartar reglas posteriores

La capacidad de descartar reglas subsiguientes es una buena característica de las reglas de precios que impide que se apilen varias reglas de precios y proporciona descuentos adicionales no deseados. Para descartar las reglas siguientes, una regla de precios debe utilizar las prioridades establecidas en la sección _[!UICONTROL Priority]_de [Configuración general de regla de precios](./pricing-rule-general-settings.md).

Si **[!UICONTROL Discard Subsequent Rules]** se configura en `Yes`, las reglas con prioridad menor (números mayores) no se aplican a los productos aptos.

Por ejemplo, supongamos que hay tres reglas de precios:

| Ejemplo | Nombre de regla | Prioridad | Descartar regla posterior |
|----------|----|----|----|
| 1 | 10% de descuento en productos | 1 | No |
| 2 | $2 productos de venta | 2 | Sí |
| 1 | 5% de todos los productos | 1 | No |

En esta situación, las reglas 1 y 2 se aplican a los productos aptos. La regla n.º 3 solo se aplica a los productos aptos que no están incluidos en la regla n.º 2 porque tiene una prioridad menor que el ejemplo n.º 2 y **[!UICONTROL Discard Subsequent Rules]** está configurado en `Yes`. Por lo tanto, los productos aptos de la categoría de venta recibirán un 10% de descuento y 2 dólares de descuento en el precio de venta de Amazon.

### Aplicación de dos reglas de precio estándar

| Campo | Configuración - Regla 1 | Configuración - Regla 2 |
|----------|----|----|
| [!UICONTROL Rule Name] | Regla 1 | Regla 2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Regla de precio estándar | Regla de precio estándar |
| [!UICONTROL Price action] | Disminuir por | Disminuir por |
| [!UICONTROL Apply] | Aplicar como porcentaje | Aplicar como importe fijo |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### Product 1

Precio: 45,49 $

Regla 1 aplicada: 45,49 x (0,9) = 40,94 $

Regla 2 aplicada: 40,94 $ - 10,00 $ = 30,94 $

Se aplica el precio final después de la regla 1 y de la regla 2: 30,94 $

#### Product 2

Precio: 47,76 $

Regla 1 aplicada: 47,76 x (0,9) = 42,98 $

Regla 2 aplicada: 42,98 $ - 10,00 $ = 32,98 $

Se aplica el precio final después de la regla 1 y la regla 2: 32,98 $

## Ejemplos de reglas de revalorización inteligentes

### Precio Buy Box con fuente de precio mínimo = precio

| Campo | Configuración |
|----------|----|
| [!UICONTROL Rule Name] | Regla 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reprecio inteligente |
| [!UICONTROL Competitor Price Source] | Usar precio &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Coincidir precio de la competencia |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Coincidencia |

#### Product 1

Precio: 15 USD

[Comprar ](./buy-box-competitor-pricing.md) Boxprice en Amazon: 10 USD

Dado que el precio del [Buy Box](./buy-box-competitor-pricing.md) es inferior al precio original, el producto aparece al precio original.

El precio final después de aplicar la regla: 15 USD

#### Product 2

Precio: 5 USD

[Comprar ](./buy-box-competitor-pricing.md) Boxprice en Amazon: 10 USD

Dado que el precio del [Buy Box](./buy-box-competitor-pricing.md) es bueno que el precio original, el producto aparece al precio del [Buy Box](./buy-box-competitor-pricing.md).

El precio final después de aplicar la regla: 10 USD

### Precio Buy Box con fuente de precio mínimo = precio y una disminución de precio del 20%

| Campo | Configuración |
|----------|----|
| [!UICONTROL Rule Name] | Regla 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reprecio inteligente |
| [!UICONTROL Competitor Price Source] | Usar precio &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Coincidir precio de la competencia |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Disminuir por |
| [!UICONTROL Apply] | Aplicar como porcentaje |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Product 1

Precio: 20 USD

Precio de piso calculado: 16 USD

[Comprar ](./buy-box-competitor-pricing.md) Boxprice en Amazon: 15 USD

Dado que el precio del [Buy Box](./buy-box-competitor-pricing.md) es menor que el precio del [piso](./floor-price.md) calculado, el producto se muestra en el [precio del piso](./floor-price.md) calculado.

El precio final después de aplicar la regla: 16 USD

#### Product 2

Precio: 15 USD

[Precio de piso](./floor-price.md) calculado: 12 USD

[Comprar ](./buy-box-competitor-pricing.md) Boxprice en Amazon: 15 USD

Dado que el precio del [Buy Box](./buy-box-competitor-pricing.md) es bueno que el precio del [piso](./floor-price.md) calculado, el producto aparece al precio del [Buy Box](./buy-box-competitor-pricing.md).

El precio final después de aplicar la regla: 15 USD

#### Product 3

Precio: 17 USD

Precio de piso calculado: 13,60 $

[Comprar ](./buy-box-competitor-pricing.md) Boxprice en Amazon: 15 USD

Dado que el precio del [Buy Box](./buy-box-competitor-pricing.md) es bueno que el precio del [piso](./floor-price.md) calculado, el producto aparece al precio del [Buy Box](./buy-box-competitor-pricing.md).

El precio final después de aplicar la regla: 15 USD

### Precio más bajo con todos los precios del competidor y usar todas las condiciones de producto del competidor

| Campo | Configuración |
|----------|-----|
| [!UICONTROL Rule Name] | Regla 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Regla de reprecio inteligente |
| [!UICONTROL Competitor Price Source] | Usar el menor precio del competidor |
| [!UICONTROL Minimum Positive Feedback] | Todos los precios de la competencia |
| [!UICONTROL Conditional Variance] | Usar todas las condiciones de producto del competidor |
| [!UICONTROL Price Action] | Coincidir precio de la competencia |
| [!UICONTROL Floor Price Source] | Precio |
| [!UICONTROL Floor Price Action] | Coincidencia |

| Precio | Condición |
|----------|----|
| 17 USD | Nuevo |
| 15 USD | Nuevo |
| 14 USD | Utilizado; Muy bueno |
| 13 USD | Utilizado; Good |

#### Product 1

Precio: 10 USD

Condición: Nuevo

Como el precio más bajo del competidor para la condición New es $15, el producto aparece en $15.

El precio final después de aplicar la regla: 15 USD

#### Product 2

Precio: 10 USD

Condición: Utilizado; Aceptable

Como el [precio más bajo del competidor](./lowest-competitor-pricing.md) para la condición Usado es de $13, el producto aparece en la lista en $13.

El precio final después de aplicar la regla: 13 USD

### Regla de reprecio inteligente que combina precio máximo, conversión de moneda e IVA

| Campo | Configuración |
|----------|-----|
| [!UICONTROL VAT] | 10 % |
| [!UICONTROL Ceiling price source] | 10 USD |
| [!UICONTROL Currency conversion] | 1,25 euros:1 USD |

[Precio máximo ](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 x 1,25 $ = 12,50 $

Cuando se alcanza el [precio máximo](./optional-ceiling-price.md) en el mercado europeo (IVA), se calcula y se añade el IVA.

Precio final después del IVA: 12,50 x (1,1) = 13,75 $

### Combinación de múltiples reglas de precios, precio máximo, conversión de moneda e IVA

#### Regla de precios inteligente (del ejemplo anterior)

| Campo | Configuración |
|----------|----|
| Prioridad | 1 |
| IVA | 10 % |
| Fuente del precio máximo | 10 USD |
| Conversión de moneda | 1,25 euros:1 USD |

[Precio máximo ](./optional-ceiling-price.md) en el mercado europeo (IVA): 10 x 1,25 $ = 12,50 $

Precio final después del IVA: 12,50 x (1,1) = 13,75 $

#### Regla de precios estándar

| Campo | Configuración |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Aumentar por |
| [!UICONTROL Apply] | Aplicar como importe fijo |
| [!UICONTROL Adjustment Amount] | 5,00 USD |

Cuando se visita el [precio máximo](./optional-ceiling-price.md), la regla de precios estándar se aplica sobre la regla de precios inteligente.

Precio final después de aplicar la regla de precios estándar: $13,75 + $5,00 = $18,75

### Ajuste de precio

En este ejemplo, el precio más competitivo se define mirando el [precio más bajo del competidor](./lowest-competitor-pricing.md) de Amazon con un 95% de comentarios positivos y un recuento mínimo de 1000 comentarios del comerciante.

![Ejemplo de ajuste de precio](assets/amazon-price-adjustment-example.png)

Después de realizar esta búsqueda basada en estos parámetros, el precio competitivo vuelve a ser de 25 dólares.

A partir de aquí, hay tres opciones diferentes [price rule action](./pricing-rule-actions.md) basadas en este precio más bajo.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]** - Esta opción reduce el precio de su anuncio en relación con el precio [ más ](./lowest-competitor-pricing.md)bajo del competidor.</li><li>**[!UICONTROL Increase By]** - Esta opción aumenta el precio del anuncio en relación con el precio [ más ](./lowest-competitor-pricing.md)bajo del competidor.</li><li>**[!UICONTROL Match Competitor Price]** - Esta opción cambia el precio de su anuncio de Amazon para que coincida con el precio más bajo en función de los parámetros. En el ejemplo, el precio de Amazon es de 25 $.</li></ul> |
| [!UICONTROL Apply] | Opciones: Aplicar como porcentaje/Aplicar como importe fijo |
| [!UICONTROL Adjustment Amount] | Valor numérico para definir el porcentaje o la cantidad fija para el descuento que se aplicará. <br>Estas selecciones resultan en tomar el precio más bajo y establecerlo en 0,01 dólares menos. |

### Precio mínimo

| Campo | Configuración |
|----------|----|
| [!UICONTROL Floor Price Source] | Costo = 5 USD |
| [!UICONTROL Floor Price Action] | Aumentar por |
| [!UICONTROL Apply] | Aplicar como porcentaje |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Cálculo de ](./floor-price.md) precios del piso = Fuente de precios del piso  `$5` x Importe de ajuste del piso  `5%` = $5,25

Cuando se aplica la regla de precios inteligente, permite que el precio del anuncio sea inferior a 5,25 $ para este producto específico cuando el coste es de 5 $.
