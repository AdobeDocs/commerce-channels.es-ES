---
title: Detalles de pedidos de Amazon
description: Consulte los detalles de sus pedidos de Amazon Marketplace en el administrador de Adobe Commerce o Magento Open Source.
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Detalles de pedido de Amazon

![Detalles de pedido de Amazon](assets/amazon-order-details-header.png)

## Ver detalles de pedidos de Amazon

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el _[!UICONTROL Recent Orders]_, haga clic en un número de pedido.

   La variable _[!UICONTROL Amazon Order Details]_se abre.

>[!NOTE]
>
>Si tiene activada la importación de pedidos en su [Configuración de pedidos](./order-settings.md) y el orden es [cumplido por Amazon (FBA)](./fulfilled-by.md), es posible que vea datos ficticios de algunos campos en los detalles del pedido. Amazon no envía los siguientes datos para los pedidos de FBA.
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


### Pestaña Detalles del pedido y envío

La variable _[!UICONTROL Order and Shipping Details]_muestra la información detallada del pedido recibida de Amazon.

>[!IMPORTANT]
>
>Amazon acepta información de direcciones no estándar que no se puede importar en el canal de ventas de Amazon, lo que evita que los códigos de estado/país se actualicen correctamente para algunos pedidos. Para corregir los errores de dirección, los campos siguientes se pueden editar en los detalles del pedido:
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>No olvide hacer clic en **Guardar orden** después de realizar ediciones.

![Detalles de pedidos y envíos](assets/amazon-order-details.png)

### Ficha Ordenar elementos

La variable _[!UICONTROL Order Items]_muestra todos los elementos asociados con el pedido de Amazon, tal como se recibieron de Amazon.

![Detalles del artículo del pedido](assets/amazon-order-item-details.png)

### Ficha Tracking

La variable _[!UICONTROL Tracking]_muestra la información de seguimiento asociada al pedido de Amazon.

![Detalles de seguimiento](assets/amazon-order-tracking-details.png)
