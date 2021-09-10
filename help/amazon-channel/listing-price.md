---
title: Precio de anuncio
description: Utilice la configuración de Precio de anuncio para determinar el origen de precio y el valor de precio base (predeterminado) para sus anuncios de Amazon.
redirect_from: /sales-channels/asc/ob-listing-price.html: 
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 0%

---

# Precio de anuncio

[!UICONTROL Listing Price] la configuración forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Estos ajustes definen qué atributo de precio [!DNL Commerce] utilizar como fuente de precios, que es el valor de precio base (predeterminado) para sus anuncios de Amazon. Estas configuraciones las utilizan las [reglas de precios](./pricing-rule-general-settings.md) para ajustar automáticamente el precio de listado de Amazon en relación con el valor establecido para _[!UICONTROL Magento Price Source]_.

Puede configurar su [ámbito de precios](./price-scope.md) como global o sitio web. Si su ámbito de precios está establecido en `Global`, existe una única fuente de precios para todas sus tiendas/sitios web. Si el ámbito de precios está establecido en `Website`, la fuente de precios utiliza una lógica de reserva del precio del sitio web (si está disponible) seguida del precio predeterminado (global).

Si una regla de listado está configurada para aplicarse a más de un sitio web, el orden en que se usa el precio del sitio web está determinado por la configuración de prioridad del sitio web definida en la [regla de listado](./listing-rules.md). Estas reglas permiten definir los precios de los productos en todo el catálogo. Para ver si está usando el ámbito de precios del sitio web, consulte [Alcance de precio del catálogo](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

Las opciones enumeradas en _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ y _[!UICONTROL Strike Through Price (MSRP)]_incluyen los atributos de precios configurados. Los atributos de precio son [!DNL Commerce] atributos de producto con el valor Tipo de entrada de catálogo para propietario de tienda establecido en `Price`. Consulte [Tipos de entrada de atributos](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Configurar los precios de anuncio {#configure-listing-price-settings}

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección _[!UICONTROL Listing Price]_.

1. Para **[!UICONTROL Magento Price Source]** (obligatorio), elija una opción.

   El valor predeterminado es `Price`. Esta configuración determina el origen de precio que se usa para los anuncios de Amazon. Si crea [reglas de precios](./pricing-products.md), las reglas se aplican al valor definido para el atributo seleccionado aquí. Puede seleccionar cualquier atributo de precio configurado. Sin embargo, si el atributo seleccionado no se rellena para un producto, el origen de precios del producto vuelve a `Price` de forma predeterminada cuando se aplican las reglas de precios para determinar el precio publicado en la lista de Amazon.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], elija una opción.

   El valor predeterminado no es ninguna selección. Esta configuración habilita un precio mínimo publicitado (MAP) para un producto. Cuando define un atributo de precio y el precio de anuncio de un producto cae por debajo del precio mínimo determinado (según la fuente de precios y las reglas), este valor se convierte en el MAP para la oferta. Esta configuración le permite implementar [reglas de precios](./pricing-products.md), a la vez que controla el precio mínimo de un producto. Para evitar que el precio de un anuncio sea demasiado bajo, elija un atributo de precio para utilizarlo como MAP. Sin embargo, si el campo de precios seleccionado no está definido para un producto, no se utiliza el MAP.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, elija una opción.

   El valor predeterminado no es ninguna selección. Esta configuración determina qué atributo de precio se utiliza como precio de venta sugerido por el fabricante (MSRP) para un producto. Si el precio de su anuncio es inferior al MSRP definido, su anuncio de Amazon se muestra con una pulsación del precio MSRP con el precio de la cotización más bajo, junto con el porcentaje y la cantidad calculados &quot;Usted ahorra&quot;. Sin embargo, si el campo de precios seleccionado no está definido para un producto, el MSRP no se calcula.

   >[!NOTE]
   >
   >Esta configuración solo se aplica a los anuncios que hayan ganado la posición [Buy Box](./buy-box-competitor-pricing.md). El Buy Box es otorgado por Amazon al vendedor que tiene el producto listado normalmente al mejor precio, junto con otros factores como la oferta de envío FBA/Prime, disponibilidad y el rendimiento del vendedor.

1. Para **Aplicar impuesto sobre el valor añadido (IVA)**, elija una opción:

   - `Disabled` - (Predeterminado) Elija cuándo no desea aplicar IVA a su precio de venta.

   - `Enabled` - Elija cuándo desea aplicar el IVA a su precio de venta. El IVA se utiliza normalmente como un impuesto sobre las ventas en los países europeos y se añade al precio final en Amazon. El IVA no se aplica al precio final para los anuncios que se utilizan dentro de una regla de precios inteligente, a menos que se llegue al [precio mínimo](./floor-price.md).
   >[!NOTE]
   >
   >Las empresas de la Unión Europea (UE) están obligadas a enviar facturas a compradores comerciales, de modo que el cliente pueda remitir impuestos. Puede generar estas facturas y calcular los impuestos usted mismo o utilizar un servicio de cálculo de impuestos como el servicio de cálculo de IVA de Amazon. Amazon recomienda registrarse en [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Si elige un método diferente, es responsable del cumplimiento del IVA.>
   >
   >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, introduzca el valor de su tasa de IVA.

   El valor predeterminado es `0.00`. Este valor se utiliza para calcular el importe del IVA que se agregará al precio de venta. Si se introduce `10.2`, se aplica un IVA del 10,20% al precio de su anuncio. Este campo se desactiva cuando el campo Aplicar impuesto sobre el valor añadido (IVA) se establece en `Disabled`.

1. **(solo tiendas del Reino Unido)** Para  **[!UICONTROL Amazon Product Tax Code (PTC)]**, elija una opción:

   - `Do Not Manage PTC` - (Predeterminado) Elija si está utilizando un servicio de cálculo de impuestos de terceros o si ya ha configurado todos los cálculos de impuestos en su  [!DNL Amazon Seller Central] cuenta. Cuando se elige, el canal de ventas de Amazon no envía ninguna información sobre el código de impuestos al producto a su cuenta [!DNL Amazon Seller Central].

   - `Set Default PTC` - Elija si tiene un código de impuesto universal (PTC) que desee usar para todos sus productos. Cuando se elige, debe completar _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, introduzca el PTC predeterminado que se utilizará para todos los listados de Amazon aptos. Si su PTC predeterminado está establecido en su cuenta [!DNL Amazon Seller Central], deje este campo en blanco. Los cambios realizados en este campo no afectan a las listas de Amazon existentes. Para cambiar el PTC predeterminado de un listado existente, el listado debe estar [finalizado](./end-listings-manually.md) y se debe crear un listado nuevo.
   >[!NOTE]
   >
   >Si utiliza el servicio de cálculo de IVA de Amazon, debe conocer la categoría de impuestos de sus productos. Un PTC es el código de ID de categoría de impuestos de Amazon para compras B2B en la UE. Consulte [Códigos de impuestos del producto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;} de Amazon.

1. Para **[!UICONTROL Currency Conversion]**, elija una opción.

   El valor predeterminado es `Disabled`. Estas opciones dependen de la configuración [!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}. Si no hay opciones disponibles, configure la configuración de moneda.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Precio de anuncio](assets/amazon-listing-price.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Magento Price Source] | Determina el origen de precio que se usa al crear los anuncios de Amazon. El valor predeterminado es `Price`. Si elige un atributo diferente como `Amazon Price` o `Special Price`, el valor definido para el atributo se utilizará en la lista de Amazon. Sin embargo, si el atributo seleccionado no está definido, se utiliza `Price`. |
| [!UICONTROL Minimum Advertised Price (MAP)] | El atributo [!DNL Commerce] para los precios de MAP. Al seleccionar la opción MAP, se establece automáticamente el anuncio de Amazon en el precio MAP si el precio del anuncio es inferior al precio MAP. |
| [!UICONTROL Strike Through Price (MSRP)] | El atributo [!DNL Commerce] que representa el precio del MSRP. Si el precio de su cotización en Amazon es inferior al MSRP, muestra una pulsación del precio del MSRP y el precio de la cotización. Esta configuración también se utiliza para calcular la cantidad y el porcentaje &quot;Se guarda&quot;, pero esta función solo se aplica a los anuncios que han ganado la posición [Buy Box](./buy-box-competitor-pricing.md). |
| [!UICONTROL Apply Value Added Tax (VAT)] | El IVA lo utilizan los vendedores de la Unión Europea.<br><br>Elija  `Disabled` si no desea que se agregue IVA a los precios de venta.<br><br>Elija  `Enabled` y, a continuación, introduzca el porcentaje de IVA para aplicar el IVA a los precios de su anuncio. |
| [!UICONTROL VAT Percentage] | Defina el porcentaje que se utilizará para calcular la cantidad de IVA que se agregará al precio de cotización de sus anuncios de Amazon. <br><br>Si introduce  `5`, se aplicará un IVA del 5 % al precio final del anuncio después de aplicar todas las reglas de precios. El impuesto sobre el IVA no se aplica al precio final de los anuncios que se utilizan dentro de una regla de precios inteligente, a menos que se pulse [floor](./floor-price.md) o [techo](./optional-ceiling-price.md). |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Solo aparece en las tiendas del Reino Unido) Determina si el canal de ventas de Amazon envía la información del código fiscal del producto a su cuenta [!DNL Amazon Seller Central]. <br><br>Seleccione  **No administrar** PTC si utiliza un servicio de cálculo de impuestos de terceros o si ya ha configurado todos los cálculos de impuestos en su  [!DNL Amazon Seller Central] cuenta. Cuando se establece en esta opción, el canal de ventas de Amazon no envía información del código de impuestos del producto a su cuenta [!DNL Amazon Seller Central].<br><br>Seleccione  **Establecer** PTC predeterminado si tiene un código de impuesto universal que desee usar para todos sus productos.<br><br>Consulte Códigos de impuesto de producto de  [Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | Solo aparece cuando **Código de impuesto de producto de Amazon (PTC)** está configurado en `Set Default PTC`. Introduzca el PTC predeterminado que se utilizará para todos los anuncios de Amazon aptos. Si su PTC predeterminado está establecido en su cuenta [!DNL Amazon Seller Central], deje este campo en blanco. <br><br>Los cambios realizados en este campo no afectan a las listas existentes. El listado debe estar [finalizado](./end-listings-manually.md) y se debe crear un nuevo listado para que el cambio surta efecto. |
| [!UICONTROL Currency Conversion] | Permite que la moneda predeterminada de su tienda [!DNL Commerce] se convierta con precisión a la moneda predeterminada de Amazon para publicar los precios del anuncio en la moneda apropiada. La conversión de moneda siempre se basa en su [!DNL Commerce] moneda predeterminada.<br><br>Puede seguir viendo las monedas predeterminadas  [!DNL Commerce] y Amazon cuando haya otras monedas disponibles. Si la moneda predeterminada [!DNL Commerce] coincide con la moneda predeterminada de Amazon, deje deshabilitada la Conversión de moneda.<br><br>Por ejemplo, si la moneda  [!DNL Commerce] predeterminada es CAD (dólares canadienses) y la moneda predeterminada de Amazon es USD, debe activar Conversión de moneda y elegir CAD de tasa de conversión a USD. Las opciones presentadas se basan en las conversiones de moneda [!DNL Commerce] integradas. Si no ve la opción que está buscando, [configure la moneda en [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
