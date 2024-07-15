---
title: 'Canal de ventas de Amazon: acciones de regla de precio estándar'
description: Utilice acciones de regla de precio estándar para aumentar o reducir un precio de listado de Amazon en relación con el precio de catálogo de Commerce (o el origen de precios).
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Acciones de regla de precio estándar

Una acción de regla de precio estándar le permite aumentar o reducir un precio de listado de Amazon en un porcentaje específico o en una cantidad fija en dólares en relación con el precio de catálogo [!DNL Commerce] (o el origen del precio).

Las secciones de una acción de regla de precio estándar incluyen:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configuración de acciones de regla de precios

1. Para **[!UICONTROL Rule Type]**, elija `Standard price rule`.

   Esta opción deshabilita los demás campos de la sección _[!UICONTROL Select Rule Type]_.

1. Expanda la sección _[!UICONTROL Price Adjustment]_si es necesario.

1. Para **[!UICONTROL Price Action]**, elige una opción para determinar cómo deseas cambiar el valor de *[!UICONTROL Magento Price Source]* (definido en tu [precio del anuncio](./listing-price.md)).

   - `Decrease By`: elige cuándo quieres reducir el valor antes de ponerlo en venta en Amazon.

   - `Increase By`: elige cuándo quieres aumentar el valor antes de ponerlo en venta en Amazon.

1. Para **[!UICONTROL Apply]**, elige una opción para determinar cómo deseas que se ajuste el valor *[!UICONTROL Magento Price Source]* definido en tu [precio de anuncio](./listing-price.md):

   - `Apply as percentage`: elige cuándo quieres que el valor definido de *[!UICONTROL Magento Price Source]* en el [precio del anuncio](./listing-price.md) se ajuste en un porcentaje

   - `Apply as fixed amount`: elige cuándo quieres que el valor de *[!UICONTROL Magento Price Source]* definido en el [precio del anuncio](./listing-price.md) se ajuste en una cantidad fija.

1. Para **[!UICONTROL Adjustment Amount]** (obligatorio), introduzca el valor numérico para el ajuste de precio.

   - Cuando *[!UICONTROL Apply]* esté establecido en `Apply as percentage`, escriba el valor porcentual (por ejemplo: escriba `25` para un ajuste de precio del 25%).

   - Cuando *[!UICONTROL Apply]* se establezca en `Apply as fixed amount`, escriba el valor numérico para el importe fijo (ejemplo: escriba `25` para un ajuste de precio fijo de 25 $).

1. Una vez finalizado, haga clic en **[!UICONTROL Save pricing rule]**.

![Regla de precio estándar](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | Seleccione `Standard price rule`. |
| [!UICONTROL Price Action] | Opciones:<ul><li>**[!UICONTROL Decrease By]**: elige cuándo quieres que disminuya el valor de origen de precio de [!DNL Commerce] definido antes de ponerlo en venta en Amazon.</li><li>**[!UICONTROL Increase By]**: elige cuándo quieres que aumente el valor de origen de precio de [!DNL Commerce] definido antes de ponerlo en venta en Amazon.</li></ul> |
| [!UICONTROL Apply] | Opciones:<ul><li>**[!UICONTROL Apply as percentage]**: elija cuándo desea que el valor de origen de precio [!DNL Commerce] definido se ajuste en un porcentaje.</li><li>**[!UICONTROL Apply as fixed amount]**: elija cuándo desea que el valor de origen de precio [!DNL Commerce] definido se ajuste en una cantidad fija.</li></ul> |
| [!UICONTROL Adjustment Amount] | Requerido.<br><br>Si elige `Apply as percentage` para *[!UICONTROL Apply]*, escriba el valor porcentual (por ejemplo: escriba `25` para un ajuste porcentual del 25%).<br><br>Si elige `Apply as fixed amount` para *[!UICONTROL Apply]*, escriba el valor numérico para el importe fijo (ejemplo: escriba `25` para un ajuste fijo de 25 $). |
