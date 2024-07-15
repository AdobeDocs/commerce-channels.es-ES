---
title: Cancelar un pedido de Amazon sin enviar
description: Cancela un pedido pendiente o parcialmente enviado (no enviado) a través de tu cuenta de Amazon [!DNL Seller Central] .
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# Cancelar un pedido de Amazon sin enviar

Los pedidos de Amazon solo se pueden cancelar si se encuentran en un estado de `Unshipped`. Si el pedido está pendiente o parcialmente enviado (no enviado), el pedido solo se puede cancelar a través de su cuenta de [!DNL Amazon Seller Central]. Si el artículo se ha enviado, las devoluciones y los cambios también deben realizarse en la cuenta de [!DNL Amazon Seller Central].

>[!NOTE]
>
>Para tareas que no sean cancelar una solicitud:
>
>- Si tiene [importación de pedidos](./order-settings.md) habilitada, los pedidos se administran en el [[!DNL Commerce] flujo de trabajo de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- Si [importación de pedidos](./order-settings.md) está deshabilitada, debe administrar sus pedidos en [!DNL Amazon Seller Central].

## Cancelar un pedido en estado `Unshipped`

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En la sección _[!UICONTROL Recent Orders]_del panel de almacén, haga clic en un número de pedido.

   Aparecerá la página _[!UICONTROL Amazon Order Details]_.

1. Haga clic en **[!UICONTROL Cancel Order]** en la barra de encabezado.

   Esta opción solo aparece para pedidos con estado `Unshipped`.

1. Para **[!UICONTROL Reason for cancellation]**, elija una opción.

1. Haga clic en **[!UICONTROL Confirm]**.

   El pedido se canceló y el estado se actualizó a `Canceled` en los detalles del pedido.

La notificación de cancelación se enviará a su cuenta de [!DNL Amazon Seller Central] y también se notificará al cliente asociado con el pedido. El estado del pedido [!DNL Commerce] correspondiente, si lo hay, cambia a `Complete`.
