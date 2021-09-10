---
title: Cancelar un pedido sin enviar
description: Cancele un pedido pendiente o parcialmente enviado (no enviado) a través de su cuenta de Amazon [!DNL Seller Central] .
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Cancelar un pedido sin enviar

Los pedidos de Amazon solo se pueden cancelar si están en estado `Unshipped`. Si el pedido está pendiente o parcialmente enviado (no enviado), el pedido solo se puede cancelar a través de su cuenta [!DNL Amazon Seller Central]. Si el artículo se ha enviado, las devoluciones y los intercambios también deben gestionarse en su cuenta [!DNL Amazon Seller Central].

>[!NOTE]
>
>Para tareas que no sean la cancelación de un pedido:
>
>- Si tiene [habilitada la importación de pedidos](./order-settings.md), los pedidos se administran en el flujo de trabajo [[!DNL Commerce] pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- Si [order import](./order-settings.md) está deshabilitado, debe administrar sus pedidos en [!DNL Amazon Seller Central].


## Cancelar un pedido en estado `Unshipped`

1. Haga clic **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En la sección _[!UICONTROL Recent Orders]_del panel de almacenamiento, haga clic en un número de pedido.

   Aparece la página _[!UICONTROL Amazon Order Details]_.

1. Haga clic **[!UICONTROL Cancel Order]** en la barra de encabezado.

   Esta opción solo aparece para pedidos en estado `Unshipped`.

1. Para **[!UICONTROL Reason for cancellation]**, elija una opción.

1. Haga clic en **[!UICONTROL Confirm]**.

   El pedido se cancela y el estado se actualiza a `Canceled` en los detalles del pedido.

La notificación de cancelación se envía a su cuenta [!DNL Amazon Seller Central] y también se notifica al cliente asociado con la solicitud. El estado del orden [!DNL Commerce] correspondiente, si lo hay, cambia a `Complete`.
