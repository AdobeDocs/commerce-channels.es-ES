---
title: Procesamiento de pedidos
description: Instrucciones de envío y cancelación [!DNL Walmart Marketplace] pedidos de Adobe Commerce y Magento Open Source.
source-git-commit: 90ccbecd6d1433ae1312d79f7ae2d34c8f381b97
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# Procesamiento de pedidos

Si utiliza Adobe Commerce y Magento Open Source Order Management para administrar su [!DNL Commerce] almacenar ventas, proceso [!DNL Walmart Marketplace] pedidos de Commerce con un flujo de trabajo similar.

Cuando se procesa un pedido en Commerce, el Administrador de canales sincroniza las actualizaciones con [!DNL Walmart Marketplace]. Esta actualización garantiza que el estado de pedido y la información de envío de Commerce coincidan con los datos rastreados en la variable [!DNL Walmart Marketplace].

* **Pedidos de envíos**-Walmart requiere un número de seguimiento para todos los envíos. Si la cantidad de stock es insuficiente para rellenar un pedido completo, se crea un envío parcial. Después de enviar el envío, las actualizaciones de los pedidos se sincronizan con [!DNL Walmart Marketplace]. Luego, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

* **Cancelaciones de pedidos**-Al cancelar un [!DNL Walmart Marketplace] pedido, Walmart requiere una razón de cancelación. El motivo de la cancelación se incluye en el aviso de cancelación del pedido enviado al cliente. El motivo de la cancelación también se muestra en la [!DNL Commerce] solicitar información de pagos.

>[!NOTE]
>
> Puede transcurrir hasta cinco minutos hasta que las actualizaciones de pedidos se sincronicen con [!DNL Walmart Marketplace]. Para comprobar el estado del pedido, vuelva a la [!DNL Channel Manager] página Pedidos .

## Enviar un pedido

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de ventas.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL *Orders]**.

1. En la tabla Pedidos, abra el pedido que desea enviar seleccionando la opción **Número de pedido de comercio**.

1. Cree y envíe un envío para la totalidad o parte de un pedido seleccionando **[!UICONTROL Ship]**.

   ![Vista de detalles de un pedido de Walmart Marketplace](assets/order-detail-with-external-order-id.png)

   * Para elegir un transportista de envío y añadir un número de seguimiento, seleccione **[!UICONTROL Add tracking number]**.

   * Rellene el resto del formulario de envío según sea necesario. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obtener instrucciones detalladas.

1. Después de enviar el envío, realice un seguimiento de la variable [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace].

## Cancelar una solicitud

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de venta.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL *Orders]**.

1. En la tabla Pedidos, abra la página de detalles del pedido seleccionando la opción **Número de pedido de comercio** para la orden de cancelación.

![Vista de detalles de un pedido de Walmart Marketplace](assets/order-detail-with-external-order-id.png)

1. Cancelar el pedido.

   * Select **Cancelar** en el menú Detalle del pedido.

   * En el [!UICONTROL Cancel Order] seleccione **Motivo de cancelación**.

   ![Vista de detalles de un pedido de Walmart Marketplace](assets/cancel-order-reason-selector.png)

   * Select **Cancelar pedido**.


1. Compruebe que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace] comprobando el [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager].
