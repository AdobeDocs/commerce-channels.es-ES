---
title: '''Regla de reprecio inteligente: Precio piso'''
description: Use la configuración de precios mínimos para determinar el precio más bajo de una regla de precios inteligente para administrar sus anuncios de Amazon.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Regla de reprecio inteligente: precio mínimo

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

La configuración de [precio mínimo](./floor-price.md) protege automáticamente el precio más bajo del producto frente a las reglas de precios inteligentes. Utilice esta configuración para establecer un mínimo (precio más bajo) para sus reglas de precios inteligentes, asegurándose de que los productos no se listen por debajo del precio deseado.

Los atributos de precio del piso se basan en el ámbito del sitio web si su tienda [!DNL Commerce] está usando el ámbito de precios del sitio web. Consulte [Alcance del precio](./price-scope.md).

El precio del piso solo se usa cuando **[!UICONTROL Rule Type]** está establecido en `Intelligent repricing rule`.

## Configurar el precio mínimo

Defina la configuración de precio más baja en la sección _[!UICONTROL Floor Price]_.

1. Para **[!UICONTROL Floor Price Source]**, elija un atributo de origen de precio.

   Elija el [!DNL Commerce] [atributo del producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica su límite inferior relativo. Por ejemplo, si no desea que el precio del anuncio de Amazon sea inferior al coste del artículo, debe elegir el atributo *Cost*.

1. Para **[!UICONTROL Floor Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que el  _[!UICONTROL Floor Price Source]_valor definido se ajuste hacia abajo, creando un precio mínimo para la regla, antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se ajuste el  _[!UICONTROL Floor Price Source]_valor definido, creando un precio mínimo más alto para la regla, antes de cotizar en Amazon.

   - `Match` - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del  _[!UICONTROL Floor Price Source]_valor definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_se desactivan.

1. Deje el **[!UICONTROL Apply]** predeterminado como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, introduzca el valor numérico del porcentaje para ajustar su valor _[!UICONTROL Floor Price Source]_.

En este ejemplo, el precio mínimo se establece en un 3 % por encima del coste del artículo.

![Ejemplo de regla de reprecio inteligente: precio mínimo](assets/ob-intelligent-pricde-rule-floor-price.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Floor Price Source] | Elija el atributo [!DNL Commerce] que indica su límite inferior relativo. Por ejemplo, si no desea que el precio del anuncio de Amazon sea inferior al coste del artículo, debe elegir el atributo `Cost`. |
| [!UICONTROL Floor Price Action] | Elija una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que el  _[!UICONTROL Floor Price Source]_valor definido se ajuste hacia abajo, creando un precio mínimo para la regla, antes de cotizar en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se ajuste el  _[!UICONTROL Floor Price Source]_valor definido, creando un precio mínimo más alto para la regla, antes de cotizar en Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del  _[!UICONTROL Floor Price Source]_valor definido. Cuando se elige, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_se desactivan.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual relativo al  _[!UICONTROL Floor Price Source]_valor. |
| [!UICONTROL Floor Adjustment Amount] | Introduzca el valor numérico del porcentaje para ajustar su valor _[!UICONTROL Floor Price Source]_. |
