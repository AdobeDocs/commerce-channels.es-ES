---
title: 'Canal de ventas de Amazon: [!UICONTROL Listing Price]'
description: Utilice la configuración Precio de anuncio para determinar el origen del precio y el valor de precio base (por defecto) de los anuncios de Amazon.
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

La configuración de [!UICONTROL Listing Price] forma parte de la configuración del listado de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración define qué atributo de asignación de precios de [!DNL Commerce] usar como fuente de precios, que es el valor de precio base (predeterminado) de los anuncios de Amazon. Estas configuraciones las usan tus [reglas de precios](./pricing-rule-general-settings.md) para ajustar automáticamente el precio del anuncio de Amazon en relación con el valor establecido para _[!UICONTROL Magento Price Source]_.

Puedes configurar tu [ámbito de precios](./price-scope.md) como global o sitio web. Si el ámbito de precios se establece en `Global`, existe una única fuente de precios para todas las tiendas y sitios web. Si el ámbito de precios se establece en `Website`, la fuente de precios usa la lógica de reserva del precio del sitio web (si está disponible) seguido del precio predeterminado (global).

Si una regla de listado está configurada para aplicarse a más de un sitio web, el orden en que se usa el precio del sitio web viene determinado por la configuración de prioridad del sitio web definida en la [regla de listado](./listing-rules.md). Estas reglas permiten definir los precios de los productos en todo el catálogo. Para ver si está usando el ámbito de precios del sitio web, consulte [Ámbito de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

Las opciones enumeradas en _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ y _[!UICONTROL Strike Through Price (MSRP)]_incluyen los atributos de precios configurados. Los atributos de precios son [!DNL Commerce] atributos de productos con el valor Tipo de entrada de catálogo para propietario de tienda establecido en `Price`. Consulte [Tipos de entrada de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## Configurar el precio del anuncio {#configure-listing-price-settings}

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección _[!UICONTROL Listing Price]_.

1. Para **[!UICONTROL Magento Price Source]** (obligatorio), elija una opción.

   El valor predeterminado es `Price`. Esta opción determina la fuente de precios que se usa para los anuncios de Amazon. Si crea [reglas de precios](./pricing-products.md), las reglas se aplican al valor definido para el atributo seleccionado aquí. Puede seleccionar cualquier atributo de precios configurado. Sin embargo, si el atributo seleccionado no se ha rellenado para un producto, el origen de precios del producto vuelve a ser `Price` de forma predeterminada cuando se aplican las reglas de precios para determinar el precio de listado de Amazon publicado.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], elija una opción.

   El valor predeterminado es sin selección. Esta configuración habilita un precio mínimo anunciado (MAP) para un producto. Cuando define un atributo de asignación de precios y el precio del anuncio de un producto cae por debajo del precio mínimo determinado (según la fuente y las reglas de asignación de precios), este valor se convierte en el mapa para el anuncio. Esta configuración le permite implementar [reglas de precios](./pricing-products.md), sin dejar de controlar el precio mínimo de un producto. Para evitar que el precio de un anuncio sea demasiado bajo, elija un atributo de asignación de precios para utilizarlo como MAPA. Sin embargo, si el campo de asignación de precios seleccionado no está definido para un producto, no se utiliza el MAP.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, elija una opción.

   El valor predeterminado es sin selección. Esta configuración determina qué atributo de precios se utiliza como precio de venta sugerido por el fabricante (MSRP) para un producto. Si el precio del anuncio es menor que el MSRP definido, el anuncio de Amazon se muestra con una tacha del precio del MSRP con el precio más bajo, junto con la cantidad y el porcentaje calculados como &quot;Ahorras&quot;. Sin embargo, si el campo de precios seleccionado no está definido para un producto, el MSRP no se calcula.

   >[!NOTE]
   >
   >Esta configuración solo se aplica a los anuncios que han obtenido la posición [Buy Box](./buy-box-competitor-pricing.md). El Buy Box es otorgado por Amazon al vendedor que tiene el producto listado por lo general al mejor precio, junto con otros factores como FBA/envío Prime ofrecido, disponibilidad y el rendimiento del vendedor.

1. Para **Aplicar impuesto al valor agregado (IVA)**, elija una opción:

   - `Disabled` - (Predeterminado) Elige cuándo no quieres aplicar el IVA al precio del anuncio.

   - `Enabled`: elige cuándo quieres aplicar el IVA al precio del anuncio. El IVA se suele utilizar como impuesto sobre las ventas en los países europeos y se añade al precio final que aparece en Amazon. El IVA no se aplica al precio final de los anuncios que se usan dentro de una regla de precios inteligente, a menos que se alcance el [precio mínimo](./floor-price.md).

   >[!NOTE]
   >
   >Las empresas de la Unión Europea (UE) están obligadas a enviar facturas a los compradores de negocios, para que el cliente pueda remitir el impuesto. Puede generar estas facturas y calcular los impuestos usted mismo o utilizar un servicio de cálculo de impuestos como el servicio de cálculo de IVA de Amazon. Amazon recomienda registrarse en [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). Si elige un método diferente, usted es responsable del cumplimiento del IVA.>
   >
   >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, introduce el valor de tu tasa de IVA.

   El valor predeterminado es `0.00`. Este valor se utiliza para calcular el importe de IVA que se añadirá al precio del anuncio. Si se introduce `10.2`, se aplica un IVA del 10,20% al precio del anuncio. Este campo está deshabilitado cuando el campo Aplicar impuesto al valor agregado (IVA) está establecido en `Disabled`.

1. **(Solo tiendas del Reino Unido)** Para **[!UICONTROL Amazon Product Tax Code (PTC)]**, elija una opción:

   - `Do Not Manage PTC` - (Predeterminado) Elija si está usando un servicio de cálculo de impuestos de terceros o ya ha configurado todos los cálculos de impuestos en su cuenta de [!DNL Amazon Seller Central]. Cuando se elige, el canal de ventas de Amazon no envía información de código de impuestos del producto a su cuenta de [!DNL Amazon Seller Central].

   - `Set Default PTC`: elija si desea usar un código de impuesto universal de productos (PTC) para todos sus productos. Si se elige, se debe completar _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, introduzca el PTC predeterminado que se utilizará para todos los anuncios de Amazon aptos. Si el PTC predeterminado está establecido en su cuenta de [!DNL Amazon Seller Central], deje este campo en blanco. Los cambios realizados en este campo no afectan a los anuncios de Amazon existentes. Para cambiar el PTC predeterminado de un anuncio existente, este debe ser [finalizado](./end-listings-manually.md) y se debe crear un nuevo anuncio.

   >[!NOTE]
   >
   >Si utiliza el servicio de cálculo de IVA de Amazon, debe conocer la categoría de impuestos de sus productos. Un PTC es el código de ID de categoría fiscal de Amazon para compras B2B en la UE. Ver [Códigos de impuesto sobre productos de Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. Para **[!UICONTROL Currency Conversion]**, elija una opción.

   El valor predeterminado es `Disabled`. Estas opciones dependen de la configuración de [!DNL Commerce] [currency](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html). Si no hay opciones disponibles, configure los valores de moneda.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Precio de anuncio](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| Campo | Descripción |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Determina el origen de precios que se utiliza para crear los anuncios de Amazon. El valor predeterminado es `Price`. Si elige un atributo diferente, como `Amazon Price` o `Special Price`, el valor definido para el atributo se utilizará en el listado de Amazon. Sin embargo, si el atributo seleccionado no está definido, se utiliza `Price`. |
| [!UICONTROL Minimum Advertised Price (MAP)] | Atributo [!DNL Commerce] para los precios de MAP. Si elige la opción de asignación, el anuncio de Amazon se establece automáticamente en el precio de asignación si el precio del anuncio es inferior al precio de asignación. |
| [!UICONTROL Strike Through Price (MSRP)] | Atributo [!DNL Commerce] que representa los precios MSRP. Si el precio del anuncio de Amazon es menor que el MSRP, muestra una tachadura del precio del MSRP y el precio del anuncio. Esta configuración también se usa para calcular la cantidad y el porcentaje de &quot;Ahorras&quot;, pero esta característica solo se aplica a los anuncios que han ganado la posición de [Buy Box](./buy-box-competitor-pricing.md). |
| [!UICONTROL Apply Value Added Tax (VAT)] | Los vendedores de la Unión Europea utilizan el IVA.<br><br>Elige `Disabled` si no quieres que se agregue el IVA a los precios del anuncio.<br><br>Elige `Enabled` y luego ingresa el porcentaje de IVA para aplicar el IVA a los precios del anuncio. |
| [!UICONTROL VAT Percentage] | Define el porcentaje que se utilizará para calcular el importe de IVA que se añadirá al precio del anuncio de tus anuncios de Amazon. <br><br>Si escribes `5`, se aplicará un IVA del 5% al precio final del anuncio una vez que se hayan aplicado todas las reglas de precios. El impuesto sobre el IVA no se aplica al precio final de los anuncios que se usan dentro de una regla de precios inteligente, a menos que se aplique el [piso](./floor-price.md) o el [techo](./optional-ceiling-price.md). |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Aparece solo para tiendas de Reino Unido) Determina si el canal de ventas de Amazon envía información de código de impuestos del producto a su cuenta de [!DNL Amazon Seller Central]. <br><br>Seleccione **No administrar PTC** si está usando un servicio de cálculo de impuestos de terceros o ya ha configurado todos los cálculos de impuestos en su cuenta de [!DNL Amazon Seller Central]. Cuando se establece en esta opción, el canal de ventas de Amazon no envía información de código de impuestos del producto a su cuenta de [!DNL Amazon Seller Central].<br><br>Seleccione **Establecer PTC predeterminado** si tiene un código de impuesto universal que desee usar para todos sus productos.<br><br>Ver [Códigos de impuesto sobre productos de Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | Solo aparece cuando el **Código de impuestos sobre productos Amazon (PTC)** está establecido en `Set Default PTC`. Introduce el PTC por defecto que se utilizará para todos los anuncios de Amazon aptos. Si el PTC predeterminado está establecido en su cuenta de [!DNL Amazon Seller Central], deje este campo en blanco. <br><br>Los cambios realizados en este campo no afectan a los anuncios existentes. El anuncio debe ser [finalizado](./end-listings-manually.md) y se debe crear uno nuevo para que el cambio surta efecto. |
| [!UICONTROL Currency Conversion] | Permite que la moneda predeterminada de tu tienda [!DNL Commerce] se convierta con precisión a la moneda predeterminada de Amazon para publicar los precios del anuncio en la moneda adecuada. La conversión de moneda siempre se basa en la moneda predeterminada [!DNL Commerce].<br><br>Puede seguir viendo sus [!DNL Commerce] y monedas de Amazon predeterminadas cuando haya otras monedas disponibles. Si la moneda predeterminada [!DNL Commerce] coincide con la moneda predeterminada de Amazon, deje Deshabilitada la conversión de moneda.<br><br>Por ejemplo, si la divisa predeterminada de [!DNL Commerce] es CAD (dólares canadienses) y la divisa predeterminada de Amazon es USD, debe habilitar la conversión de divisa y elegir la tarifa de conversión CAD a USD. Las opciones presentadas se basan en las conversiones de moneda integradas de [!DNL Commerce]. Si no ve la opción que busca, [configure la moneda en [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
