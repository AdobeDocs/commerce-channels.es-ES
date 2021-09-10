---
title: Cumplido por
description: Utilice la configuración Cumplimentar por para determinar cómo se cumplen (se envían) los pedidos de los anuncios de Amazon.
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 618
ht-degree: 0%

---

# Cumplido por

_[!UICONTROL Fulfilled By]_la configuración forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Esta configuración define la parte que cumple (o envía) los pedidos. Si todos los pedidos se cumplen con un método, elija entre comerciante (usted) o Amazon. Si planea cumplir los pedidos de sus ubicaciones y utilizar Amazon, se recomienda utilizar la tercera opción y configurar un atributo de producto [!DNL Commerce].

- **[!UICONTROL Fulfilled by Merchant]** - Elija si usted, el comerciante, cumple todos los pedidos. Cuando se realiza un pedido, el inventario se resta del catálogo [!DNL Commerce].

- **[!UICONTROL Fulfilled by Amazon]** - Seleccione si Amazon cumple todos los pedidos. Con esta opción, el inventario de productos no se deduce del catálogo [!DNL Commerce] cuando se realiza un pedido. Las existencias de inventario para los pedidos cumplidos por Amazon se almacenan y se deducen de sus almacenes. Antes de asignar esta opción, debe verificar en su cuenta de [!DNL Amazon Seller Central] que sus productos cumplen los requisitos para _Cumplimentados por Amazon_ (FBA). El inventario de FBA se administra directamente a través de su cuenta [!DNL Amazon Seller Central]. Con este método de cumplimiento, el canal de ventas de Amazon no comparte actualizaciones de cantidad entre [!DNL Commerce] y Amazon. Por lo tanto, no todas las herramientas de marketing descritas en Configuración de cantidad están disponibles en el canal de ventas de Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si usted y Amazon pueden satisfacer sus productos, es posible que desee crear un atributo de  [!DNL Commerce] producto con valores para Completado por el comerciante y Cumplimentado por Amazon. Al establecer este valor por producto, se indica quién satisface los pedidos.

El método de cumplimiento es un atributo regional y se basa en la configuración **[!UICONTROL Amazon Marketplace Country]** definida durante la [integración del almacén](./store-integration.md). Cuando se realiza un cambio, el cambio afecta a todos los listados de Amazon que comparten ese [!DNL Amazon Seller SKU] en los almacenes de Amazon que venden en la misma región (tal como se define en _[!UICONTROL Amazon Marketplace Country]_durante la [integración del almacén](./store-integration.md)). Un cambio en un [!DNL Amazon Seller SKU] compartido en Estados Unidos no afecta a los almacenes de Amazon establecidos para una región diferente (tal como se definió durante la integración de tiendas).

>[!NOTE]
>
>Cuando Amazon (FBA) completa un pedido y este se importa, se pueden ver datos ficticios de algunos campos en los detalles del pedido. Consulte [Detalles de pedidos de Amazon](./amazon-order-details.md).

## Configurar las opciones de [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección _[!UICONTROL Fulfilled By]_.

1. Para **[!UICONTROL Product Fulfilled By]**, elija quién cumple (envía) el pedido:

   - `Fulfilled by Merchant` - El comerciante cumple con el orden.

   - `Fulfilled by Amazon` - El almacén de Amazon realiza el pedido.

   - `Assign Fulfilled By Using Magento Product Attribute` - Un  [!DNL Commerce] atributo indica quién satisface el pedido por producto.

      Si se elige, elija el atributo [!DNL Commerce] que desea asignar en **[!UICONTROL Fulfilled by Attribute]**.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Cumplido con la configuración](assets/amazon-fulfilled-by.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opciones:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Elija si cumple los pedidos. Cuando se realiza un pedido, el inventario se resta del catálogo [!DNL Commerce]. Cuando se crea un nuevo producto, se asigna el método de cumplimiento de Comerciante Satisfecho.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Seleccione si Amazon cumple los pedidos. Con este método de cumplimiento, el inventario de productos no se resta del catálogo [!DNL Commerce] cuando se realiza un pedido. Cuando se crea un producto, se crea con _[!UICONTROL Fulfilled by Amazon (FBA)]_como tipo de cumplimiento. Asegúrese de que sus productos sean aptos para el cumplimiento de FBA dentro de su cuenta [!DNL Amazon Seller Central]. El inventario de FBA también se administra directamente a través de su cuenta [!DNL Amazon Seller Central]. Con este método de cumplimiento, las actualizaciones de cantidad no se insertan en relación con su catálogo [!DNL Commerce], por lo que no puede utilizar algunas de las herramientas de marketing descritas en [Configuración de stock/cantidad](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Seleccione si tiene un  [!DNL Commerce] atributo existente que determine si el comerciante lo completa o si Amazon lo completa. Cuando se elige, **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Elija el atributo [!DNL Commerce] utilizado para determinar el método de cumplimiento.<br><br>Por ejemplo, si el atributo es  _de_ bytes cumplidos y elige el valor de atributo como  _[!UICONTROL Fulfilled By Merchant]_o_[!UICONTROL Fulfilled By Amazon (FBA)]_, el sistema utilizará ese valor como tipo de cumplimiento para un nuevo producto. Como comerciante, debe asegurarse de que sus productos sean elegibles para el cumplimiento de FBA dentro de su cuenta [!DNL Amazon Seller Central]. El inventario de FBA también se administra directamente a través de su cuenta de vendedor de Amazon.<br><br>Las opciones dependen de los atributos que configure para sus productos de Amazon. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
