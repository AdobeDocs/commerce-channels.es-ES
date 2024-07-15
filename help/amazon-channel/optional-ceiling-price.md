---
title: "Regla de reasignación inteligente: precio de techo opcional"
description: Utiliza la configuración opcional de precios máximos para proteger el precio más alto del producto contra las reglas inteligentes de precios que administran tus anuncios de Amazon.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
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

Defina la configuración opcional de precios más altos en la sección _[!UICONTROL Optional Ceiling Price]_.

1. Para **[!UICONTROL Ceiling Price Source]**, elija un atributo.

   Seleccione el [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica el límite máximo relativo. Por ejemplo, si no desea que el precio del anuncio de Amazon supere el precio MSRP del artículo, elegiría el atributo `Manufacturer's Suggested Retail Price`.

1. Para **[!UICONTROL Ceiling Price Action]**, elija una opción.

   - `Decrease By`: elija cuándo desea que se ajuste el valor _[!UICONTROL Ceiling Price Source]_definido, lo que crea un precio máximo más bajo para la regla, antes de ponerla en venta en Amazon.

   - `Increase By`: elija cuándo desea que se ajuste el valor de _[!UICONTROL Ceiling Price Source]_definido, lo que crea un precio máximo más alto para la regla, antes de ponerla en venta en Amazon.

   - `Match`: elija cuándo no desea que el precio del listado fluctúe por encima del valor de _[!UICONTROL Ceiling Price Source]_definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_están deshabilitados.

1. Deje **[!UICONTROL Apply]** como predeterminado `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, escriba el valor numérico del porcentaje para ajustar el valor de _[!UICONTROL Ceiling Price Source]_.

En este ejemplo, el precio máximo se establece en un 2 % por debajo del MSRP del artículo.

![Regla de reasignación de precios inteligente - precio máximo opcional](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Campo | Descripción |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Elija el [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica su límite máximo relativo. Por ejemplo, si no desea que el precio de la lista de productos supere el precio MSRP del artículo, elija el atributo `Manufacturer's Suggested Retail Price`. |
| [!UICONTROL Ceiling Price Action] | Seleccione una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]**: elija cuándo desea que se ajuste el valor _[!UICONTROL Ceiling Price Source]_definido, lo que crea un precio máximo más bajo para la regla, antes de ponerla en venta en Amazon.</li><li>**[!UICONTROL Increase By]**: elija cuándo desea que se ajuste el valor de _[!UICONTROL Ceiling Price Source]_definido, lo que crea un precio máximo más alto para la regla, antes de ponerla en venta en Amazon.</li><li>**[!UICONTROL Match]**: elija cuándo no desea que el precio del listado fluctúe por encima del valor de _[!UICONTROL Ceiling Price Source]_definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_están deshabilitados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**: un ajuste porcentual relativo al valor _[!UICONTROL Ceiling Price Source]_. |
| [!UICONTROL Ceiling Price Adjustment] | Escriba el valor numérico del porcentaje para ajustar el valor _[!UICONTROL Ceiling Price Source]_. |
