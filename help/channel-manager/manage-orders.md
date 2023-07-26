---
title: '"Ver y administrar pedidos desde" [!DNL Channel Manager]'''
description: '''Ver y administrar [!DNL Walmart Marketplace] pedidos con [!DNL Channel Manager] para Adobe Commerce y Magento Open Source".'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Ver y rastrear pedidos de [!DNL Channel Manager]

[!DNL Walmart Marketplace] datos de pedidos de [!DNL Commerce] products se sincroniza automáticamente con [!DNL Channel Manager] después [!DNL Walmart] procesa el pedido.

En el [!DNL Commerce] Una sincronización correcta déclencheur las siguientes acciones:

- [!DNL Channel Manager] envía una confirmación de pedido a Walmart.

- Un correspondiente [!DNL Commerce] El pedido se crea a partir del pedido de Walmart.

- La información actualizada del pedido se muestra en la [!DNL Channel Manager] Panel de pedidos.

En el Administrador de tienda, puede ver los datos de pedidos de [!DNL Channel Manager] abriendo el almacén del canal de ventas y seleccionando **[!UICONTROL Orders]**.

![Vista de pedidos del administrador de canales para administrar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Puede tardar hasta 35 minutos en [!DNL Walmart Marketplace] orden para mostrar en [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] tarda aproximadamente 30 minutos en procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager]. Una vez que Channel Manager recibe la solicitud, se tardan aproximadamente cinco minutos más en crear y mostrar la solicitud en Adobe Commerce o Magento Open Source.

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
<td>Proporciona información sobre errores de pedidos y solicitudes de devolución. Para consultar la información de devolución y el estado de devolución de un pedido, seleccione la <strong>[!UICONTROL Return requested]</strong> texto para abrir [!UICONTROL Returns] panel.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para ver los detalles del pedido, seleccione [!DNL Commerce] número de pedido en [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar la configuración del canal, seleccione las credenciales de la conexión Walmart del canal, los atributos asignados o los identificadores de envío, la configuración seleccione el [!DNL Commerce] número de pedido en [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
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
<td>El número de pedido de compra asignado al pedido en la [!DNL Walmart Marketplace]. Cuando se importa un pedido inicialmente a [!DNL Channel Manager], solo el [!DNL Walmart] se muestra el número de pedido. Si la variable [!DNL Commerce] Cuando se crea el pedido, [!DNL Walmart] El número de pedido se almacena en [!UICONTROL External ID] atributo de producto.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº de pedido</td>
<td>El número asignado al [!DNL Commerce] pedido creado a partir de [!DNL Walmart Marketplace] pedido.</td>
</tr>
<tr>
<td>Elementos</td>
<td>Número de artículos pedidos el [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Coste total de los artículos pedidos.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>La fecha en la que se envió el pedido al [!DNL Walmart Marketplace] convertida a la zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>La fecha en la que debe enviarse el pedido para cumplir [!DNL Walmart Marketplace] requisitos convertidos a la zona horaria local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>La fecha en la que se debe entregar el pedido al cliente para que se cumpla [!DNL Walmart Marketplace] requisitos convertidos a la zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>La [[!DNL Walmart Marketplace] Método de envío](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 seleccionado para el pedido.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Marca de tiempo que indica la última vez que se actualizaron los datos del pedido en [!DNL Channel Manager] convertido a zona horaria local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica el estado de pedido actual en el [!DNL Commerce] flujo de trabajo de pedidos. El estado inicial de un pedido importado de [!DNL Walmart Marketplace] es _Open_. Se producen actualizaciones de estado adicionales cuando [!DNL Commerce] los pedidos se procesan y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envíos, envíos parciales y cancelaciones con el [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Proporciona información más detallada sobre los pedidos con errores o solicitudes de reembolso.</td>
</tr>
</table>

## Estado del pedido

[!UICONTROL Order Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] pedidos gestionados desde Adobe Commerce o Magento Open Source. Las actualizaciones de estado de pedidos se producen cuando [!DNL Channel Manager] recibe información actualizada del pedido de la [!DNL Walmart Marketplace] o el [!DNL Commerce] sistema de pedidos. Los pedidos pueden tener los siguientes estados:

- **[!UICONTROL Shipped]**: pedidos enviados desde el [!DNL Commerce] tienda. Cuando se envíe el pedido, [!DNL Channel Manager] envía una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío en Walmart y proporcionar el número de seguimiento del pedido para el envío. Una vez enviado un pedido, los artículos de pedido pueden ser reembolsados parcial o totalmente si Walmart emite un formulario de autorización de devolución de mercancía. Consulte [Devoluciones y reembolsos](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**: pedidos que tienen algunos artículos marcados como enviados y otros que esperan ser enviados. Cuando los artículos del pedido se envían, [!DNL Channel Manager] envía una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío a _[!DNL Partially Shipped]_en Walmart y proporcione el número de seguimiento del pedido para el envío.

- **[!UICONTROL Canceled]**: pedidos que se han cancelado desde el [!DNL Commerce] tienda.

  Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] actualizaciones de cantidad de stock para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con el [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**: si Walmart Marketplace solicita una devolución para los artículos de pedido que se han enviado, una `Return requested` El vínculo se muestra en [!UICONTROL Status details] columna. Al seleccionar el vínculo, se abre [!UICONTROL Returns] panel para ver la devolución y administrar el proceso de devolución.

- **[!UICONTROL Error]**: los pedidos que tienen errores. Pueden producirse errores cuando falla una operación de actualización de pedido. Por ejemplo, los errores se producen si [!DNL Channel Manager] no puede recibir un nuevo pedido de Walmart. También pueden ocurrir si [!DNL Channel Manager] no puede enviar un envío de pedido o una actualización de cancelación a [!DNL Walmart Marketplace]. Si falla una operación, la página Pedidos muestra un _Error_ estado del pedido. Para obtener más información, consulte [Corrección de errores de pedidos](errores process-orders.md#fix-shipping-and-cancelation-).

- **[!UICONTROL Status details]**: proporciona más información sobre los errores de pedidos que se producen debido a problemas como la falta de información o valores no válidos, detalles de envío incorrectos o una cancelación de pedido fallida. La descripción ayuda a determinar si se ha producido un error en la [!DNL Commerce] o en el [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si los artículos de pedido se envían en varios envíos, el estado del pedido en [!DNL Channel Manager] refleja el último estado de pedido disponible. Por ejemplo, si se envía el primer artículo y no se devuelve ningún error cuando se sincronizan las actualizaciones de pedidos con [!DNL Channel Manager] y [!DNL Walmart Marketplace], el [!DNL Channel Manager] el estado del pedido es _[!UICONTROL Partially Shipped]_. Si se envía un segundo artículo y [!DNL Channel Manager] devuelve un error, el estado del pedido se actualiza a_[!UICONTROL Error]_.

## Revisar pedidos

1. En Admin, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono en forma de ojo en una fila de entrada de tienda.

1. Para ver la información del pedido, seleccione *[!UICONTROL *Orders]**.

1. Obtenga información sobre el pedido y determine los pasos siguientes comprobando la **[Estado](#order-status)** columna.

## Revisar detalles del pedido

Después de recibir un pedido del mercado e importarlo en su tienda de canales de ventas, utilice el [!DNL Commerce] ID de pedido para ver los detalles del pedido en Adobe Commerce.

Desde **[!UICONTROL Orders]**, seleccione la **[!UICONTROL Commerce Order Number]** para abrir [!DNL Commerce] detalle del pedido.

![Vista de detalles de pedido comercial para un [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

En la tienda de Commerce, los pedidos importados de [!DNL Walmart Marketplace] incluya la siguiente información adicional en los datos del pedido:

- **Información de pago y método de envío**-Los pedidos importados de Walmart incluyen los siguientes valores para los campos de pago y envío:

   - **[!UICONTROL Offline Channel Payment]**: indica que el pago del pedido se procesa sin conexión por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**: permite mostrar el [!DNL Walmart Marketplace] número de pedido.

   - **[!UICONTROL Channel Shipping - Value]**-Indica que los gastos de envío se gestionan mediante [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**: este campo solo se muestra si un pedido se ha importado de [!DNL Walmart Marketplace] se ha cancelado. Los motivos de cancelación incluyen:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Elementos pedidos**: en esta sección se enumeran los elementos de pedido de todos los pedidos de comercio. El [!UICONTROL Qty] proporciona el historial de estado de los artículos de pedido. Por ejemplo, si un pedido se ha facturado, enviado y reembolsado, puede ver las transiciones de estado.

  ![Detalle del pedido historial de estado del artículo pedido [!DNL Walmart Marketplace] pedidos](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Consultar los detalles de la factura y el reembolso del artículo seleccionando la [!UICONTROL Invoice] y [!UICONTROL Credit Memo] opciones del menú de navegación. También puede acceder a la nota de crédito directamente desde [[!UICONTROL Returns]](return-refund-orders.md) en su tienda de canales de ventas.
