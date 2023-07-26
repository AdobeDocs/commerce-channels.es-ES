---
title: "Regla de reasignación inteligente: precio de techo opcional"
description: Utiliza la configuración opcional de precios máximos para proteger el precio más alto del producto contra las reglas inteligentes de precios que administran tus anuncios de Amazon.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Regla de reasignación inteligente: precio de techo opcional

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [Seleccionar tipo de regla](./intelligent-repricing-rules.md)
- [Variaciones condicionales del competidor](./competitor-conditional-variances.md)
- [Ajuste de precio](./price-adjustment.md)
- [Precio mínimo](./floor-price.md)
- Precio de techo opcional

La configuración automatizada de precios máximos protege automáticamente el precio más alto del producto contra las reglas inteligentes de precios, lo que le permite establecer un límite (precio más alto) para sus reglas inteligentes de precios.

## Configurar el precio máximo opcional

Defina la configuración de precio más alto opcional en la _[!UICONTROL Optional Ceiling Price]_sección.

1. Para **[!UICONTROL Ceiling Price Source]**, elija un atributo.

   Seleccione su [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica el límite máximo relativo. Por ejemplo, si no quieres que el precio de tu anuncio de Amazon supere el precio MSRP de tu artículo, elige la opción `Manufacturer's Suggested Retail Price` atributo.

1. Para **[!UICONTROL Ceiling Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que se defina el _[!UICONTROL Ceiling Price Source]_valor que se va a ajustar hacia abajo, creando un precio máximo más bajo para la regla, antes de añadirlo a Amazon.

   - `Increase By` - Elija cuándo desea que se defina el _[!UICONTROL Ceiling Price Source]_valor que se debe ajustar, lo que crea un precio máximo más alto para la regla, antes de ponerlo en venta en Amazon.

   - `Match` - Elija cuándo no desea que el precio de la lista fluctúe por encima del valor definido _[!UICONTROL Ceiling Price Source]_valor. Cuando se establece en `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_Los campos de están desactivados.

1. Deje el **[!UICONTROL Apply]** predeterminado como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, introduzca el valor numérico para el porcentaje para ajustar el _[!UICONTROL Ceiling Price Source]_valor.

En este ejemplo, el precio máximo se establece en un 2 % por debajo del MSRP del artículo.

![Regla de reasignación de precios inteligente: precio máximo opcional](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Campo | Descripción |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Elija la [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica el límite máximo relativo. Por ejemplo, si no desea que el precio de la lista de productos supere el precio MSRP del artículo, elija la opción `Manufacturer's Suggested Retail Price` atributo. |
| [!UICONTROL Ceiling Price Action] | Seleccione una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina el _[!UICONTROL Ceiling Price Source]_valor que se va a ajustar hacia abajo, creando un precio máximo más bajo para la regla, antes de añadirlo a Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina el _[!UICONTROL Ceiling Price Source]_valor que se debe ajustar, lo que crea un precio máximo más alto para la regla, antes de ponerlo en venta en Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio de la lista fluctúe por encima del valor definido _[!UICONTROL Ceiling Price Source]_valor. Cuando se establece en `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_Los campos de están desactivados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual en relación con el _[!UICONTROL Ceiling Price Source]_valor. |
| [!UICONTROL Ceiling Price Adjustment] | Introduzca el valor numérico para el porcentaje para ajustar su _[!UICONTROL Ceiling Price Source]_valor. |
