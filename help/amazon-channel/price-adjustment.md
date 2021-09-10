---
title: Ajuste de precio
description: Configure los ajustes de precio para definir el cálculo de precio cuando haya identificado el origen de precio del competidor de Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Ajuste de precio

>[!NOTE]
>
>La sección Ajuste de precio difiere ligeramente para las reglas de reasignación de precios estándar e inteligentes. **[!UICONTROL Match Competitor Price]** solo está disponible en  _[!UICONTROL Price Action]_cuando **[!UICONTROL Rule Type]**se establece en  `Intelligent repricing rule`.

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [Seleccionar tipo de regla](./intelligent-repricing-rules.md)
- [Variaciones condicionales de la competencia](./competitor-conditional-variances.md)
- Ajuste de precio
- [Precio mínimo](./floor-price.md)
- [Precio máximo opcional](./optional-ceiling-price.md)

El ajuste de precio define el cálculo de precio cuando ha identificado la fuente de precios del competidor.

## Configurar el ajuste de precio

Defina el ajuste de precios en la sección _[!UICONTROL Price Adjustment]_.

1. Para **[!UICONTROL Price Action]**, elija una opción:

   - `Decrease By` - Elija cuándo desea que el valor de origen de precio definido se ajuste hacia abajo, lo que crea un precio más bajo para la regla, antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se ajuste el valor de la fuente de precios definido, lo que crea un precio más alto para la regla, antes de cotizar en Amazon.

   - `Match Competitor Price` - (Solo regla de revalorización inteligente) Elija cuándo desea cambiar el precio de anuncio de Amazon para que coincida con el precio de  [competidor ](./lowest-competitor-pricing.md) más bajo, según los comentarios de su competidor y los parámetros de variación. Cuando se establece en `Match Competitor Price`, se eliminan los campos _[!UICONTROL Apply]_y_[!UICONTROL Adjustment Amount]_ .

1. Para **[!UICONTROL Apply]**, elija una opción:

   - `Apply as percentage` - Elija cuándo desea que el  **[!UICONTROL Magento Price Source]** definido en su  [precio de ](./listing-price.md) anuncio se ajuste en un porcentaje.

   - `Apply as fixed amount` - Elija cuándo desea que el  **[!UICONTROL Magento Price Source]** definido en su  [precio de ](./listing-price.md) anuncio se ajuste por una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - Cuando **[!UICONTROL Apply]** está configurado en `Apply as percentage`, introduzca el valor de porcentaje (ejemplo: introduzca `25` para un ajuste del 25%).

   - Cuando **[!UICONTROL Apply]** está configurado en `Apply as fixed amount`, introduzca el valor numérico de la cantidad fija (ejemplo: introduzca `25` para un ajuste fijo de 25 $).

![Regla de revalorización inteligente: ajuste de precio](assets/amazon-price-adjustment.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Price Action] | Elija una acción de ajuste de precios. Opciones:<br>**[!UICONTROL Decrease By]**: elija cuándo desea que el _[!UICONTROL Magento Price Source]_definido en el [Precio de anuncio](./listing-price.md) se ajuste a la baja, lo que crea un precio más bajo para la regla, antes de agregarlo a Amazon.<br>**[!UICONTROL Increase By]**- Elija cuándo desea que se ajuste el_[!UICONTROL Magento Price Source]_ valor definido en el  [Precio de ](./listing-price.md) anuncio, creando un precio más alto para la regla, antes de cotizar en Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Solo regla de revalorización inteligente) Elija cuándo desea cambiar el precio de anuncio de Amazon para que coincida con el precio de  [competidor ](./lowest-competitor-pricing.md) más bajo, según los comentarios de su competidor y los parámetros de variación. Cuando se elige, los campos _Apply_ y _Ajuste Amount_ se eliminan. |
| [!UICONTROL Apply] | Opciones:<br>**[!UICONTROL Apply as percentage]**- Elija cuándo desea que el _[!UICONTROL Magento Price Source]_definido en su [Precio de Listing](./listing-price.md) se ajuste en un porcentaje.<br>**[!UICONTROL Apply as fixed amount]**- Elija cuándo desea que el_[!UICONTROL Magento Price Source]_ definido en su  [precio de ](./listing-price.md) anuncio se ajuste por una cantidad fija. |
| [!UICONTROL Adjustment Amount] | Requerido.<br>Si elige  `Apply as percentage` para  **[!UICONTROL Apply]**, introduzca el valor de porcentaje (ejemplo: introduzca  `25` para un ajuste del 25 %).<br>Si elige  `Apply as fixed amount` para  **[!UICONTROL Apply]**, introduzca el valor numérico de la cantidad fija (ejemplo: introduzca  `25` para un ajuste fijo de 25 $). |
