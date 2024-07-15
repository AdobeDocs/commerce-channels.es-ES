---
title: Cumplido por la configuración de anuncios de Amazon
description: Utilice la configuración Satisfecho por para determinar cómo se satisfacen (envían) los pedidos de los listados de Amazon.
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Cumplido por la configuración de anuncios de Amazon

La configuración de _[!UICONTROL Fulfilled By]_forma parte de la configuración del listado de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración define la parte que cumple (o envía) los pedidos. Si todos sus pedidos se satisfacen con un método, elija entre comerciante (usted) o Amazon. Si planea cumplir pedidos desde sus ubicaciones y utilizar Amazon, se recomienda utilizar la tercera opción y configurar un atributo de producto [!DNL Commerce].

- **[!UICONTROL Fulfilled by Merchant]** - Elija si usted, el comerciante, cumple todos los pedidos. Cuando se realiza un pedido, el inventario se resta del catálogo [!DNL Commerce].

- **[!UICONTROL Fulfilled by Amazon]**: seleccione si Amazon cumple todos los pedidos. Con esta opción, el inventario de productos no se resta del catálogo [!DNL Commerce] cuando se realiza un pedido. Las existencias de inventario para los pedidos satisfechos de Amazon se almacenan y deducen de sus almacenes. Antes de asignar esta opción, debe comprobar en su cuenta de [!DNL Amazon Seller Central] que sus productos cumplen los requisitos para el cumplimiento de _Cumplido por Amazon_ (FBA). El inventario de FBA se administra directamente a través de su cuenta de [!DNL Amazon Seller Central]. Con este método de cumplimiento, el canal de ventas de Amazon no comparte actualizaciones cuantitativas entre [!DNL Commerce] y Amazon. Por lo tanto, no todas las herramientas de marketing descritas en la configuración de cantidad están disponibles en el canal de ventas de Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**: si es posible que usted y Amazon completen sus productos, es posible que desee crear un atributo de producto [!DNL Commerce] con valores para Satisfecho por el comerciante y Satisfecho por Amazon. La configuración de este valor por producto indica quién cumple los pedidos.

El método de cumplimiento es un atributo regional y se basa en la configuración **[!UICONTROL Amazon Marketplace Country]** definida durante la [integración de almacén](./store-integration.md). Cuando se realice un cambio, este afectará a todos los anuncios de Amazon que compartan ese(a) [!DNL Amazon Seller SKU] en sus tiendas Amazon que vendan en la misma región (tal como se define en _[!UICONTROL Amazon Marketplace Country]_durante [integración de tiendas](./store-integration.md)). Un cambio en un(a) [!DNL Amazon Seller SKU] compartido(a) en Estados Unidos no afecta el conjunto de tiendas Amazon para una región diferente (como se definió durante la integración de la tienda).

>[!NOTE]
>
>Cuando Amazon (FBA) completa un pedido y este se importa, puede ver datos ficticios de algunos campos en los detalles del pedido. Ver [detalles del pedido de Amazon](./amazon-order-details.md).

## Configurar la configuración de [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección _[!UICONTROL Fulfilled By]_.

1. Para **[!UICONTROL Product Fulfilled By]**, elija quién cumple (envía) el pedido:

   - `Fulfilled by Merchant` - El comerciante cumple el pedido.

   - `Fulfilled by Amazon`: Amazon data warehouse cumple el pedido.

   - `Assign Fulfilled By Using Magento Product Attribute` - Un atributo [!DNL Commerce] indica quién cumple el pedido por producto.

     Si se elige, elija el atributo [!DNL Commerce] que desea asignar en **[!UICONTROL Fulfilled by Attribute]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Satisfecho Por La Configuración](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| Campo | Descripción |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | Opciones:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Elija si desea cumplir los pedidos. Cuando se realiza un pedido, el inventario se resta del catálogo [!DNL Commerce]. Cuando se crea un nuevo producto, se asigna el método de cumplimiento de Merchant Fulfilled.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Elija si Amazon cumple los pedidos. Con este método de cumplimiento, el inventario de productos no se resta del catálogo [!DNL Commerce] cuando se realiza un pedido. Cuando se crea un producto, se crea con _[!UICONTROL Fulfilled by Amazon (FBA)]_como tipo de cumplimiento. Asegúrese de que sus productos cumplen los requisitos para el cumplimiento de FBA en su cuenta de [!DNL Amazon Seller Central]. El inventario de FBA también se administra directamente a través de su cuenta de [!DNL Amazon Seller Central]. Con este método de cumplimiento, las actualizaciones de cantidad no se insertan en relación con el catálogo [!DNL Commerce], por lo que no puede utilizar algunas de las herramientas de marketing descritas en [Configuración de stock/cantidad](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**: elija si tiene un atributo [!DNL Commerce] existente que determine si el comerciante lo cumple o Amazon lo completa. Cuando se elige **[!UICONTROL Fulfilled by Attribute]** habilita.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Elija el atributo [!DNL Commerce] utilizado para determinar el método de cumplimiento.<br><br>Por ejemplo, si el atributo es _Satisfecho por_ y elige el valor del atributo como `Fulfilled By Merchant` o `Fulfilled By Amazon (FBA)`, el sistema utilizará ese valor como el tipo de satisfacción para un nuevo producto. Como comerciante, debe asegurarse de que sus productos cumplen los requisitos para recibir la certificación FBA en su cuenta de [!DNL Amazon Seller Central]. El inventario de FBA también se administra directamente a través de su cuenta de vendedor de Amazon.<br><br>Las opciones dependen de los atributos que haya configurado para sus productos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
