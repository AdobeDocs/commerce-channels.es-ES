---
title: Cancelar un pedido sin enviar
description: Cancelar un pedido pendiente o parcialmente enviado (no enviado) a través de su Amazon [!DNL Seller Central] cuenta.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cancelar un pedido sin enviar

Los pedidos de Amazon solo se pueden cancelar si se encuentran en una `Unshipped` estado. Si el pedido está pendiente o parcialmente enviado (sin enviar), el pedido solo se puede cancelar a través de su [!DNL Amazon Seller Central] cuenta. Si el artículo se ha enviado, las devoluciones y los intercambios también deben gestionarse en su [!DNL Amazon Seller Central] Cuenta.

>[!NOTE]
>
>Para tareas que no sean la cancelación de un pedido:
>
>- Si tiene [importación de pedidos](./order-settings.md) activada, los pedidos se administran en la variable [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- If [importación de pedidos](./order-settings.md) está desactivado, debe administrar sus pedidos en [!DNL Amazon Seller Central].


## Cancelar un pedido en `Unshipped` status

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el _[!UICONTROL Recent Orders]_del panel de almacenamiento, haga clic en un número de pedido.

   La variable _[!UICONTROL Amazon Order Details]_se abre.

1. Haga clic en **[!UICONTROL Cancel Order]** en la barra de encabezado.

   Esta opción solo aparece para los pedidos de `Unshipped` estado.

1. Para **[!UICONTROL Reason for cancellation]**, elija una opción.

1. Haga clic en **[!UICONTROL Confirm]**.

   El pedido se cancela y el estado se actualiza a `Canceled` en los detalles del pedido.

La notificación de cancelación se envía a su [!DNL Amazon Seller Central] también se notifica al cliente asociado con el pedido. El estado del [!DNL Commerce] solicite, si hay, cambios en `Complete`.
