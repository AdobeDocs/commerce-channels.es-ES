---
title: Precio de anuncio
description: Utilice la configuración de Precio de anuncio para determinar el origen de precio y el valor de precio base (predeterminado) para sus anuncios de Amazon.
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# Precio de anuncio

[!UICONTROL Listing Price] la configuración forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [tablero de almacenamiento](./amazon-store-dashboard.md).

Estos ajustes definen qué [!DNL Commerce] atributo de precio que se utilizará como fuente de precios, que es el valor de precio base (predeterminado) para sus anuncios de Amazon. Los [reglas de precios](./pricing-rule-general-settings.md) para ajustar automáticamente el precio de su anuncio de Amazon en relación con el valor establecido para _[!UICONTROL Magento Price Source]_.

Puede configurar su [ámbito de precios](./price-scope.md) como global o sitio web. Si su ámbito de precios está establecido en `Global`, hay una única fuente de precios para todas sus tiendas/sitios web. Si su ámbito de precios está establecido en `Website`, la fuente de precios utiliza una lógica de reserva del precio del sitio web (si está disponible) seguida del precio predeterminado (global).

Si una regla de listado está configurada para aplicarse a más de un sitio web, el orden en que se usa el precio del sitio web se determina mediante la configuración de prioridad del sitio web definida en la variable [regla de listado](./listing-rules.md). Estas reglas permiten definir los precios de los productos en todo el catálogo. Para ver si está utilizando el ámbito de precios del sitio web, consulte [Alcance del precio del catálogo](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

Las opciones enumeradas en _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ y _[!UICONTROL Strike Through Price (MSRP)]_incluya los atributos de precios configurados. Los atributos de precio son [!DNL Commerce] Atributos de producto con el valor Tipo de entrada de catálogo para propietario de tienda establecido en `Price`. Consulte [Tipos de entrada de atributos](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Configurar los precios de anuncio {#configure-listing-price-settings}

1. Haga clic en **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda el _[!UICONTROL Listing Price]_para obtener más información.

1. Para **[!UICONTROL Magento Price Source]** (obligatorio), elija una opción.

   El valor predeterminado es `Price`. Esta configuración determina el origen de precio que se usa para los anuncios de Amazon. Si crea [reglas de precios](./pricing-products.md), las reglas se aplican al valor definido para el atributo seleccionado aquí. Puede seleccionar cualquier atributo de precio configurado. Sin embargo, si el atributo seleccionado no se rellena para un producto, el origen de precio del producto vuelve a ser `Price` cuando se aplican reglas de precios para determinar el precio de anuncio de Amazon publicado.

1. Para **[!UICONTROL Minimum Advertised Price (MAP)**], elija una opción.

   El valor predeterminado no es ninguna selección. Esta configuración habilita un precio mínimo publicitado (MAP) para un producto. Cuando define un atributo de precio y el precio de anuncio de un producto cae por debajo del precio mínimo determinado (según la fuente de precios y las reglas), este valor se convierte en el MAP para la oferta. Esta configuración le permite implementar [reglas de precios](./pricing-products.md), mientras controla el precio mínimo de un producto. Para evitar que el precio de un anuncio sea demasiado bajo, elija un atributo de precio para utilizarlo como MAP. Sin embargo, si el campo de precios seleccionado no está definido para un producto, no se utiliza el MAP.

1. Para **[!UICONTROL Strike Through Price (MSRP)]**, elija una opción.

   El valor predeterminado no es ninguna selección. Esta configuración determina qué atributo de precio se utiliza como precio de venta sugerido por el fabricante (MSRP) para un producto. Si el precio de su anuncio es inferior al MSRP definido, su anuncio de Amazon se muestra con una pulsación del precio MSRP con el precio de la cotización más bajo, junto con el porcentaje y la cantidad calculados &quot;Usted ahorra&quot;. Sin embargo, si el campo de precios seleccionado no está definido para un producto, el MSRP no se calcula.

   >[!NOTE]
   >
   >Esta configuración solo se aplica a los anuncios que hayan ganado el [Buy Box](./buy-box-competitor-pricing.md) posición. El Buy Box es otorgado por Amazon al vendedor que tiene el producto listado normalmente al mejor precio, junto con otros factores como la oferta de envío FBA/Prime, disponibilidad y el rendimiento del vendedor.

1. Para **Aplicar impuesto sobre el valor añadido (IVA)**, elija una opción:

   - `Disabled` - (Predeterminado) Elija cuándo no desea aplicar IVA a su precio de venta.

   - `Enabled` - Elija cuándo desea aplicar el IVA a su precio de venta. El IVA se utiliza normalmente como un impuesto sobre las ventas en los países europeos y se añade al precio final en Amazon. El IVA no se aplica al precio final de los anuncios que se utilizan dentro de una regla de precios inteligente, a menos que la variable [precio mínimo](./floor-price.md) se visita.
   >[!NOTE]
   >
   >Las empresas de la Unión Europea (UE) están obligadas a enviar facturas a compradores comerciales, de modo que el cliente pueda remitir impuestos. Puede generar estas facturas y calcular los impuestos usted mismo o utilizar un servicio de cálculo de impuestos como el servicio de cálculo de IVA de Amazon. Amazon recomienda registrarse en [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Si elige un método diferente, es responsable del cumplimiento del IVA.>
   >
   >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

1. Para **[!UICONTROL VAT Percentage]**, introduzca el valor de su tipo de IVA.

   El valor predeterminado es `0.00`. Este valor se utiliza para calcular el importe del IVA que se agregará al precio de venta. If `10.2` se introduce, se aplica un IVA del 10,20% al precio de tu anuncio. Este campo está desactivado cuando el campo Aplicar impuesto sobre el valor añadido (IVA) está establecido en `Disabled`.

1. **(solo tiendas del Reino Unido)** Para **[!UICONTROL Amazon Product Tax Code (PTC)]**, elija una opción:

   - `Do Not Manage PTC` - (Predeterminado) Seleccione si utiliza un servicio de cálculo de impuestos de terceros o si ya ha configurado todos los cálculos de impuestos en su [!DNL Amazon Seller Central] cuenta. Cuando se elige, el canal de ventas de Amazon no envía información del código de impuestos al producto a su [!DNL Amazon Seller Central] cuenta.

   - `Set Default PTC` - Elija si tiene un código de impuesto universal (PTC) que desee usar para todos sus productos. Cuando se elija, debe completar la _[!UICONTROL Default PTC]_.

      - Para **[!UICONTROL Default PTC]**, introduzca el PTC predeterminado que se utilizará para todos los anuncios de Amazon aptos. Si su PTC predeterminado está establecido en su [!DNL Amazon Seller Central] deje este campo en blanco. Los cambios realizados en este campo no afectan a las listas de Amazon existentes. Para cambiar el PTC predeterminado de un anuncio existente, el listado debe ser [ended](./end-listings-manually.md) y se ha creado un nuevo listado.
   >[!NOTE]
   >
   >Si utiliza el servicio de cálculo de IVA de Amazon, debe conocer la categoría de impuestos de sus productos. Un PTC es el código de ID de categoría de impuestos de Amazon para compras B2B en la UE. Consulte [Códigos de impuesto de producto de Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Currency Conversion]**, elija una opción.

   El valor predeterminado es `Disabled`. Estas opciones dependen del [!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html)Configuración de {target=&quot;_blank&quot;}. Si no hay opciones disponibles, configure la configuración de moneda.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Precio de anuncio](assets/amazon-listing-price.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Magento Price Source] | Determina el origen de precio que se usa al crear los anuncios de Amazon. El valor predeterminado es `Price`. Si elige un atributo diferente, como `Amazon Price` o `Special Price`, el valor definido para el atributo se utiliza en la lista de Amazon. Sin embargo, si el atributo seleccionado no está definido, `Price` se utiliza. |
| [!UICONTROL Minimum Advertised Price (MAP)] | La variable [!DNL Commerce] para los precios de MAP. Al seleccionar la opción MAP, se establece automáticamente el anuncio de Amazon en el precio MAP si el precio del anuncio es inferior al precio MAP. |
| [!UICONTROL Strike Through Price (MSRP)] | La variable [!DNL Commerce] que representa el precio de MSRP. Si el precio de su cotización en Amazon es inferior al MSRP, muestra una pulsación del precio del MSRP y el precio de la cotización. Esta configuración también se utiliza para calcular la cantidad y el porcentaje de &quot;Guardar&quot;, pero esta función solo se aplica a los anuncios que hayan ganado la [Buy Box](./buy-box-competitor-pricing.md) posición. |
| [!UICONTROL Apply Value Added Tax (VAT)] | El IVA lo utilizan los vendedores de la Unión Europea.<br><br>Choose `Disabled` si no desea que se agregue el IVA a los precios de venta.<br><br>Choose `Enabled` e introduzca el porcentaje de IVA para aplicar el IVA a los precios de venta. |
| [!UICONTROL VAT Percentage] | Defina el porcentaje que se utilizará para calcular la cantidad de IVA que se agregará al precio de cotización de sus anuncios de Amazon. <br><br>Si introduce `5`, se aplicará un IVA del 5 % al precio final de la cotización una vez que se hayan aplicado todas las reglas de precios. El impuesto sobre el IVA no se aplica al precio final de los anuncios que se utilizan dentro de una regla de precios inteligente, a menos que la variable [floor](./floor-price.md) o [techo](./optional-ceiling-price.md) se visita. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Solo aparece en las tiendas del Reino Unido) Determina si el canal de ventas de Amazon envía la información del código de impuestos al producto a su [!DNL Amazon Seller Central] cuenta. <br><br>Select **No administrar PTC** si utiliza un servicio de cálculo de impuestos de terceros o ya ha configurado todos los cálculos de impuestos en su [!DNL Amazon Seller Central] cuenta. Cuando se establece en esta opción, el canal de ventas de Amazon no envía ninguna información de código de impuesto al producto a su [!DNL Amazon Seller Central] cuenta.<br><br>Select **Definir PTC predeterminado** si tiene un código de impuesto universal que desea usar para todos sus productos.<br><br>Consulte [Códigos de impuesto de producto de Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | Solo aparece cuando **Código de impuesto de producto (PTC) de Amazon** está configurado como `Set Default PTC`. Introduzca el PTC predeterminado que se utilizará para todos los anuncios de Amazon aptos. Si su PTC predeterminado está establecido en su [!DNL Amazon Seller Central] deje este campo en blanco. <br><br>Los cambios realizados en este campo no afectan a las listas existentes. El listado debe ser [ended](./end-listings-manually.md) y un nuevo listado creado para que el cambio surta efecto. |
| [!UICONTROL Currency Conversion] | Permite que [!DNL Commerce] moneda predeterminada de tienda para convertir con precisión a su moneda predeterminada de Amazon y publicar sus precios en la moneda apropiada. La conversión de moneda siempre se basa en su [!DNL Commerce] moneda predeterminada.<br><br>Puede seguir viendo su [!DNL Commerce] y monedas de Amazon cuando haya otras monedas disponibles. Si su valor predeterminado es [!DNL Commerce] La moneda coincide con la moneda predeterminada de Amazon y deje desactivada la Conversión de moneda.<br><br>Por ejemplo, si su [!DNL Commerce] la moneda predeterminada es CAD (dólares canadienses) y la moneda predeterminada de Amazon es USD. Debe activar Conversión de moneda y elegir CAD de tasa de conversión a USD. Las opciones presentadas se basan en la integración de [!DNL Commerce] conversiones de moneda. Si no ve la opción que está buscando, [configure la moneda en [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
