---
title: '''Regla de reprecio inteligente: Precio máximo opcional"'
description: Utilice la configuración opcional de precios máximos para proteger el precio más alto del producto contra las reglas de precios inteligentes que administran sus anuncios de Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Regla de reprecio inteligente: precio máximo opcional

Las secciones de una regla de reasignación de precios inteligente incluyen:

- [Seleccionar tipo de regla](./intelligent-repricing-rules.md)
- [Variaciones condicionales de la competencia](./competitor-conditional-variances.md)
- [Ajuste de precio](./price-adjustment.md)
- [Precio mínimo](./floor-price.md)
- Precio máximo opcional

La configuración automatizada de precios máximos protege automáticamente su precio de producto más alto contra las reglas de precios inteligentes, lo que le permite establecer un techo (precio más alto) para sus reglas de precios inteligentes.

## Configurar el precio máximo opcional

Defina la configuración de precio más alto opcional en la sección _[!UICONTROL Optional Ceiling Price]_.

1. Para **[!UICONTROL Ceiling Price Source]**, elija un atributo.

   Seleccione su [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} que indica su límite máximo relativo. Por ejemplo, si no desea que el precio de su anuncio de Amazon sea superior al MSRP de su artículo, elegirá el atributo `Manufacturer's Suggested Retail Price`.

1. Para **[!UICONTROL Ceiling Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que el  _[!UICONTROL Ceiling Price Source]_valor definido se ajuste hacia abajo, lo que crea un precio límite inferior para la regla, antes de añadirla a Amazon.

   - `Increase By` - Elija cuándo desea que se ajuste el  _[!UICONTROL Ceiling Price Source]_valor definido, creando un precio máximo más alto para la regla, antes de añadirla a Amazon.

   - `Match` - Elija cuándo no desea que el precio del anuncio fluctúe por encima del  _[!UICONTROL Ceiling Price Source]_valor definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_se desactivan.

1. Deje el **[!UICONTROL Apply]** predeterminado como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, introduzca el valor numérico del porcentaje para ajustar su valor _[!UICONTROL Ceiling Price Source]_.

En este ejemplo, el precio máximo se establece en un 2 % por debajo del MSRP del artículo.

![Regla de revalorización inteligente: precio máximo opcional](assets/ob-intelligent-price-rule-ceiling.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Ceiling Price Source] | Elija el [!DNL Commerce] [atributo del producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} que indica su límite máximo relativo. Por ejemplo, si no desea que el precio de la lista de productos sea superior al MSRP de su artículo, elegirá el atributo `Manufacturer's Suggested Retail Price`. |
| [!UICONTROL Ceiling Price Action] | Elija una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que el  _[!UICONTROL Ceiling Price Source]_valor definido se ajuste hacia abajo, lo que crea un precio límite inferior para la regla, antes de añadirla a Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se ajuste el  _[!UICONTROL Ceiling Price Source]_valor definido, creando un precio máximo más alto para la regla, antes de añadirla a Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio del anuncio fluctúe por encima del  _[!UICONTROL Ceiling Price Source]_valor definido. Cuando se establece en `Match`, los campos_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_se desactivan.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual relativo al  _[!UICONTROL Ceiling Price Source]_valor. |
| [!UICONTROL Ceiling Price Adjustment] | Introduzca el valor numérico del porcentaje para ajustar su valor _[!UICONTROL Ceiling Price Source]_. |
