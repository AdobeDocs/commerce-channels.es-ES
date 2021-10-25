---
title: '''Regla de reprecio inteligente: Variaciones condicionales de la competencia'
description: Determine el precio del anuncio de Amazon en función de los precios y las condiciones de los competidores del producto creando una regla de reprecio inteligente.
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Regla de reprecio inteligente: variaciones condicionales del competidor

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Una regla inteligente de revalorización utiliza los precios de los competidores de Amazon para determinar el precio de su anuncio. Los competidores son otros vendedores que están enumerando los mismos productos que están listando en Amazon.

Si existe un producto con la misma condición, el precio de coincidencia base es el [competidor más bajo](./lowest-competitor-pricing.md) precio con la misma condición. Si ningún producto de la competencia coincide con su condición, el precio de coincidencia base pasa a través de otras condiciones de la competencia disponibles, empezando por Nuevo, Reformado y continuando a través de las condiciones disponibles. Una vez que se encuentre una condición, el precio de coincidencia base será el precio más bajo dentro de esa condición.

Si tiene un producto enumerado con la condición `Used; Good` y el precio base de coincidencia, y un competidor tiene el mismo producto en la misma condición a un precio más bajo, se utiliza el precio del competidor. Si un competidor no existe con la misma condición, el sistema comprueba la existencia de un competidor con la siguiente condición, que es `New`. Si se encuentra un competidor con esa condición, se utiliza el precio más bajo.

## Configurar variaciones condicionales del competidor

Defina las variaciones de condición en la variable _[!UICONTROL Competitor Conditional Variances]_para obtener más información.

Para **[!UICONTROL Conditional Variance]**, elija una opción:

- `Use all competitor's product conditions` - (Predeterminado) Elija cuándo desea que su producto se compare con cualquier condición disponible (si no existe una coincidencia con la condición que está enumerando).

- `Use Only Matching Competitor's Product Condition` - Elija cuándo desea que su producto se compare solamente con los productos de la competencia en la misma condición. Si no existe coincidencia, el precio del producto es el _Fuente de precios del Magento_ definida en [Precio de anuncio](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Elija primero intentar compararlo con su condición de producto coincidente. Si no existe ninguna condición coincidente, se aplica una varianza (como porcentaje) en relación con la condición del producto y la condición del competidor más bajo.

   Cuando la variable _[!UICONTROL Apply Variance]_se elige la función , se muestran campos de variación adicionales para cada una de las condiciones de Amazon. Esta función le permite utilizar reglas de revalorización inteligentes cuando ofrece productos que están en una condición diferente a la de sus competidores. Para comprender el cálculo de la varianza condicional, primero debe comprender que toda la varianza se determina a partir de un precio de coincidencia base.

   Las opciones de varianza condicional que aparecen se basan en la configuración de listado de `Condition` que se asignan a valores de condición mediante un [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Para todas las condiciones asignadas, puede definir un porcentaje de varianza del 1 al 100. La excepción son las coleccionables, en cuyo caso se puede aplicar un porcentaje bueno a 100.

![Regla de reprecio inteligente: variaciones condicionales del competidor](assets/amazon-competitor-cond-variances.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | Opciones: <ul><li>**[!UICONTROL Use all competitor's product conditions]** - Si no existe una coincidencia con la condición con la que está enumerando su producto, esta opción coincide con cualquier condición disponible. Primero intenta hacer coincidir su condición y luego funciona de la `New` condición para `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** - Esta opción coincide con la condición del producto. Si no existe coincidencia, los precios del producto en la variable _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** - Esta opción primero intenta coincidir con la condición del producto. Si no existe ninguna condición coincidente, se aplica una varianza (como porcentaje) en relación con la condición del producto y la condición del competidor más bajo.</li></ul><br><br>Las opciones de varianza condicional que aparecen en función de la configuración de listado para Condición que están asignadas a valores de condición usando un [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Para todas las condiciones asignadas, puede indicar un porcentaje de varianza del 1 al 100. La excepción son las coleccionables, en cuyo caso se puede aplicar un porcentaje bueno a 100.<br><br>Esta función le permite utilizar reglas de revalorización inteligentes cuando ofrece productos que están en una condición diferente a la de sus competidores. Para comprender el cálculo de la varianza condicional, primero debe comprender que toda la varianza se determina a partir de un precio de coincidencia base. |

## Calcular la base de variación condicional

- Varianza de condición de coincidencia base (BMC) = La varianza para la condición de su competidor de precio de coincidencia base. Utilizando el ejemplo anterior, BMC es la varianza para la variable `New` condición.
- Varianza de condición del comerciante (MCV) = La varianza de la condición de su producto. En el ejemplo anterior, MCV = la varianza del `Used; Good` condición.
- Precio de coincidencia base (BMP) = 7,99 $ (explicado anteriormente)

La fórmula para calcular la base de varianza condicional es la siguiente:

![fórmula de cálculo de base de varianza condicional](assets/amazon-cond-variance-calc-1.png)

## Ejemplo

La configuración de variación condicional es la siguiente:

![ejemplo de configuración de varianza condicional](assets/amazon-cond-variances.png)

- BMC = 100 (Condición de la competencia = Nuevo)
- MCV = 80 (Condición de comerciante = Utilizado; Bueno)
- BMP = 7,99 $ (precio base del partido = precio más bajo de la condición del competidor coincidente)

![ejemplo de cálculo de base de varianza condicional](assets/amazon-cond-variance-calc-2.png)

Utilizando el cálculo de base de varianza condicional desde arriba, la base de varianza condicional = 6,39 $. Este cálculo es la fuente de precios de la competencia utilizada para las acciones de reglas de precio, explicada más adelante en [Ajuste de precio](./price-adjustment.md).
