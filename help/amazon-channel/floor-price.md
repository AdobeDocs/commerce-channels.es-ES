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

La variable [precio mínimo](./floor-price.md) proteja automáticamente su precio de producto más bajo contra las reglas de precios inteligentes. Utilice esta configuración para establecer un mínimo (precio más bajo) para sus reglas de precios inteligentes, asegurándose de que los productos no se listen por debajo del precio deseado.

Los atributos de precio mínimo se basan en el ámbito del sitio web si su [!DNL Commerce] la tienda utiliza el ámbito de precios del sitio web. Consulte [Alcance del precio](./price-scope.md).

El precio del piso solo se usa cuando **[!UICONTROL Rule Type]** está configurado como `Intelligent repricing rule`.

## Configurar el precio mínimo

Defina la configuración de precio más baja en la variable _[!UICONTROL Floor Price]_para obtener más información.

1. Para **[!UICONTROL Floor Price Source]**, elija un atributo de origen de precio.

   Elija la [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica su límite de piso relativo. Por ejemplo, si no desea que el precio de su anuncio de Amazon sea inferior al coste de su artículo, debe elegir la *Costo* atributo.

1. Para **[!UICONTROL Floor Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que se defina _[!UICONTROL Floor Price Source]_para ajustar hacia abajo, creando un precio mínimo para la regla, antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se defina _[!UICONTROL Floor Price Source]_para ajustar, creando un precio mínimo más alto para la regla, antes de cotizar en Amazon.

   - `Match` - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del valor definido _[!UICONTROL Floor Price Source]_valor. Cuando se configura como `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_los campos están desactivados.

1. Deje el **[!UICONTROL Apply]** default como `Apply as percentage`.

1. Para **[!UICONTROL Floor Adjustment Price]**, introduzca el valor numérico del porcentaje para ajustar el _[!UICONTROL Floor Price Source]_valor.

En este ejemplo, el precio mínimo se establece en un 3 % por encima del coste del artículo.

![Ejemplo de regla de reprecio inteligente: precio mínimo](assets/ob-intelligent-pricde-rule-floor-price.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Floor Price Source] | Elija la [!DNL Commerce] que indica su límite mínimo relativo (precio más bajo). Por ejemplo, si no desea que el precio de su anuncio de Amazon sea inferior al coste de su artículo, debe elegir la `Cost` atributo. |
| [!UICONTROL Floor Price Action] | Elija una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina _[!UICONTROL Floor Price Source]_para ajustar hacia abajo, creando un precio mínimo para la regla, antes de cotizar en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina _[!UICONTROL Floor Price Source]_para ajustar, creando un precio mínimo más alto para la regla, antes de cotizar en Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio del anuncio fluctúe por debajo del valor definido _[!UICONTROL Floor Price Source]_valor. Si se elige, la variable_[!UICONTROL Apply]_ y _[!UICONTROL Floor Adjustment Amount]_los campos están desactivados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual en relación con la variable _[!UICONTROL Floor Price Source]_valor. |
| [!UICONTROL Floor Adjustment Amount] | Introduzca el valor numérico del porcentaje para ajustar el _[!UICONTROL Floor Price Source]_valor. |
