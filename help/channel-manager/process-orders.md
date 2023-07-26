---
title: Procesar pedidos
description: '''Instrucciones de envío y cancelación [!DNL Walmart Marketplace] pedidos de Adobe Commerce y Magento Open Source."'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Procesar pedidos

Después [!DNL Walmart Marketplace] los pedidos se han reconocido y enviado correctamente a [!DNL Channel Manager], se utiliza [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) para procesar la solicitud.

El Administrador de canales sincroniza las actualizaciones con [!DNL Walmart Marketplace] para garantizar que el estado del pedido y la información de envío de [!DNL Commerce] coincide con los datos rastreados en la variable [!DNL Walmart Marketplace].

* **Envíos de pedidos**- Walmart requiere un número de seguimiento para todos los envíos. Si algunos artículos están agotados, puede crear envíos parciales para enviar los artículos que están disponibles actualmente. Después de enviar el envío, las actualizaciones de pedidos se sincronizan con [!DNL Walmart Marketplace]. A continuación, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

* **Cancelaciones de pedidos**-Cuando se cancela un [!DNL Walmart Marketplace] Para realizar el pedido, Walmart requiere un motivo de cancelación que se incluye en el aviso de cancelación del pedido enviado al cliente. El motivo de la cancelación también se muestra en la [!DNL Commerce] información de pagos del pedido. Después de enviar la cancelación, las actualizaciones de inventario se sincronizan con [!DNL Walmart Marketplace]. A continuación, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

  En la tienda, debe cancelar todo el pedido. [!DNL Commerce] no permite cancelaciones parciales.

* **Solicitud de reembolso**-Si se solicita una devolución de Walmart Marketplace para un pedido enviado, la [!UICONTROL Status details] incluye un vínculo a la devolución. Las devoluciones y reembolsos se gestionan desde el [Devuelve](return-refund-orders.md) panel.

Cuando se procesan los pedidos de Commerce y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envíos, envíos parciales y cancelaciones con el [!DNL Walmart Marketplace], el procesamiento del pedido ha finalizado. Las solicitudes de devolución y los reembolsos de los pedidos enviados se administran desde el [Devuelve](return-refund-orders.md) panel.

>[!NOTE]
>
> Las actualizaciones de pedidos pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Para comprobar el estado del pedido, vuelva a la [!DNL Channel Manager] Página Pedidos.

## Envío de un pedido

1. En Admin, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione **[!UICONTROL Orders]**.

1. En la tabla Orders, abra el pedido que desea enviar seleccionando la **[!UICONTROL Commerce Order Number]**.

1. Cree y envíe un envío para la totalidad o parte de un pedido seleccionando **[!UICONTROL Ship]**.

   ![Vista de detalles de pedido comercial para un [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Seleccione un transportista y añada un número de seguimiento seleccionando **[!UICONTROL Add tracking number]**.

     ![Vista de detalles de pedido comercial para un [!DNL Walmart Marketplace] pedido](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Complete el resto del formulario de envío según sea necesario. Consulte [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) para obtener instrucciones detalladas.

1. Después de enviar el envío, realice un seguimiento de [estado del pedido](manage-orders.md#about-order-status) in [!DNL Channel Manager] para verificar que las actualizaciones se han enviado a [!DNL Walmart Marketplace].

Después de enviar un pedido, puede procesar los reembolsos completos o parciales desde [!DNL Channel Manager] para artículos incluidos en el pedido en función de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]. Consulte [Pedidos de devolución y reembolso](return-refund-orders.md).

## Cancelar un pedido

1. En Admin, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de la tienda seleccionando el icono en forma de ojo de una tienda de canales de venta.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL Orders]**.

1. En la tabla Orders, abra el [página de detalles del pedido](manage-orders.md#view-order-detail) seleccionando la opción **[!UICONTROL Commerce Order Number]** para la orden de cancelación.

   ![Vista de detalles de pedido comercial para un[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Cancele el pedido.

   * Seleccionar **Cancelar** en el menú Detalles del pedido.

   * En el [!UICONTROL Cancel Order] , seleccione la **[!UICONTROL Cancellation reason]**.

   ![Vista de detalles de pedido comercial para un [!DNL Walmart Marketplace] pedido](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Seleccionar **[!UICONTROL Cancel Order]**.

1. Después de enviar la cancelación, realice un seguimiento de [estado del pedido](manage-orders.md#about-order-status) in [!DNL Channel Manager] para verificar que las actualizaciones se han enviado a [!DNL Walmart Marketplace].

## Corrección de errores de pedidos

Pueden producirse errores durante el proceso de sincronización de pedidos desde [!DNL Walmart Marketplace]o durante el proceso de actualización de pedidos para envíos, envíos parciales y cancelaciones.

Si la operación de sincronización de un envío, envío parcial o actualización de la cancelación falla, el [!DNL Channel Manager] La página Pedidos muestra un _Error_ estado del pedido. Para asegurarse de que la información de envío y la información de cancelación del pedido se reflejen con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su [!DNL Walmart Marketplace] tienda.


