---
title: Detalles del pedido de Amazon
description: Vea los detalles de sus pedidos de Amazon Marketplace en Adobe Commerce o en el administrador de Magento Open Source.
feature: Sales Channels, Orders
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Detalles del pedido de Amazon

![Detalles del pedido de Amazon](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## Ver detalles del pedido de Amazon

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En la sección _[!UICONTROL Recent Orders]_, haga clic en un número de pedido.

   Se abre la página _[!UICONTROL Amazon Order Details]_.

>[!NOTE]
>
>Si tiene habilitada la importación de pedidos en [Configuración de pedidos](./order-settings.md) y Amazon (FBA)](./fulfilled-by.md) completa el pedido, es posible que vea datos ficticios de algunos campos en los detalles del pedido. [ Amazon no envía los siguientes datos para pedidos de FBA.
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`

### Pestaña Detalles del pedido y el envío

La ficha _[!UICONTROL Order and Shipping Details]_muestra información detallada del pedido, tal como se recibió de Amazon.

>[!IMPORTANT]
>
>Amazon acepta información de direcciones no estándar que no se puede importar al canal de ventas de Amazon, lo que impide que los códigos de estado/país se actualicen correctamente en algunos pedidos. Para corregir errores de dirección, los siguientes campos pueden editarse en los detalles del pedido:
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>No olvide hacer clic en **Guardar pedido** después de realizar las modificaciones.

![Detalles de pedido y envío](assets/amazon-order-details.png){width="600" zoomable="yes"}

### Pestaña Ordenar elementos

La ficha _[!UICONTROL Order Items]_muestra todos los elementos asociados con el pedido de Amazon, tal como se recibieron de Amazon.

![Detalles del artículo de pedido](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### Pestaña Seguimiento

La pestaña _[!UICONTROL Tracking]_muestra información de seguimiento asociada con el pedido de Amazon.

![Detalles de seguimiento](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
