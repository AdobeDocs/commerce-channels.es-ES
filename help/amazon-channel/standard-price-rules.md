---
title: Acciones de regla de precio estándar
description: Utilice acciones de regla de precio estándar para aumentar o reducir un precio de listado de Amazon en relación con el precio del catálogo de Commerce (o la fuente de precios).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Acciones de regla de precio estándar

Una acción de regla de precio estándar permite aumentar o reducir el precio de un anuncio de Amazon en un porcentaje específico o en una cantidad en dólares fijos en relación con el [!DNL Commerce] precio de catálogo (o fuente de precios).

Las secciones de una acción de regla de precio estándar incluyen:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configuración de acciones de regla de precios

1. Para **[!UICONTROL Rule Type]**, elija `Standard price rule`.

   Esta opción deshabilita los demás campos del _[!UICONTROL Select Rule Type]_sección.

1. Expanda el _[!UICONTROL Price Adjustment]_, si es necesario.

1. Para **[!UICONTROL Price Action]**, elija una opción para determinar cómo desea cambiar el *[!UICONTROL Magento Price Source]* (definido en su [Precio del anuncio](./listing-price.md)) valor.

   - `Decrease By` : elige cuándo quieres reducir el valor antes de ponerlo en venta en Amazon.

   - `Increase By` : elige cuándo quieres aumentar el valor antes de ponerlo en venta en Amazon.

1. Para **[!UICONTROL Apply]**, elija una opción y una opción para determinar cómo desea que se definan las *[!UICONTROL Magento Price Source]* definido en su [Precio del anuncio](./listing-price.md) valor que debe ajustarse:

   - `Apply as percentage` - Elija cuándo desea que se defina el *[!UICONTROL Magento Price Source]* definido en su [Precio del anuncio](./listing-price.md) valor ajustado en porcentaje

   - `Apply as fixed amount` - Elija cuándo desea que se defina el *[!UICONTROL Magento Price Source]* definido en su [Precio del anuncio](./listing-price.md) valor ajustado en una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - Cuándo *[!UICONTROL Apply]* se establece en `Apply as percentage`, introduzca el valor porcentual (por ejemplo: introduzca `25` para un ajuste de precio del 25%).

   - Cuándo *[!UICONTROL Apply]* se establece en `Apply as fixed amount`, introduzca el valor numérico para el importe fijo (por ejemplo: introduzca `25` para un ajuste de precio fijo de 25 dólares).

1. Cuando termine, haga clic en **[!UICONTROL Save pricing rule]**.

![Regla de precio estándar](assets/ob-price-rule-action-standard-example.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Rule Type] | Seleccionar `Standard price rule`. |
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina el [!DNL Commerce] el valor de origen del precio debe reducirse antes de ponerlo en venta en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina el [!DNL Commerce] el valor de la fuente de precios debe aumentarse antes de añadirse a Amazon.</li></ul> |
| [!UICONTROL Apply] | Opciones:<ul><li>**[!UICONTROL Apply as percentage]** - Elija cuándo desea que se defina el [!DNL Commerce] valor fuente del precio ajustado en un porcentaje.</li><li>**[!UICONTROL Apply as fixed amount]** - Elija cuándo desea que se defina el [!DNL Commerce] valor fuente del precio ajustado por un importe fijo.</li></ul> |
| [!UICONTROL Adjustment Amount] | Requerido.<br><br>Si elige `Apply as percentage` para *[!UICONTROL Apply]*, introduzca el valor porcentual (por ejemplo: introduzca `25` para un ajuste del 25%).<br><br>Si elige `Apply as fixed amount` para *[!UICONTROL Apply]*, introduzca el valor numérico para el importe fijo (por ejemplo: introduzca `25` para un ajuste fijo de 25 dólares). |
