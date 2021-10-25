---
title: '''Regla de reprecio inteligente: Precio máximo opcional"'
description: Utilice la configuración opcional de precios máximos para proteger el precio más alto del producto contra las reglas de precios inteligentes que administran sus anuncios de Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
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

Defina la configuración de precio más alto opcional en la variable _[!UICONTROL Optional Ceiling Price]_para obtener más información.

1. Para **[!UICONTROL Ceiling Price Source]**, elija un atributo.

   Seleccione su [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica su límite de límite relativo. Por ejemplo, si no desea que el precio de su anuncio de Amazon sea superior al MSRP de su artículo, elegirá el `Manufacturer's Suggested Retail Price` atributo.

1. Para **[!UICONTROL Ceiling Price Action]**, elija una opción.

   - `Decrease By` - Elija cuándo desea que se defina _[!UICONTROL Ceiling Price Source]_para ajustar hacia abajo, lo que crea un precio máximo más bajo para la regla, antes de cotizar en Amazon.

   - `Increase By` - Elija cuándo desea que se defina _[!UICONTROL Ceiling Price Source]_para ajustar, lo que crea un precio máximo más alto para la regla, antes de añadirla a Amazon.

   - `Match` - Elija cuándo no desea que el precio del anuncio fluctúe por encima del valor definido _[!UICONTROL Ceiling Price Source]_valor. Cuando se configura como `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_los campos están desactivados.

1. Deje el **[!UICONTROL Apply]** default como `Apply as percentage`.

1. Para **[!UICONTROL Ceiling Adjustment Price]**, introduzca el valor numérico del porcentaje para ajustar el _[!UICONTROL Ceiling Price Source]_valor.

En este ejemplo, el precio máximo se establece en un 2 % por debajo del MSRP del artículo.

![Regla de revalorización inteligente: precio máximo opcional](assets/ob-intelligent-price-rule-ceiling.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Ceiling Price Source] | Elija la [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} que indica su límite de límite relativo. Por ejemplo, si no desea que el precio de la lista de productos sea superior al MSRP de su artículo, elegirá la variable `Manufacturer's Suggested Retail Price` atributo. |
| [!UICONTROL Ceiling Price Action] | Elija una acción de ajuste de precios. Opciones:<ul><li>**[!UICONTROL Decrease By]** - Elija cuándo desea que se defina _[!UICONTROL Ceiling Price Source]_para ajustar hacia abajo, lo que crea un precio máximo más bajo para la regla, antes de cotizar en Amazon.</li><li>**[!UICONTROL Increase By]** - Elija cuándo desea que se defina _[!UICONTROL Ceiling Price Source]_para ajustar, lo que crea un precio máximo más alto para la regla, antes de añadirla a Amazon.</li><li>**[!UICONTROL Match]** - Elija cuándo no desea que el precio del anuncio fluctúe por encima del valor definido _[!UICONTROL Ceiling Price Source]_valor. Cuando se configura como `Match`, el_[!UICONTROL Apply]_ y _[!UICONTROL Ceiling Adjustment Amount]_los campos están desactivados.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajuste porcentual en relación con la variable _[!UICONTROL Ceiling Price Source]_valor. |
| [!UICONTROL Ceiling Price Adjustment] | Introduzca el valor numérico del porcentaje para ajustar el _[!UICONTROL Ceiling Price Source]_valor. |
