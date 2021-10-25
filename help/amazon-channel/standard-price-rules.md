---
title: Acciones de regla de precio estándar
description: Utilice acciones de reglas de precios estándar para aumentar o reducir un precio de anuncio de Amazon en relación con el precio del catálogo de comercio (o la fuente de precios).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Acciones de reglas de precio estándar

Una acción de regla de precio estándar le permite aumentar o reducir un precio de anuncio de Amazon en un porcentaje específico o una cantidad de dólares fija en relación con el [!DNL Commerce] precio de catálogo (o fuente de precio).

Las secciones de una acción de regla de precio estándar incluyen:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configurar acciones de reglas de precio

1. Para **[!UICONTROL Rule Type]**, elija `Standard price rule`.

   Esta opción deshabilita los demás campos de la variable _[!UICONTROL Select Rule Type]_para obtener más información.

1. Expanda el _[!UICONTROL Price Adjustment]_, si es necesario.

1. Para **[!UICONTROL Price Action]**, elija una opción para determinar cómo desea cambiar la variable *[!UICONTROL Magento Price Source]* (definida en el [Precio de anuncio](./listing-price.md)).

   - `Decrease By` - Elija cuándo desea que el valor se reduzca antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se aumente el valor antes de añadirlo a Amazon.

1. Para **[!UICONTROL Apply]**, elija una opción para determinar cómo desea que se defina la variable *[!UICONTROL Magento Price Source]* definida en [Precio de anuncio](./listing-price.md) valor que se va a ajustar:

   - `Apply as percentage` - Elija cuándo desea que se defina *[!UICONTROL Magento Price Source]* definida en [Precio de anuncio](./listing-price.md) valor ajustado en porcentaje

   - `Apply as fixed amount` - Elija cuándo desea que se defina *[!UICONTROL Magento Price Source]* definida en [Precio de anuncio](./listing-price.md) valor ajustado por una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - When *[!UICONTROL Apply]* está configurado como `Apply as percentage`, introduzca el valor de porcentaje (ejemplo: enter `25` para un ajuste de precio del 25%).

   - When *[!UICONTROL Apply]* está configurado como `Apply as fixed amount`, introduzca el valor numérico de la cantidad fija (ejemplo: enter `25` para un ajuste de precio fijo de 25 dólares).

1. Cuando termine, haga clic en **[!UICONTROL Save pricing rule]**.

![Regla de precio estándar](assets/ob-price-rule-action-standard-example.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Rule Type] | Select `Standard price rule`. |
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina [!DNL Commerce] el valor de la fuente de precios se reducirá antes de cotizar en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina [!DNL Commerce] el valor de la fuente de precios se aumentará antes de publicarlo en Amazon.</li></ul> |
| [!UICONTROL Apply] | Opciones:<ul><li>**[!UICONTROL Apply as percentage]** - Elija cuándo desea que se defina [!DNL Commerce] valor de fuente de precios ajustado en un porcentaje.</li><li>**[!UICONTROL Apply as fixed amount]** - Elija cuándo desea que se defina [!DNL Commerce] valor de origen de precio ajustado por una cantidad fija.</li></ul> |
| [!UICONTROL Adjustment Amount] | Requerido.<br><br>Si elige `Apply as percentage` para *[!UICONTROL Apply]*, introduzca el valor de porcentaje (ejemplo: enter `25` para un ajuste del 25%).<br><br>Si elige `Apply as fixed amount` para *[!UICONTROL Apply]*, introduzca el valor numérico de la cantidad fija (ejemplo: enter `25` para un ajuste fijo de 25 dólares). |
