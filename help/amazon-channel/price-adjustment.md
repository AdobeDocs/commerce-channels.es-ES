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
>La sección Ajuste de precio difiere ligeramente para las reglas de reasignación de precios estándar e inteligentes. **[!UICONTROL Match Competitor Price]** solo está disponible en _[!UICONTROL Price Action]_when **[!UICONTROL Rule Type]**está configurado como `Intelligent repricing rule`.

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [Seleccionar tipo de regla](./intelligent-repricing-rules.md)
- [Variaciones condicionales de la competencia](./competitor-conditional-variances.md)
- Ajuste de precio
- [Precio mínimo](./floor-price.md)
- [Precio máximo opcional](./optional-ceiling-price.md)

El ajuste de precio define el cálculo de precio cuando ha identificado la fuente de precios del competidor.

## Configurar el ajuste de precio

Defina su ajuste de precios en la variable _[!UICONTROL Price Adjustment]_para obtener más información.

1. Para **[!UICONTROL Price Action]**, elija una opción:

   - `Decrease By` - Elija cuándo desea que el valor de origen de precio definido se ajuste hacia abajo, lo que crea un precio más bajo para la regla, antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se ajuste el valor de la fuente de precios definido, lo que crea un precio más alto para la regla, antes de cotizar en Amazon.

   - `Match Competitor Price` - (Solo regla de reasignación inteligente) Elija cuándo desea cambiar el precio de su anuncio de Amazon para que coincida con el [competidor más bajo](./lowest-competitor-pricing.md) en función de los comentarios de su competidor y los parámetros de varianza. Cuando se configura como `Match Competitor Price`, el _[!UICONTROL Apply]_y_[!UICONTROL Adjustment Amount]_ se eliminan los campos.

1. Para **[!UICONTROL Apply]**, elija una opción:

   - `Apply as percentage` - Elija cuándo desea que se defina **[!UICONTROL Magento Price Source]** definida en [Precio de anuncio](./listing-price.md) ajustado en un porcentaje.

   - `Apply as fixed amount` - Elija cuándo desea que se defina **[!UICONTROL Magento Price Source]** definida en [Precio de anuncio](./listing-price.md) ajustado por una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - When **[!UICONTROL Apply]** está configurado como `Apply as percentage`, introduzca el valor de porcentaje (ejemplo: enter `25` para un ajuste del 25%).

   - When **[!UICONTROL Apply]** está configurado como `Apply as fixed amount`, introduzca el valor numérico de la cantidad fija (ejemplo: enter `25` para un ajuste fijo de 25 dólares).

![Regla de revalorización inteligente: ajuste de precio](assets/amazon-price-adjustment.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Price Action] | Elija una acción de ajuste de precios. Opciones:<br>**[!UICONTROL Decrease By]**- Elija cuándo desea que se defina _[!UICONTROL Magento Price Source]_definida en [Precio de anuncio](./listing-price.md) para ajustar hacia abajo, creando un precio más bajo para la regla, antes de cotizar en Amazon.<br>**[!UICONTROL Increase By]**- Elija cuándo desea que se defina_[!UICONTROL Magento Price Source]_ definida en [Precio de anuncio](./listing-price.md) para ajustar, creando un precio más alto para la regla, antes de cotizar en Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Solo regla de reasignación inteligente) Elija cuándo desea cambiar el precio de su anuncio de Amazon para que coincida con el [competidor más bajo](./lowest-competitor-pricing.md) en función de los comentarios de su competidor y los parámetros de varianza. Si se elige, la variable _Aplicar_ y _Importe de ajuste_ se eliminan los campos. |
| [!UICONTROL Apply] | Opciones:<br>**[!UICONTROL Apply as percentage]**- Elija cuándo desea que se defina _[!UICONTROL Magento Price Source]_definida en [Precio de anuncio](./listing-price.md) ajustado en un porcentaje.<br>**[!UICONTROL Apply as fixed amount]**- Elija cuándo desea que se defina_[!UICONTROL Magento Price Source]_ definida en [Precio de anuncio](./listing-price.md) ajustado por una cantidad fija. |
| [!UICONTROL Adjustment Amount] | Requerido.<br>Si elige `Apply as percentage` para **[!UICONTROL Apply]**, introduzca el valor de porcentaje (ejemplo: enter `25` para un ajuste del 25%).<br>Si elige `Apply as fixed amount` para **[!UICONTROL Apply]**, introduzca el valor numérico de la cantidad fija (ejemplo: enter `25` para un ajuste fijo de 25 dólares). |
