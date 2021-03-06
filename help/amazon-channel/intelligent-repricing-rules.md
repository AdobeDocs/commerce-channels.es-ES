---
title: '''Regla de reprecio inteligente: Seleccionar tipo de regla'
description: Determine el precio de anuncio de Amazon según los precios de la competencia creando una regla de reprecio inteligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Regla de reprecio inteligente: seleccionar tipo de regla

>[!IMPORTANT]
>
>Las reglas inteligentes de revalorización no funcionan correctamente si la región de Amazon está configurada en `Inactive` , tal como está durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en `Active` para que las tarifas de envío se sincronicen con Amazon.<br><br>
>
>Para actualizar el estado de su región en su cuenta de Amazon, vaya a Configuración > Información de la cuenta > Configuración de las vacaciones. Consulte [Amazon: Estado de anuncio de las vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Una regla inteligente de revalorización utiliza los precios de los competidores de Amazon para determinar el precio de su anuncio. Los competidores son otros vendedores que enumeran los mismos productos que los suyos en Amazon.

Las secciones de una regla de reasignación de precios inteligente incluyen:

- Seleccionar tipo de regla
- [Variaciones condicionales de la competencia](./competitor-conditional-variances.md)
- [Ajuste de precio](./price-adjustment.md)
- [Precio mínimo](./floor-price.md)
- [Precio máximo opcional](./optional-ceiling-price.md)

## Configuración del tipo de regla

Defina el tipo de regla en la variable _[!UICONTROL Select Rule Type]_para obtener más información.

1. Para **[!UICONTROL Rule Type]**, elija `Intelligent repricing rule`.

   Esta configuración habilita la variable _[!UICONTROL Competitor Price Source]_y [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)y [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) secciones.

1. Para **[!UICONTROL Competitor Price Source]**, elija una opción:

   - **[!UICONTROL Use "Buy Box" Price]** - Elija cuándo desea ajustar los precios de Amazon en función de Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio de venta. A [!DNL Buy Box] El precio existe cuando varios vendedores de Amazon ofrecen el mismo producto. Amazon define [!DNL Buy Box] vendedor en función de los requisitos de rendimiento. Los comerciantes buscan ganar la [!DNL Buy Box] el estado del vendedor y ofrecen la máxima visibilidad de sus listas de productos.

   - **[!UICONTROL Use Lowest Competitor Price]** - Elija cuándo desea comparar y ajustar el precio de su anuncio a los precios de la competencia para el mismo producto. Si se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ los campos están habilitados.

1. Si está activada, elija una opción para **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Elija cuándo desea comparar y ajustar sus precios en función de todos los precios de la competencia para el mismo producto.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Elija cuándo desea limitar a los competidores a los que se compara el precio para el mismo producto. Este ajuste reduce aún más a los competidores al exigir que su cotización tenga un mínimo del porcentaje elegido de comentarios positivos antes de aplicar la regla de precio más bajo.

1. Si está activado, introduzca un valor numérico para **[!UICONTROL Minimum Feedback Count]**.

   Este valor numérico opcional reduce aún más los precios competitivos. Por ejemplo, si un comerciante tiene una clasificación de comentarios positiva del 95 %, pero solo tiene un recuento de comentarios de `20`, puede que no sea un competidor con el que desee modificar sus precios. Sin embargo, si introduce un valor de `1000`, requeriría que el comerciante tenga un 95% de comentarios positivos y un mínimo de 1000 revisiones de comerciantes.

>[!NOTE]
>
>Puede utilizar estas opciones de precios y comentarios del competidor para evitar basar sus precios en un competidor que tiene comentarios deficientes y vende un producto de menor calidad.

![Regla de revalorización inteligente: seleccione el tipo de regla](assets/ob-intelligent-price-rule-type.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Rule Type] | Seleccione un tipo de regla. Opciones:<ul><li>**[!UICONTROL Standard price rule]** - Este tipo de regla le permite aumentar o reducir el precio de la lista de Amazon en un porcentaje específico o una cantidad de dólares fija en relación con la variable _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Este tipo de regla le permite ajustar el precio de su anuncio de Amazon en función de los precios del competidor. Si se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ los campos están habilitados.</li></ul> |
| [!UICONTROL Competitor Price Source] | Seleccione el origen de precio que desee. Opciones:<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Elija esta opción cuando desee ajustar los precios de Amazon en función de Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio de venta. A [!DNL Buy Box] El precio existe cuando varios vendedores de Amazon ofrecen el mismo producto. Amazon define [!DNL Buy Box] vendedor en función de los requisitos de rendimiento. Los comerciantes buscan ganar la [!DNL Buy Box] el estado del vendedor y ofrecen la máxima visibilidad de sus listas de productos.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Elija esta opción cuando desee comparar y ajustar su precio de venta al [precio más bajo para el competidor](./lowest-competitor-pricing.md) para el mismo producto. Si se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ los campos están habilitados.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Solo activa si `Use Lowest Competitor Price` se selecciona. Opciones:<ul><li>**[!UICONTROL All Competitor's Prices]** - Elija cuándo desea comparar y ajustar sus precios en función de todos los precios de la competencia para el mismo producto.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Elija cuándo desea limitar a los competidores a los que compara y ajustar sus precios. Este ajuste reduce aún más a sus competidores al exigir que su cotización tenga un mínimo del porcentaje elegido de comentarios positivos y luego usar el precio más bajo de ese subconjunto de competidores.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Solo activa si `Use Lowest Competitor Price` se selecciona. Este valor numérico opcional reduce aún más la comparación competitiva de precios. Por ejemplo, si un comerciante tiene una puntuación de comentarios positiva del 95 % pero solo tiene un recuento de comentarios de `20`, puede que no sea un competidor con el que desee modificar sus precios. Sin embargo, si introduce un valor de `1000`, requeriría que el comerciante tenga un 95% de comentarios positivos y un mínimo de 1000 revisiones de comerciantes. |
