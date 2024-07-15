---
title: 'Canal de ventas de Amazon: [!UICONTROL Price Adjustment]'
description: Configure los ajustes de precios para definir el cálculo de precios cuando haya identificado la fuente de precios del competidor de Amazon.
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>La sección Ajuste de Precio difiere ligeramente para las reglas de reasignación de precios Estándar e Inteligente. **[!UICONTROL Match Competitor Price]** solo está disponible en _[!UICONTROL Price Action]_cuando **[!UICONTROL Rule Type]**está establecido en `Intelligent repricing rule`.

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [Seleccionar tipo de regla](./intelligent-repricing-rules.md)
- [Variaciones condicionales del competidor](./competitor-conditional-variances.md)
- Ajuste de precio
- [Precio mínimo](./floor-price.md)
- [Precio de techo opcional](./optional-ceiling-price.md)

El ajuste de precios define el cálculo de precios cuando se ha identificado el origen de precios del competidor.

## Configuración del ajuste de precios

Defina el ajuste de precios en la sección _[!UICONTROL Price Adjustment]_.

1. Para **[!UICONTROL Price Action]**, elija una opción:

   - `Decrease By`: elige cuándo quieres que se ajuste el valor de origen del precio definido, lo que crea un precio más bajo para la regla, antes de ponerla en venta en Amazon.

   - `Increase By`: elige cuándo quieres ajustar el valor de origen del precio definido, creando un precio más alto para la regla, antes de ponerlo en venta en Amazon.

   - `Match Competitor Price` - (Solo regla de reasignación de precios inteligente) Elige cuándo quieres cambiar el precio del anuncio de Amazon para que coincida con el precio de [competidor más bajo](./lowest-competitor-pricing.md), en función de los comentarios de la competencia y los parámetros de variación. Cuando se establece en `Match Competitor Price`, se eliminan los campos _[!UICONTROL Apply]_y_[!UICONTROL Adjustment Amount]_.

1. Para **[!UICONTROL Apply]**, elija una opción:

   - `Apply as percentage`: elige cuándo quieres que el **[!UICONTROL Magento Price Source]** definido en el [precio del anuncio](./listing-price.md) se ajuste en un porcentaje.

   - `Apply as fixed amount`: elige cuándo quieres que el **[!UICONTROL Magento Price Source]** definido en el [precio del anuncio](./listing-price.md) se ajuste en una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - Cuando **[!UICONTROL Apply]** se establezca en `Apply as percentage`, escriba el valor porcentual (por ejemplo: escriba `25` para un ajuste porcentual del 25%).

   - Cuando **[!UICONTROL Apply]** se establezca en `Apply as fixed amount`, escriba el valor numérico para el importe fijo (ejemplo: escriba `25` para un ajuste fijo de 25 $).

![Regla de reasignación de precios inteligente - ajuste de precio](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Seleccione una acción de ajuste de precios. Opciones: <br>**[!UICONTROL Decrease By]**: elige cuándo quieres que se ajuste el _[!UICONTROL Magento Price Source]_definido en el [precio del anuncio](./listing-price.md), lo que crea un precio más bajo para la regla, antes de ponerlo en venta en Amazon.<br>**[!UICONTROL Increase By]**: elige cuándo quieres que se ajuste el_[!UICONTROL Magento Price Source]_ definido en el [precio del anuncio](./listing-price.md), lo que crea un precio más alto para la regla, antes de ponerlo en venta en Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Solo regla de reasignación de precios inteligente) Elige cuándo quieres cambiar el precio del anuncio de Amazon para que coincida con el precio de [competidor más bajo](./lowest-competitor-pricing.md), en función de los comentarios de la competencia y los parámetros de variación. Si se elige, se eliminan los campos _Aplicar_ e _Importe de ajuste_. |
| [!UICONTROL Apply] | Opciones:<br>**[!UICONTROL Apply as percentage]**- Elige cuándo quieres que el _[!UICONTROL Magento Price Source]_definido en tu [precio del anuncio](./listing-price.md) se ajuste en un porcentaje.<br>**[!UICONTROL Apply as fixed amount]**: elige cuándo quieres que el_[!UICONTROL Magento Price Source]_ definido en el [precio del anuncio](./listing-price.md) se ajuste en una cantidad fija. |
| [!UICONTROL Adjustment Amount] | Requerido.<br>Si elige `Apply as percentage` para **[!UICONTROL Apply]**, escriba el valor porcentual (por ejemplo: escriba `25` para un ajuste porcentual del 25%).<br>Si elige `Apply as fixed amount` para **[!UICONTROL Apply]**, escriba el valor numérico para el importe fijo (ejemplo: escriba `25` para un ajuste fijo de 25 $). |
