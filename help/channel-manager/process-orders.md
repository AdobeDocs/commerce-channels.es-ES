---
title: Procesar pedidos
description: 'Instrucciones para enviar y cancelar  [!DNL Walmart Marketplace] pedidos de Adobe Commerce y Magento Open Source.'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Procesar pedidos

Después de que se hayan reconocido [!DNL Walmart Marketplace] pedidos y se hayan enviado correctamente a [!DNL Channel Manager], usa [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) para procesar el pedido.

El Administrador de canales sincroniza las actualizaciones de [!DNL Walmart Marketplace] para garantizar que el estado del pedido y la información de envío de [!DNL Commerce] coincidan con los datos rastreados en [!DNL Walmart Marketplace].

* **Envíos de pedidos**-Walmart requiere un número de seguimiento para todos los envíos. Si algunos artículos están agotados, puede crear envíos parciales para enviar los artículos que están disponibles actualmente. Después de enviar el envío, las actualizaciones de pedidos se sincronizan con [!DNL Walmart Marketplace]. A continuación, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

* **Cancelaciones de pedidos**-Cuando cancela un pedido de [!DNL Walmart Marketplace], Walmart requiere un motivo de cancelación que se incluye en el aviso de cancelación de pedido enviado al cliente. El motivo de la cancelación también se muestra en la información de pagos del pedido [!DNL Commerce]. Después de enviar la cancelación, las actualizaciones de inventario se sincronizan con [!DNL Walmart Marketplace]. A continuación, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

  En la tienda, debe cancelar todo el pedido. [!DNL Commerce] no permite cancelaciones parciales.

* **Solicitud de reembolso**: si se solicita una devolución de Walmart Marketplace para un pedido enviado, [!UICONTROL Status details] incluye un vínculo a la devolución. Las devoluciones y reembolsos se administran desde el panel [Devuelve](return-refund-orders.md).

Cuando se procesan los pedidos de Commerce y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envío, envío parcial y cancelación con el [!DNL Walmart Marketplace], se completa el procesamiento del pedido. Las solicitudes de devolución y los reembolsos de los pedidos enviados se administran desde el panel [Devuelve](return-refund-orders.md).

>[!NOTE]
>
> Las actualizaciones de pedidos pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Para comprobar el estado del pedido, vuelva a la página [!DNL Channel Manager] pedidos.

## Envío de un pedido

1. En el Administrador, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione **[!UICONTROL Orders]**.

1. En la tabla Pedidos, abra el pedido que desea enviar seleccionando **[!UICONTROL Commerce Order Number]**.

1. Cree y envíe un envío para todo o parte de un pedido seleccionando **[!UICONTROL Ship]**.

   ![Vista de detalles de pedido Commerce para un pedido [!DNL Walmart Marketplace]](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Elija un transportista y agregue un número de seguimiento seleccionando **[!UICONTROL Add tracking number]**.

     ![Vista de detalles de pedido Commerce para un pedido [!DNL Walmart Marketplace]](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Complete el resto del formulario de envío según sea necesario. Consulte [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) para obtener instrucciones detalladas.

1. Después de enviar el envío, realiza un seguimiento del [estado del pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que se hayan enviado actualizaciones a [!DNL Walmart Marketplace].

Una vez enviado el pedido, puede procesar los reembolsos totales o parciales de [!DNL Channel Manager] de los artículos incluidos en el pedido en función de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]. Ver [Pedidos de devolución y reembolso](return-refund-orders.md).

## Cancelar un pedido

1. En el Administrador, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de la tienda seleccionando el icono en forma de ojo de una tienda de canales de venta.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL Orders]**.

1. En la tabla Pedidos, abra la [página de detalles del pedido](manage-orders.md#view-order-detail) seleccionando **[!UICONTROL Commerce Order Number]** para el pedido que desea cancelar.

   ![Vista de detalles del pedido de Commerce para un[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Cancele el pedido.

   * Seleccione **Cancelar** en el menú Detalles del pedido.

   * En el formulario [!UICONTROL Cancel Order], seleccione **[!UICONTROL Cancellation reason]**.

   ![Vista de detalles de pedido Commerce para un pedido [!DNL Walmart Marketplace]](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Seleccione **[!UICONTROL Cancel Order]**.

1. Después de enviar la cancelación, realiza un seguimiento del [estado del pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que se hayan enviado actualizaciones a [!DNL Walmart Marketplace].

## Corrección de errores de pedidos

Pueden producirse errores durante el proceso de sincronización de pedidos de [!DNL Walmart Marketplace] o durante el proceso de actualización de pedidos para envíos, envíos parciales y cancelaciones.

Si la operación de sincronización para un envío, envío parcial o actualización de cancelación falla, la página [!DNL Channel Manager] Pedidos muestra el estado _Error_ para el pedido. Para asegurarse de que la información de envío y la información de cancelación de pedidos se reflejen con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su tienda [!DNL Walmart Marketplace].


