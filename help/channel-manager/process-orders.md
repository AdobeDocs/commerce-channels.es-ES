---
title: Procesamiento de Pedidos
description: '"Instrucciones de envío y cancelación [!DNL Walmart Marketplace] pedidos de Adobe Commerce y Magento Open Source.'''
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Procesamiento de Pedidos

Después [!DNL Walmart Marketplace] los pedidos se han reconocido y enviado correctamente a [!DNL Channel Manager], utilice [Administración de pedidos de comercio](https://docs.magento.com/user-guide/sales/orders-workspace.html) para procesar el pedido.

El Administrador de canales sincroniza las actualizaciones con [!DNL Walmart Marketplace] para garantizar que el estado del pedido y la información de envío [!DNL Commerce] coincide con los datos rastreados en la variable [!DNL Walmart Marketplace].

* **Pedidos de envíos**-Walmart requiere un número de seguimiento para todos los envíos. Si algunos artículos no están en existencias, puede crear envíos parciales para enviar los artículos que están disponibles actualmente. Después de enviar el envío, las actualizaciones de los pedidos se sincronizan con [!DNL Walmart Marketplace]. Luego, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

* **Cancelaciones de pedidos**-Al cancelar un [!DNL Walmart Marketplace] pedido, Walmart requiere un motivo de cancelación que se incluye en el aviso de cancelación de pedido enviado al cliente. El motivo de la cancelación también se muestra en la [!DNL Commerce] solicitar información de pagos. Después de enviar la cancelación, las actualizaciones de inventario se sincronizan con [!DNL Walmart Marketplace]. Luego, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

   En la tienda, debe cancelar todo el pedido. [!DNL Commerce] no permite cancelaciones parciales.

* **Solicitud de reembolso**-Si se solicita una devolución de Walmart para un pedido enviado, la variable [!UICONTROL Status details] incluye un vínculo al retorno. Las devoluciones y los reembolsos se administran desde [Devuelve](return-refund-orders.md) tablero.

Cuando se procesan los pedidos comerciales y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envío, envío parcial y cancelación a la variable [!DNL Walmart Marketplace], se ha completado el procesamiento de la solicitud. Las solicitudes de devolución y los reembolsos de los pedidos enviados se administran desde el [Devuelve](return-refund-orders.md) tablero.

>[!NOTE]
>
> Las actualizaciones de pedidos pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Para comprobar el estado del pedido, vuelva a la [!DNL Channel Manager] página Pedidos .

## Enviar un pedido

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de ventas.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccionar **[!UICONTROL Orders]**.

1. En la tabla Pedidos, abra el pedido que desea enviar seleccionando la opción **Número de pedido de comercio**.

1. Cree y envíe un envío para la totalidad o parte de un pedido seleccionando **[!UICONTROL Ship]**.

   ![Vista de detalles de pedidos de comercio para un [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

   * Seleccione un transportista y añada un número de seguimiento seleccionando **[!UICONTROL Add tracking number]**.

      ![Vista de detalles de pedidos de comercio para un [!DNL Walmart Marketplace] pedido](assets/order-shipment-add-tracking-number.png)


   * Rellene el resto del formulario de envío según sea necesario. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obtener instrucciones detalladas.

1. Después de enviar el envío, realice un seguimiento de la variable [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace].

Después de enviar un pedido, puede procesar los reembolsos completos o parciales desde [!DNL Channel Manager] para elementos incluidos en el pedido en función de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]. Consulte [órdenes de devolución y devolución](return-refund-orders.md).

## Cancelar una solicitud

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de venta.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL *Orders]**.

1. En la tabla Pedidos, abra el [página de detalles del pedido](manage-orders.md#view-order-detail) seleccionando **Número de pedido de comercio** para la orden de cancelación.

   ![Vista de detalles de pedidos de comercio para un[!DNL Walmart Marketplace]pedido](assets/order-detail-with-external-order-id.png)

1. Cancelar el pedido.

   * Select **Cancelar** en el menú Detalle del pedido.

   * En el [!UICONTROL Cancel Order] seleccione **Motivo de cancelación**.
   ![Vista de detalles de pedidos de comercio para un [!DNL Walmart Marketplace] pedido](assets/cancel-order-reason-selector.png)

   * Select **Cancelar pedido**.


1. Después de enviar la cancelación, realice un seguimiento de la [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace].

## Corrección de errores de orden

Los errores pueden producirse durante el proceso de sincronización de pedidos desde [!DNL Walmart Marketplace], o durante el proceso de actualización de pedidos para envíos, envíos parciales y cancelaciones.

Si falla la operación de sincronización para un envío, envío parcial o actualización de cancelación, se llama a [!DNL Channel Manager] La página Pedidos muestra un _Error_ para el pedido. Para garantizar que la información de envío y la información de cancelación de pedidos se reflejen con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su [!DNL Walmart Marketplace] tienda.


