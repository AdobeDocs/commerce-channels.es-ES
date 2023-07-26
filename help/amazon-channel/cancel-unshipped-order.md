---
title: Cancelar un pedido de Amazon sin enviar
description: Cancelar un pedido pendiente o parcialmente enviado (no enviado) a través de su Amazon [!DNL Seller Central] cuenta.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Cancelar un pedido de Amazon sin enviar

Los pedidos de Amazon solo se pueden cancelar si están en un `Unshipped` estado. Si el pedido está pendiente o parcialmente enviado (no enviado), el pedido solo se puede cancelar a través de [!DNL Amazon Seller Central] cuenta. Si el artículo ha sido enviado, las devoluciones y los cambios también deben ser manejados en su [!DNL Amazon Seller Central] Cuenta.

>[!NOTE]
>
>Para tareas que no sean cancelar una solicitud:
>
>- Si tiene [importación de pedidos](./order-settings.md) si está activada, los pedidos se administran en [[!DNL Commerce] flujo de trabajo pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- If [importación de pedidos](./order-settings.md) está desactivado, debe gestionar sus pedidos en [!DNL Amazon Seller Central].

## Cancelar un pedido en `Unshipped` status

1. Clic **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el _[!UICONTROL Recent Orders]_del panel de tienda, haga clic en un número de pedido.

   El _[!UICONTROL Amazon Order Details]_página.

1. Clic **[!UICONTROL Cancel Order]** en la barra de encabezado.

   Esta opción solo aparece para pedidos en `Unshipped` estado.

1. Para **[!UICONTROL Reason for cancellation]**, elija una opción.

1. Clic **[!UICONTROL Confirm]**.

   El pedido se cancela y el estado se actualiza a `Canceled` en los detalles del pedido.

La notificación de cancelación se envía a su [!DNL Amazon Seller Central] y también se notifica al cliente asociado con el pedido. El estado del correspondiente [!DNL Commerce] Si hay algún cambio, solicite. `Complete`.
