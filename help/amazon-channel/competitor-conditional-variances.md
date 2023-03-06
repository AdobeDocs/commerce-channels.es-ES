---
title: "Regla de reasignación inteligente: variaciones condicionales de la competencia"
description: Determine el precio del anuncio de Amazon en función de los precios de la competencia y las condiciones del producto creando una regla de reasignación de precios inteligente.
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Regla de reasignación inteligente: variaciones condicionales de la competencia

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Una regla de reasignación de precios inteligente emplea los precios de los competidores de Amazon para determinar el precio del anuncio. Los competidores son otros vendedores que están anunciando los mismos productos que usted está anunciando en Amazon.

Si un producto existe con la misma condición, el precio base de coincidencia es el [competidor más bajo](./lowest-competitor-pricing.md) precio con la misma condición. Si ningún producto de la competencia coincide con su condición, el precio base de coincidencia pasa por otras condiciones de la competencia disponibles, empezando por Nuevo, Reacondicionado y continuando hacia abajo por las condiciones disponibles. Después de encontrar una condición, el precio de coincidencia base será el precio más bajo dentro de esa condición.

Si tiene un producto enumerado con la condición `Used; Good` y el precio base de coincidencia, y un competidor tiene el mismo producto en la misma condición a un precio más bajo, se utiliza el precio del competidor. Si un competidor no existe con la misma condición, el sistema comprueba si hay un competidor con la siguiente condición, que es `New`. Si se encuentra un competidor con esa condición, se utiliza el precio más bajo.

## Configurar variaciones condicionales de la competencia

Defina las variaciones de condición en la variable _[!UICONTROL Competitor Conditional Variances]_sección.

Para **[!UICONTROL Conditional Variance]**, elija una opción:

- `Use all competitor's product conditions` - (Predeterminado) Elige cuándo quieres que tu producto se compare con cualquier condición disponible (si no existe una coincidencia para la condición que estás anunciando).

- `Use Only Matching Competitor's Product Condition` - Elija cuándo desea que su producto se compare únicamente con los productos de la competencia en la misma condición. Si no existe ninguna coincidencia, el producto tiene un precio de _Origen de precio de Magento_ definido en su [Precio del anuncio](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Elige primero intentar comparar con tu condición de producto coincidente. Si no existe ninguna condición que coincida, se aplica una variación (en forma de porcentaje) en relación con la condición del producto y la condición del competidor más bajo.

   Si la variable _[!UICONTROL Apply Variance]_se elige esta función, se muestran campos de variación adicionales para cada una de las condiciones de Amazon. Esta función le permite utilizar reglas de reasignación de precios inteligentes cuando ofrece productos en condiciones diferentes a las de su competencia. Para comprender el cálculo detrás de la variación condicional, primero debe comprender que toda la variación se determina a partir de un precio de coincidencia base.

   Las opciones de variación condicional que aparecen se basan en la configuración del anuncio para `Condition` que se asignan a valores de condición mediante una [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. Para todas las condiciones asignadas, puede definir un porcentaje de varianza de 1 a 100. La excepción son los coleccionables, en cuyo caso se puede aplicar un porcentaje bueno a 100.

![Regla de reasignación de precios inteligente: variaciones condicionales del competidor](assets/amazon-competitor-cond-variances.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | Opciones: <ul><li>**[!UICONTROL Use all competitor's product conditions]** : Si no existe ninguna coincidencia para la condición con la que está poniendo en venta el producto, esta opción coincide con cualquier condición disponible. Primero intenta hacer coincidir su condición y luego funciona a su manera desde el `New` condición para `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** : Esta opción coincide con la condición del producto. Si no existe ninguna coincidencia, los precios del producto en _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** : Esta opción intenta coincidir primero con la condición del producto. Si no existe ninguna condición que coincida, se aplica una variación (como porcentaje) relativa a la condición del producto y a la condición del competidor más bajo.</li></ul><br><br>Las opciones de variación condicional que aparecen en función de la configuración del listado para Condición y que se asignan a valores de condición mediante una [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. Para todas las condiciones asignadas, puede denotar un porcentaje de varianza de 1 a 100. La excepción son los coleccionables, en cuyo caso se puede aplicar un porcentaje bueno a 100.<br><br>Esta función le permite utilizar reglas de reasignación de precios inteligentes cuando ofrece productos en condiciones diferentes a las de su competencia. Para comprender el cálculo detrás de la variación condicional, primero debe comprender que toda la variación se determina a partir de un precio de coincidencia base. |

## Calcular la base de varianza condicional

- Desviación de condición de coincidencia base (BMC) = La variación de la condición de su competidor de precio de coincidencia base. En el ejemplo anterior, BMC es la variación para el `New` condición.
- Varianza de la condición del comerciante (MCV) = La variación de la condición del producto. Utilizando el ejemplo anterior, MCV = la varianza del `Used; Good` condición.
- Precio base de coincidencia (BMP) = 7,99 $ (explicado anteriormente)

La fórmula para calcular la base de varianza condicional es la siguiente:

![fórmula de cálculo base de varianza condicional](assets/amazon-cond-variance-calc-1.png)

## Ejemplo

La configuración de varianza condicional es la siguiente:

![ejemplo de configuración de varianza condicional](assets/amazon-cond-variances.png)

- BMC = 100 (Condición del competidor = Nuevo)
- MCV = 80 (Condición de comerciante = Usado; Bueno)
- BMP = 7,99 $ (precio base de coincidencia = el precio más bajo de la condición de competidor coincidente)

![ejemplo de cálculo de base de varianza condicional](assets/amazon-cond-variance-calc-2.png)

Utilizando el cálculo de la base de varianza condicional anterior, la base de varianza condicional = 6,39 $. Este cálculo es la fuente de precios del competidor que se utiliza para las acciones de regla de precios, como se explica más adelante en [Ajuste de precio](./price-adjustment.md).
