---
title: "Regla de reasignación inteligente: precio mínimo"
description: Utiliza la configuración de precios mínimos para determinar el precio más bajo de una regla de precios inteligente para administrar tus anuncios de Amazon.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Regla de reasignación inteligente: precio mínimo

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

El [precio mínimo](./floor-price.md) la configuración protege automáticamente el precio más bajo del producto contra las reglas inteligentes de precios. Utilice esta configuración para establecer un piso (precio más bajo) para sus reglas inteligentes de precios, asegurándose de que sus productos no aparezcan por debajo del precio deseado.

Los atributos del precio mínimo se basan en el ámbito del sitio web si su [!DNL Commerce] la tienda utiliza el ámbito de precios del sitio web. Consulte [Precios y alcance](./price-scope.md).

El precio mínimo solo se usa cuando **[!UICONTROL Rule Type]** se establece en `Intelligent repricing rule`.

## Configurar precio mínimo

Defina la configuración de precio más bajo en la _[!UICONTROL Floor Price]_sección.

1. Para **[!UICONTROL Floor Price Source]**, elija un atributo de fuente de precios.

   Elija la [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica su límite mínimo relativo. Por ejemplo, si no quieres que el precio de tu anuncio de Amazon sea inferior al coste del artículo, elige la opción *Coste* atributo.

1. Para **[!UICONTROL Floor Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que se defina el _[!UICONTROL Floor Price Source]_valor que se debe ajustar hacia abajo, lo que crea un precio mínimo más bajo para la regla, antes de ponerlo en venta en Amazon.

   - `Increase By` - Elija cuándo desea que se defina el _[!UICONTROL Floor Price Source]_valor que se debe ajustar, lo que crea un precio mínimo más alto para la regla, antes de ponerlo en venta en Amazon.

   - `Match` - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del valor definido _[!UICONTROL Floor Price Source]_valor. Cuando se establece en `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_Los campos de están desactivados.

1. Deje el **[!UICONTROL Apply]** predeterminado como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, introduzca el valor numérico para el porcentaje para ajustar el _[!UICONTROL Floor Price Source]_valor.

En este ejemplo, el precio mínimo se establece en un 3 % por encima del coste del artículo.

![Ejemplo de regla de reasignación de precios inteligente: precio mínimo](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Elija la [!DNL Commerce] atributo que indica el límite mínimo relativo (precio más bajo). Por ejemplo, si no quieres que el precio de tu anuncio de Amazon sea inferior al coste del artículo, elige la opción `Cost` atributo. |
| [!UICONTROL Floor Price Action] | Seleccione una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina el _[!UICONTROL Floor Price Source]_valor que se debe ajustar hacia abajo, lo que crea un precio mínimo más bajo para la regla, antes de ponerlo en venta en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina el _[!UICONTROL Floor Price Source]_valor que se debe ajustar, lo que crea un precio mínimo más alto para la regla, antes de ponerlo en venta en Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del valor definido _[!UICONTROL Floor Price Source]_valor. Cuando se elige, la variable_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_Los campos de están desactivados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual en relación con el _[!UICONTROL Floor Price Source]_valor. |
| [!UICONTROL Floor Adjustment Amount] | Introduzca el valor numérico para el porcentaje para ajustar su _[!UICONTROL Floor Price Source]_valor. |
