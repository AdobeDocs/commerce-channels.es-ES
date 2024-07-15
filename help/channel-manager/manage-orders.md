---
title: 'Ver y administrar pedidos de  [!DNL Channel Manager]'
description: 'Ver y administrar [!DNL Walmart Marketplace] pedidos con [!DNL Channel Manager] para Adobe Commerce y el Magento Open Source.'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Ver y rastrear pedidos de [!DNL Channel Manager]

[!DNL Walmart Marketplace] datos de pedido de [!DNL Commerce] productos se sincroniza automáticamente con [!DNL Channel Manager] después de que [!DNL Walmart] procese el pedido.

En el lado [!DNL Commerce], una sincronización correcta déclencheur las siguientes acciones:

- [!DNL Channel Manager] envía una confirmación de pedido a Walmart.

- Se crea un pedido [!DNL Commerce] correspondiente a partir del pedido de Walmart.

- La información de pedidos actualizada se muestra en el panel [!DNL Channel Manager] pedidos.

En el administrador de tienda, puede ver los datos de pedido de [!DNL Channel Manager] abriendo el almacén del canal de ventas y seleccionando **[!UICONTROL Orders]**.

![Vista de pedidos del administrador de canal para administrar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Puede tardar hasta 35 minutos en mostrarse un pedido de [!DNL Walmart Marketplace] en la lista de pedidos de [!DNL Channel Manager]. [!DNL Walmart] requiere aproximadamente 30 minutos para procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager]. Una vez que Channel Manager recibe la solicitud, se tardan aproximadamente cinco minutos más en crear y mostrar la solicitud en Adobe Commerce o Magento Open Source.

## Controles de pedidos y descripciones de columnas

En las tablas siguientes se describen los controles y las columnas disponibles para Pedidos.

**Controles para[!UICONTROL Orders]**

<table>
<tr>
<td><strong>Control</strong></td>
<td><strong>Descripción</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Ordene la vista seleccionando una de las [!UICONTROL Order Status] tarjetas.</td>
</tr>
<tr>
<td>Detalles del estado</td>
<td>Proporciona información sobre errores de pedidos y solicitudes de devolución. Para ver la información de devolución y el estado de devolución de un pedido, seleccione el texto <strong>[!UICONTROL Return requested]</strong> para abrir el panel [!UICONTROL Returns].</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para ver los detalles del pedido, seleccione el número de pedido [!DNL Commerce] en la tabla [!UICONTROL Order]. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar la configuración del canal, seleccione las credenciales de la conexión Walmart del canal, los atributos asignados o los identificadores de envío, la configuración selecciona el número de pedido [!DNL Commerce] en la tabla [!UICONTROL Order]. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
</tr>
</table>


**Descripciones de columna**

<table>
<tr>
<td>Campo</td>
<td>Descripción</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>Número de pedido de compra asignado al pedido en [!DNL Walmart Marketplace]. Cuando se importa un pedido inicialmente a [!DNL Channel Manager], solo se muestra el número de pedido [!DNL Walmart]. Cuando se crea el pedido [!DNL Commerce], el número de pedido [!DNL Walmart] se almacena en el atributo de producto [!UICONTROL External ID].</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº de pedido</td>
<td>Número asignado al pedido [!DNL Commerce] creado a partir del pedido [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>Elementos</td>
<td>Número de elementos pedidos en [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Coste total de los artículos pedidos.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>Fecha en la que se envió el pedido a [!DNL Walmart Marketplace] convertido a la zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>La fecha en la que debe enviarse el pedido para cumplir los requisitos de [!DNL Walmart Marketplace] convertidos a la zona horaria local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>La fecha en la que se debe entregar el pedido al cliente para cumplir los requisitos de [!DNL Walmart Marketplace] convertidos a la zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>El [[!DNL Walmart Marketplace] método de envío](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 seleccionado para el pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Marca de tiempo que indica la última vez que se actualizaron los datos de pedido en [!DNL Channel Manager] convertidos a la zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica el estado de pedido actual en el flujo de trabajo de pedido [!DNL Commerce]. El estado inicial de un pedido importado de [!DNL Walmart Marketplace] es _Open_. Se producen actualizaciones de estado adicionales cuando se procesan [!DNL Commerce] pedidos y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envío, envío parcial y cancelación con [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Proporciona información más detallada sobre los pedidos con errores o solicitudes de reembolso.</td>
</tr>
</table>

## Estado del pedido

[!UICONTROL Order Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] pedidos administrados desde Adobe Commerce o Magento Open Source. Las actualizaciones del estado de los pedidos se producen cuando [!DNL Channel Manager] recibe información actualizada del pedido del sistema de pedidos [!DNL Walmart Marketplace] o [!DNL Commerce]. Los pedidos pueden tener los siguientes estados:

- **[!UICONTROL Shipped]**: pedidos enviados desde el almacén [!DNL Commerce]. Cuando se envíe el pedido, [!DNL Channel Manager] enviará una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío en Walmart y proporcionar el número de seguimiento del pedido para el envío. Una vez enviado un pedido, los artículos de pedido pueden ser reembolsados parcial o totalmente si Walmart emite un formulario de autorización de devolución de mercancía. Ver [devoluciones y reembolsos](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**: pedidos que tienen algunos artículos marcados como enviados y otros que esperan ser enviados. Cuando los artículos del pedido se envían, [!DNL Channel Manager] envía una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío a _[!DNL Partially Shipped]_en Walmart y proporcionar el número de seguimiento del pedido para el envío.

- **[!UICONTROL Canceled]**: pedidos que se han cancelado del almacén [!DNL Commerce].

  Una vez finalizada la cancelación del pedido, la cantidad de existencias [!DNL Commerce] se actualiza para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**: si Walmart Marketplace solicita una devolución para los artículos de pedido que se han enviado, aparece un vínculo `Return requested` en la columna [!UICONTROL Status details]. Al seleccionar el vínculo, se abre el panel [!UICONTROL Returns] para ver la devolución y administrar el proceso de devolución.

- **[!UICONTROL Error]**: pedidos con errores. Pueden producirse errores cuando falla una operación de actualización de pedido. Por ejemplo, se producen errores si [!DNL Channel Manager] no puede recibir un nuevo pedido de Walmart. También pueden ocurrir si [!DNL Channel Manager] no puede enviar un envío de pedido o una actualización de cancelación a [!DNL Walmart Marketplace]. Si falla una operación, la página Pedidos muestra el estado _Error_ para el pedido. Para obtener más información, consulte [Corregir errores de pedidos](errores de proceso-pedidos.md#fix-shipping-and-cancelation-).

- **[!UICONTROL Status details]**: proporciona más información sobre los errores de pedidos que se producen debido a problemas como la falta de información o valores no válidos, detalles de envío incorrectos o una cancelación de pedido fallida. La descripción ayuda a determinar si se produjo un error en la instancia [!DNL Commerce] o en [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si los artículos de pedido se envían en varios envíos, el estado del pedido en [!DNL Channel Manager] refleja el último estado de pedido disponible. Por ejemplo, si el primer elemento se envía y no se devuelve ningún error cuando las actualizaciones de pedidos se sincronizan con [!DNL Channel Manager] y [!DNL Walmart Marketplace], el estado del pedido [!DNL Channel Manager] es _[!UICONTROL Partially Shipped]_. Si se envía un segundo artículo y [!DNL Channel Manager] devuelve un error, el estado del pedido se actualiza a_[!UICONTROL Error]_.

## Revisar pedidos

1. En Admin., seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir la página [!UICONTROL Channel Manager Marketplace Stores].

1. Abra la vista de tienda seleccionando el icono en forma de ojo en una fila de entrada de tienda.

1. Para ver la información del pedido, seleccione *[!UICONTROL *Orders]**.

1. Obtenga información sobre el pedido y determine los pasos siguientes comprobando la columna **[Estado](#order-status)**.

## Revisar detalles del pedido

Después de recibir un pedido del mercado e importarlo en su tienda de canales de ventas, use el identificador de pedido [!DNL Commerce] para ver los detalles del pedido en Adobe Commerce.

De **[!UICONTROL Orders]**, seleccione **[!UICONTROL Commerce Order Number]** para abrir los detalles del pedido de [!DNL Commerce].

![Vista de detalles de pedido Commerce para un pedido [!DNL Walmart Marketplace]](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

En la tienda Commerce, los pedidos importados de [!DNL Walmart Marketplace] incluyen la siguiente información adicional en los datos de pedidos:

- **Información de pago y método de envío**: los pedidos importados de Walmart incluyen los siguientes valores para los campos de pago y envío:

   - **[!UICONTROL Offline Channel Payment]**: indica que el pago del pedido se procesa sin conexión por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**: muestra el número de pedido [!DNL Walmart Marketplace].

   - **[!UICONTROL Channel Shipping - Value]**: indica que los gastos de envío se administran a través de [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**: este campo solo se muestra si se cancela un pedido importado de [!DNL Walmart Marketplace]. Los motivos de cancelación incluyen:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Elementos pedidos**: esta sección enumera los elementos de pedido de todos los pedidos de Commerce. La columna [!UICONTROL Qty] proporciona el historial de estado de los elementos de pedido. Por ejemplo, si un pedido se ha facturado, enviado y reembolsado, puede ver las transiciones de estado.

  ![Historial de estado de artículo pedido detallado de pedido [!DNL Walmart Marketplace] pedidos](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Ver los detalles de la factura del artículo y el reembolso seleccionando las opciones [!UICONTROL Invoice] y [!UICONTROL Credit Memo] en el menú de navegación. También puede acceder a la nota de crédito directamente desde el panel [[!UICONTROL Returns]](return-refund-orders.md) de su tienda del canal de ventas.
