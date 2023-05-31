---
title: "Regla de reasignación de precios inteligente: Seleccionar tipo de regla"
description: Determine el precio del anuncio de Amazon en función de los precios de la competencia mediante la creación de una regla de reasignación de precios inteligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Regla de reasignación de precios inteligente: Seleccionar tipo de regla

>[!IMPORTANT]
>
>Las reglas de reasignación de precios inteligentes no funcionan correctamente si la región de Amazon está configurada como `Inactive` estado, tal como aparece durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en `Active` estado de las tarifas de envío que se sincronizarán desde Amazon.<br><br>
>
>Para actualizar el estado de tu región en la cuenta de Amazon, ve a Configuración > Información de la cuenta > Configuración de vacaciones. Consulte [Amazon: Estado del anuncio para vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Una regla de reasignación de precios inteligente emplea los precios de los competidores de Amazon para determinar el precio del anuncio. Los competidores son otros vendedores que enumeran los mismos productos que el suyo en Amazon.

Las secciones de una regla de reasignación de precios inteligente incluyen:

- Seleccionar tipo de regla
- [Variaciones condicionales del competidor](./competitor-conditional-variances.md)
- [Ajuste de precio](./price-adjustment.md)
- [Precio mínimo](./floor-price.md)
- [Precio de techo opcional](./optional-ceiling-price.md)

## Configuración del tipo de regla

Defina el tipo de regla en _[!UICONTROL Select Rule Type]_sección.

1. Para **[!UICONTROL Rule Type]**, elija `Intelligent repricing rule`.

   Esta configuración habilita la variable _[!UICONTROL Competitor Price Source]_y el [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md), y [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) secciones.

1. Para **[!UICONTROL Competitor Price Source]**, elija una opción:

   - **[!UICONTROL Use "Buy Box" Price]** : elija cuándo desea ajustar los precios de Amazon en función de Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio de venta. A [!DNL Buy Box] el precio existe cuando varios vendedores en Amazon ofrecen el mismo producto. Amazon define el [!DNL Buy Box] vendedor según los requisitos de rendimiento. Los comerciantes buscan ganar el [!DNL Buy Box] el estado del vendedor y ofrecen una visibilidad máxima de sus anuncios de productos.

   - **[!UICONTROL Use Lowest Competitor Price]** - Elige cuándo quieres comparar y ajustar el precio del anuncio a los precios de la competencia para el mismo producto. Cuando se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ Los campos están activados.

1. Si está activada, elija una opción para **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Elija cuándo quiere comparar y ajustar sus precios en función de todos los precios de la competencia para el mismo producto.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Elija cuándo desea limitar los competidores a los que se compara el precio para el mismo producto. Esta configuración reduce aún más a los competidores al exigir que sus anuncios tengan un mínimo del porcentaje elegido de comentarios positivos antes de aplicar la regla de precio más bajo.

1. Si está activado, introduzca un valor numérico para **[!UICONTROL Minimum Feedback Count]**.

   Este valor numérico opcional reduce aún más los precios competitivos. Por ejemplo, si un comerciante tiene un 95 % de votos positivos, pero solo tiene un recuento de votos de `20`Sin embargo, es posible que no sea un competidor en el que desee modificar los precios. Sin embargo, si introduce un valor de `1000`Sin embargo, requeriría que el comerciante tenga un 95% de comentarios positivos y un mínimo de 1000 reseñas de comerciantes.

>[!NOTE]
>
>Puede utilizar estas opciones de precios y comentarios de la competencia para evitar basar los precios en un competidor que tiene comentarios deficientes y que vende un producto de menor calidad.

![Regla de reasignación de precios inteligente: seleccione el tipo de regla](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Rule Type] | Seleccione un tipo de regla. Opciones:<ul><li>**[!UICONTROL Standard price rule]** : este tipo de regla le permite aumentar o reducir el precio de listado de Amazon en un porcentaje específico o en una cantidad en dólares fijos en relación con la variable _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** : este tipo de regla le permite ajustar el precio del anuncio de Amazon según los precios de la competencia. Cuando se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ Los campos están activados.</li></ul> |
| [!UICONTROL Competitor Price Source] | Seleccione el origen de precio deseado. Opciones:<ul><li>**[!UICONTROL Use "Buy Box" Price]** : elija esta opción cuando desee ajustar los precios de Amazon según Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio de venta. A [!DNL Buy Box] el precio existe cuando varios vendedores en Amazon ofrecen el mismo producto. Amazon define el [!DNL Buy Box] vendedor según los requisitos de rendimiento. Los comerciantes buscan ganar el [!DNL Buy Box] el estado del vendedor y ofrecen una visibilidad máxima de sus anuncios de productos.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Elige esta opción cuando quieras comparar y ajustar el precio de tu anuncio a la [precios más bajos para la competencia](./lowest-competitor-pricing.md) para el mismo producto. Cuando se elige, la variable _[!UICONTROL Minimum Positive Feedback]_y_[!UICONTROL Minimum Feedback Count]_ Los campos están activados.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Solo activo si `Use Lowest Competitor Price` se elige. Opciones:<ul><li>**[!UICONTROL All Competitor's Prices]** - Elija cuándo quiere comparar y ajustar sus precios en función de todos los precios de la competencia para el mismo producto.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Elige cuándo quieres limitar a los competidores con los que comparas y ajusta tus precios. Esta configuración reduce aún más a sus competidores al exigir que sus anuncios tengan un mínimo del porcentaje elegido de comentarios positivos y luego utilicen el precio más bajo de ese subconjunto de competidores.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Solo activo si `Use Lowest Competitor Price` se elige. Este valor numérico opcional reduce aún más la comparación de precios competitivos. Por ejemplo, si un comerciante tiene un 95 % de votos positivos, pero solo tiene un recuento de votos de `20`Sin embargo, es posible que no sea un competidor en el que desee modificar los precios. Sin embargo, si introduce un valor de `1000`Sin embargo, requeriría que el comerciante tenga un 95% de comentarios positivos y un mínimo de 1000 reseñas de comerciantes. |
