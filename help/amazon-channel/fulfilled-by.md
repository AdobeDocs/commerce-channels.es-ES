---
title: Cumplido por
description: Utilice la configuración Satisfecho por para determinar cómo se satisfacen (envían) los pedidos de los listados de Amazon.
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Cumplido por

_[!UICONTROL Fulfilled By]_La configuración de forma parte de la configuración del anuncio de la tienda. Se accede a la configuración de anuncio desde el [tablero de tienda](./amazon-store-dashboard.md).

Esta configuración define la parte que cumple (o envía) los pedidos. Si todos sus pedidos se satisfacen con un método, elija entre comerciante (usted) o Amazon. Si planea cumplir los pedidos de sus ubicaciones y utilizar Amazon, se recomienda utilizar la tercera opción y configurar una [!DNL Commerce] atributo de producto.

- **[!UICONTROL Fulfilled by Merchant]** - Elija si usted, el comerciante, cumple todos los pedidos. Cuando se realiza un pedido, el inventario se deduce de su [!DNL Commerce] catálogo.

- **[!UICONTROL Fulfilled by Amazon]** : seleccione si Amazon cumple todos los pedidos. Con esta opción, el inventario de productos no se deduce de su [!DNL Commerce] catálogo cuando se realiza un pedido. Las existencias de inventario para los pedidos satisfechos de Amazon se almacenan y deducen de sus almacenes. Antes de asignar esta opción, debe comprobar en su [!DNL Amazon Seller Central] cuenta de que sus productos cumplen los requisitos para _Cumplido Por Amazon_ (FBA) cumplimiento. El inventario de FBA se administra directamente a través de su [!DNL Amazon Seller Central] Cuenta. Con este método de cumplimiento, el canal de ventas de Amazon no comparte actualizaciones de cantidad entre [!DNL Commerce] y Amazon. Por lo tanto, no todas las herramientas de marketing descritas en la configuración de cantidad están disponibles en el canal de ventas de Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si es posible que Amazon y usted completen sus productos, es posible que desee crear un [!DNL Commerce] atributo de producto con valores para Satisfecho por el Comerciante y Satisfecho por Amazon. La configuración de este valor por producto indica quién cumple los pedidos.

El método de cumplimiento es un atributo regional y se basa en la variable **[!UICONTROL Amazon Marketplace Country]** configuración definida durante [integración de tienda](./store-integration.md). Cuando se realiza un cambio, este afecta a todos los anuncios de Amazon que lo compartan [!DNL Amazon Seller SKU] en las tiendas de Amazon que venden en la misma región (tal y como se define en _[!UICONTROL Amazon Marketplace Country]_durante [integración de tienda](./store-integration.md)). Un cambio en un recurso compartido [!DNL Amazon Seller SKU] en Estados Unidos no afecta a la configuración de las tiendas Amazon para una región diferente (tal como se define durante la integración de la tienda).

>[!NOTE]
>
>Cuando Amazon (FBA) completa un pedido y este se importa, puede ver datos ficticios de algunos campos en los detalles del pedido. Consulte [Detalles de pedidos de Amazon](./amazon-order-details.md).

## Configure las variables [!UICONTROL Fulfilled By] configuración {#configure-fulfilled-by-settings}

1. Clic **[!UICONTROL Listing Settings]** en el tablero de la tienda.

1. Expanda el _[!UICONTROL Fulfilled By]_sección.

1. Para **[!UICONTROL Product Fulfilled By]**, elija quién cumple (envía) el pedido:

   - `Fulfilled by Merchant` - El comerciante cumple la orden.

   - `Fulfilled by Amazon` - Amazon data warehouse cumple el pedido.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] El atributo indica quién cumple el pedido por producto.

      Si se elige, elija la [!DNL Commerce] atributo que desea asignar en **[!UICONTROL Fulfilled by Attribute]**.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Cumplido por la configuración](assets/amazon-fulfilled-by.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Opciones:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Elija si cumple los pedidos. Cuando se realiza un pedido, el inventario se deduce de su [!DNL Commerce] catálogo. Cuando se crea un nuevo producto, se asigna el método de cumplimiento de Merchant Fulfilled.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Seleccione si Amazon cumple los pedidos. Con este método de cumplimiento, el inventario de productos no se deduce de su [!DNL Commerce] catálogo cuando se realiza un pedido. Cuando se crea un producto, se crea con _[!UICONTROL Fulfilled by Amazon (FBA)]_como el tipo de cumplimiento. Asegúrese de que sus productos cumplen los requisitos para la FBA dentro de su [!DNL Amazon Seller Central] cuenta. El inventario de FBA también se administra directamente a través de su [!DNL Amazon Seller Central] cuenta. Con este método de satisfacción de pedidos, las actualizaciones de cantidad no se publican en relación con su [!DNL Commerce] catálogo, por lo que no puede utilizar algunas de las herramientas de marketing descritas en [Configuración de stock/cantidad](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Elija si tiene un existente [!DNL Commerce] atributo que determina si el comerciante lo cumple o Amazon lo cumple. Cuando se elige, **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Elija la [!DNL Commerce] atributo utilizado para determinar el método de cumplimiento.<br><br>Por ejemplo, si el atributo es _Cumplido por_ y elige el valor del atributo como _[!UICONTROL Fulfilled By Merchant]_o_[!UICONTROL Fulfilled By Amazon (FBA)]_, el sistema utiliza ese valor como tipo de cumplimiento para un nuevo producto. Como comerciante, debe asegurarse de que sus productos son aptos para la realización de FBA dentro de su [!DNL Amazon Seller Central] cuenta. El inventario de FBA también se administra directamente a través de su cuenta de vendedor de Amazon.<br><br>Las opciones dependen de los atributos que configure para sus productos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
