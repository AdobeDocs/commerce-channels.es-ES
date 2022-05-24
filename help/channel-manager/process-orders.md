---
title: Procesamiento de pedidos
description: Instrucciones de envío y cancelación [!DNL Walmart Marketplace] pedidos de Adobe Commerce y Magento Open Source.
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Procesamiento de pedidos

Si utiliza Adobe Commerce y Magento Open Source Order Management para administrar su [!DNL Commerce] almacenar ventas, procesar [!DNL Walmart Marketplace] pedidos de Commerce con un flujo de trabajo similar.

Cuando se procesa un pedido en Commerce, el Administrador de canales sincroniza las actualizaciones con [!DNL Walmart Marketplace]. Esta actualización garantiza que el inventario de productos y el estado de los pedidos de Commerce coincidan con los datos rastreados en la variable [!DNL Walmart Marketplace] y notifica a Walmart que envíe información de estado de pedido y envío a los clientes.

>[!NOTE]
>
> Las actualizaciones de pedidos pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Para comprobar el estado del pedido, vuelva a [!DNL Channel Manager] Pedidos.

## Enviar un pedido

Cuando envía un pedido desde Commerce, usa la variable [[!DNL Commerce Order Management] flujo de trabajo de envío](https://docs.magento.com/user-guide/sales/order-ship.html). Después de enviar la solicitud, las actualizaciones se sincronizan con [!DNL Walmart Marketplace]. Luego, Walmart notifica a los clientes sobre el estado del pedido y los detalles de envío.

**Requisito previo**

Antes de enviar los pedidos, compruebe que la variable [configuración de envío de canal y de operador de telefonía](map-shipping-carriers.md) meet [!DNL Walmart Marketplace requirements].

### Creación y envío del envío

Cuando envía un [!DNL Walmart Marketplace] pedido de [!DNL Commerce], debe agregar un número de seguimiento. Los clientes reciben el número de seguimiento en la notificación de envío de la que reciben [!DNL Walmart].

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir el [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de ventas.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL *Orders]**.

1. En la tabla Pedidos, abra el pedido que desea enviar seleccionando la opción **Número de pedido de comercio**.

1. Cree y envíe un envío para la totalidad o parte de un pedido seleccionando **[!UICONTROL Ship]**.

   - Para elegir un transportista de envío y añadir un número de seguimiento, seleccione **[!UICONTROL Add tracking number]**.

   - Rellene el resto del formulario de envío según sea necesario. Consulte [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) para obtener instrucciones detalladas.

1. Después de enviar el envío, realice un seguimiento de la variable [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager] para verificar que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace].

## Cancelar una solicitud

Al cancelar una [!DNL Walmart Marketplace] pedido, Walmart requiere una razón de cancelación. Cuando la cancelación del pedido se actualiza a Walmart, el motivo de la cancelación se incluye en el aviso de cancelación enviado al cliente.

El motivo de la cancelación también se muestra en la [!DNL Commerce] solicitar información de pagos.

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir el [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de venta.

1. Para ver [!DNL Walmart Marketplace] pedidos, seleccione *[!UICONTROL *Orders]**.

1. En la tabla Pedidos, abra la página de detalles del pedido seleccionando la opción **Número de pedido de comercio** para la orden de cancelación.

   ![Vista de detalles de un pedido de Walmart Marketplace](assets/order-detail-with-external-order-id.png)

1. Cancelar el pedido.

   - Select **Cancelar** en el menú Detalle del pedido.

   - En el formulario Cancelar pedido , seleccione la opción **Motivo de cancelación**.

      ![Vista de detalles de un pedido de Walmart Marketplace](assets/order-detail-with-external-order-id.png)

   - Select **Cancelar pedido**.

1. Compruebe que las actualizaciones se hayan enviado a [!DNL Walmart Marketplace] comprobando el [estado de pedido](manage-orders.md#about-order-status) en [!DNL Channel Manager].
