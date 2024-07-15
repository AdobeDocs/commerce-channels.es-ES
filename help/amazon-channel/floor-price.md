---
title: "Regla de reasignación inteligente: precio mínimo"
description: Utiliza la configuración de precios mínimos para determinar el precio más bajo de una regla de precios inteligente para administrar tus anuncios de Amazon.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Regla de reasignación inteligente: precio mínimo

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

La configuración del [precio mínimo](./floor-price.md) protege automáticamente el precio más bajo del producto contra las reglas inteligentes de precios. Utilice esta configuración para establecer un piso (precio más bajo) para sus reglas inteligentes de precios, asegurándose de que sus productos no aparezcan por debajo del precio deseado.

Los atributos del precio mínimo se basan en el ámbito del sitio web si la tienda [!DNL Commerce] utiliza el ámbito de precios del sitio web. Ver [Precios](./price-scope.md).

El precio mínimo solo se usa cuando **[!UICONTROL Rule Type]** está establecido en `Intelligent repricing rule`.

## Configurar precio mínimo

Defina el precio más bajo en la sección _[!UICONTROL Floor Price]_.

1. Para **[!UICONTROL Floor Price Source]**, elija un atributo de origen de precio.

   Elija el [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) que indica su límite mínimo relativo. Por ejemplo, si no quieres que el precio de tu anuncio de Amazon sea inferior al coste del artículo, elige el atributo *Coste*.

1. Para **[!UICONTROL Floor Price Action]**, elija una opción.

   - `Decrease By`: elija cuándo desea que se ajuste el valor _[!UICONTROL Floor Price Source]_definido, lo que crea un precio mínimo más bajo para la regla, antes de ponerla en venta en Amazon.

   - `Increase By`: elige cuándo quieres que se ajuste el valor de _[!UICONTROL Floor Price Source]_definido, lo que crea un precio mínimo más alto para la regla, antes de ponerla en venta en Amazon.

   - `Match`: elige si no deseas que el precio del anuncio fluctúe por debajo del valor de _[!UICONTROL Floor Price Source]_definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_están deshabilitados.

1. Deje **[!UICONTROL Apply]** como predeterminado `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, escriba el valor numérico del porcentaje para ajustar el valor de _[!UICONTROL Floor Price Source]_.

En este ejemplo, el precio mínimo se establece en un 3 % por encima del coste del artículo.

![Ejemplo de regla de reasignación de precios inteligente - precio mínimo](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Elija el atributo [!DNL Commerce] que indica el límite mínimo relativo (precio más bajo). Por ejemplo, si no quieres que el precio del anuncio de Amazon sea inferior al coste del artículo, elige el atributo `Cost`. |
| [!UICONTROL Floor Price Action] | Seleccione una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]**: elija cuándo desea que se ajuste el valor _[!UICONTROL Floor Price Source]_definido, lo que crea un precio mínimo más bajo para la regla, antes de ponerla en venta en Amazon.</li><li>**[!UICONTROL Increase By]**: elige cuándo quieres que se ajuste el valor de _[!UICONTROL Floor Price Source]_definido, lo que crea un precio mínimo más alto para la regla, antes de ponerla en venta en Amazon.</li><li>**[!UICONTROL Match]**: elige si no deseas que el precio del anuncio fluctúe por debajo del valor de _[!UICONTROL Floor Price Source]_definido. Cuando se elige, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_se desactivan.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**: un ajuste porcentual relativo al valor _[!UICONTROL Floor Price Source]_. |
| [!UICONTROL Floor Adjustment Amount] | Escriba el valor numérico del porcentaje para ajustar el valor _[!UICONTROL Floor Price Source]_. |
