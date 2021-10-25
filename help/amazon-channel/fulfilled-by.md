---
title: Cumplido por
description: Utilice la configuración Cumplimentar por para determinar cómo se cumplen (se envían) los pedidos de los anuncios de Amazon.
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Cumplido por

_[!UICONTROL Fulfilled By]_la configuración forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [tablero de almacenamiento](./amazon-store-dashboard.md).

Esta configuración define la parte que cumple (o envía) los pedidos. Si todos los pedidos se cumplen con un método, elija entre comerciante (usted) o Amazon. Si planea cumplir los pedidos de sus ubicaciones y utilizar Amazon, se recomienda utilizar la tercera opción y configurar una [!DNL Commerce] atributo de producto.

- **[!UICONTROL Fulfilled by Merchant]** - Elija si usted, el comerciante, cumple todos los pedidos. Cuando se realiza un pedido, el inventario se resta de su [!DNL Commerce] catálogo.

- **[!UICONTROL Fulfilled by Amazon]** - Seleccione si Amazon cumple todos los pedidos. Con esta opción, el inventario de productos no se deduce de su [!DNL Commerce] catálogo cuando se realiza un pedido. Las existencias de inventario para los pedidos cumplidos por Amazon se almacenan y se deducen de sus almacenes. Antes de asignar esta opción, debe verificar en la [!DNL Amazon Seller Central] tenga en cuenta que sus productos son aptos para _Completado Por Amazon_ (FBA) cumplimiento. El inventario de FBA se administra directamente a través de su [!DNL Amazon Seller Central] Cuenta. Con este método de cumplimiento, el canal de ventas de Amazon no comparte actualizaciones de cantidad entre [!DNL Commerce] y Amazon. Por lo tanto, no todas las herramientas de marketing descritas en Configuración de cantidad están disponibles en el canal de ventas de Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si usted y Amazon pueden satisfacer sus productos, es posible que desee crear un [!DNL Commerce] atributo product con valores para Completado por comerciante y Cumplimentado por Amazon. Al establecer este valor por producto, se indica quién satisface los pedidos.

El método de cumplimiento es un atributo regional y se basa en la variable **[!UICONTROL Amazon Marketplace Country]** configuración definida durante [integración de tiendas](./store-integration.md). Cuando se realiza un cambio, el cambio afecta a todos los listados de Amazon que comparten ese [!DNL Amazon Seller SKU] en las tiendas de Amazon que vendan en la misma región (tal y como se define en _[!UICONTROL Amazon Marketplace Country]_during [integración de tiendas](./store-integration.md)). Un cambio en un [!DNL Amazon Seller SKU] en Estados Unidos no afecta a los almacenes de Amazon establecidos para una región diferente (tal y como se define durante la integración de tiendas).

>[!NOTE]
>
>Cuando Amazon (FBA) completa un pedido y este se importa, se pueden ver datos ficticios de algunos campos en los detalles del pedido. Consulte [Detalles de pedidos de Amazon](./amazon-order-details.md).

## Configure las variables [!UICONTROL Fulfilled By] configuración {#configure-fulfilled-by-settings}

1. Haga clic en **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda el _[!UICONTROL Fulfilled By]_para obtener más información.

1. Para **[!UICONTROL Product Fulfilled By]**, elija quién cumple (envía) el orden:

   - `Fulfilled by Merchant` - El comerciante cumple con el orden.

   - `Fulfilled by Amazon` - El almacén de Amazon realiza el pedido.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] indica quién satisface el pedido por producto.

      Si se elige, elija la opción [!DNL Commerce] atributo que desea asignar en **[!UICONTROL Fulfilled by Attribute]**.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Cumplido con la configuración](assets/amazon-fulfilled-by.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opciones:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Elija si cumple los pedidos. Cuando se realiza un pedido, el inventario se resta de su [!DNL Commerce] catálogo. Cuando se crea un nuevo producto, se asigna el método de cumplimiento de Comerciante Satisfecho.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Seleccione si Amazon cumple los pedidos. Con este método de cumplimiento, el inventario de productos no se deduce de su [!DNL Commerce] catálogo cuando se realiza un pedido. Cuando se crea un producto, se crea con _[!UICONTROL Fulfilled by Amazon (FBA)]_como tipo de cumplimiento. Asegúrese de que sus productos sean aptos para el cumplimiento de FBA dentro de su [!DNL Amazon Seller Central] cuenta. El inventario de FBA también se administra directamente a través de su [!DNL Amazon Seller Central] cuenta. Con este método de cumplimiento, las actualizaciones de cantidad no se eliminan en relación con su [!DNL Commerce] , por lo que no puede utilizar algunas de las herramientas de marketing descritas en [Valores de stock/cantidad](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Elija si tiene una [!DNL Commerce] que determina si el comerciante lo cumple o si Amazon lo cumple. Cuando se elige, **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Elija la [!DNL Commerce] para determinar el método de cumplimiento.<br><br>Por ejemplo, si el atributo es _Cumplido por_ y elija el valor de atributo como _[!UICONTROL Fulfilled By Merchant]_o_[!UICONTROL Fulfilled By Amazon (FBA)]_, el sistema utiliza ese valor como tipo de cumplimiento para un nuevo producto. Como comerciante, debe asegurarse de que sus productos sean elegibles para el cumplimiento de FBA dentro de su [!DNL Amazon Seller Central] cuenta. El inventario de FBA también se administra directamente a través de su cuenta de vendedor de Amazon.<br><br>Las opciones dependen de los atributos que configure para sus productos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
