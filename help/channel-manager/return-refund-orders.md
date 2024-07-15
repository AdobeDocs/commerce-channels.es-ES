---
title: Órdenes de devolución y reembolso
description: Instrucciones para emitir reembolsos completos o parciales para las solicitudes de devolución recibidas de  [!DNL Walmart Marketplace] de [!DNL Channel Manager] para Adobe Commerce y Magento Open Source.
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Órdenes de devolución y reembolso

Cuando un comprador solicita una devolución de artículos de pedido comprados a través de [!DNL Walmart Marketplace], Walmart crea una solicitud de devolución. [!DNL Channel Manager] supervisa el canal del mercado en busca de estas solicitudes y sincroniza automáticamente la información de la solicitud de retorno con el Administrador de canales.

En el lado de Commerce, la solicitud de retorno inicia el siguiente flujo de trabajo:

1. Channel Manager crea una solicitud de retorno correspondiente con un estado recibido y agrega el número de identificador de retorno ([!UICONTROL RMA #]) al panel [!UICONTROL Returns]. En el panel [!DNL Orders], el detalle de estado del pedido asociado con la devolución se actualiza para incluir un vínculo [!UICONTROL Return requested] que permita ver y procesar la devolución.

1. Los comerciantes procesan el reembolso asociado con la devolución creando un abono siguiendo el [flujo de trabajo de reembolso de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). Todos los reembolsos se procesan mediante el método sin conexión.

1. [!DNL Channel Manager] envía una actualización de reembolso al mercado de Walmart para que el estado de devolución se pueda actualizar a fin de reflejar el reembolso completado de Adobe Commerce.

En el Administrador de tienda, puede ver y procesar las devoluciones de Channel Manager. Para ello, abra el almacén del canal de ventas y seleccione **[!UICONTROL Returns]**.

![El Administrador de canales devuelve el panel para procesar los reembolsos de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Solo puede procesar reembolsos para pedidos enviados. En [!DNL Channel Manager], el estado del pedido debe ser [!UICONTROL Shipped]. En la cuenta de vendedor [!DNL Walmart Marketplace], el pedido debe ser [!UICONTROL Delivered].

## Devuelve controles y descripciones de columnas

Las tablas siguientes describen los controles y las columnas disponibles para los valores devueltos de [!DNL Channel Manager].

**Controles para[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Control</strong></td>
<td><strong>Descripción</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filtre la vista seleccionando una de las [!UICONTROL Return Status] tarjetas.</td>
</tr>
<tr>
<td>Detalles del estado</td>
<td>Para las entradas de devolución con el estado [!UICONTROL Received] o [!UICONTROL Refunded], puede crear o ver la nota de abono de la devolución seleccionando el texto vinculado en la columna Detalles de estado.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para ver los detalles del pedido, seleccione el número de pedido [!DNL Commerce] en la tabla [!UICONTROL Order] para abrir el pedido de Commerce.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar la configuración del canal, seleccione las credenciales de la conexión Walmart del canal, los atributos asignados o los identificadores de envío, la configuración selecciona el número de pedido [!DNL Commerce] en la tabla [!UICONTROL Order]. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
</tr>
</table>

**Descripciones de columna**

<table>
<tr>
<td><strong>Campo</strong></td>
<td><strong>Descripción</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>Número de autorización de devolución de mercancía asociado con la solicitud de devolución recibida de [!DNL Walmart Marketplace]. Walmart Marketplace [!UICONTROL Returns] genera este número cuando se inicia el proceso de devolución.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº de pedido</td>
<td>El número de pedido [!DNL Commerce] asociado con los artículos incluidos en la solicitud de devolución de Walmart Marketplace. Consultar los detalles del pedido seleccionando el número de pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>Fecha en la que se solicitó la devolución el [!DNL Walmart Marketplace]
convertido a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>Fecha en la que se debe reembolsar la devolución para cumplir [!DNL Walmart Marketplace] [requisitos](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) convertidos a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Indica el SKU y la cantidad de cada artículo enumerado en la devolución.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>El valor total a reembolsar por los artículos devueltos.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica el estado de retorno actual en el flujo de trabajo de retorno [!DNL Commerce]-<i>Recibido</i>, <i>Reembolsado</i> o <i>Error</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Para las entradas de devolución recibidas y reembolsadas, los detalles de estado proporcionan un enlace para acceder a la nota de abono para el procesamiento de devoluciones. Si se produce un error durante el proceso de sincronización de [!DNL Channel Manager] entre Adobe Commerce y [!DNL Walmart marketplace], este campo proporciona la descripción del error.</td>
</tr>
</table>

## Estado de devolución

[!UICONTROL Return Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] solicitudes de devolución administradas desde Adobe Commerce o Magento Open Source.

Las actualizaciones de estado de devolución se producen cuando [!DNL Channel Manager] recibe una solicitud de devolución de [!DNL Walmart Marketplace] o cuando se crea el abono de [!DNL Commerce] para procesar el reembolso de los elementos devueltos.

Las devoluciones pueden tener los siguientes estados:

* **[!UICONTROL Received]**: este es el estado inicial de la solicitud de devolución recibida desde el almacén [!DNL Walmart Marketplace]. El comerciante puede procesar el reembolso de la devolución seleccionando **[!UICONTROL Create credit memo]** en [!UICONTROL Status details].

* **[!UICONTROL Refunded]**: indica que se ha creado un abono para emitir un reembolso por los artículos devueltos. Los comerciantes pueden ver la información de los reembolsos seleccionando **[!UICONTROL View credit memo]** en [!UICONTROL Status details].

* **[!UICONTROL Error]**: devuelve solicitudes con errores. Pueden producirse errores cuando la solicitud de devolución de Walmart contiene datos incorrectos o que faltan. O bien, si [!DNL Channel Manager] no puede enviar la notificación de actualización de reembolso a Walmart.

## Situaciones de retorno

Los siguientes escenarios describen cómo emitir reembolsos para diferentes tipos de solicitudes de devolución de [!DNL Channel Manager].

* **Devolución completa**: si la solicitud de devolución de Walmart Marketplace es para todos los artículos del pedido, actualice la cantidad de nota de abono para reembolsar todos los artículos.

* **Devolución parcial**: si la solicitud de devolución de Walmart Marketplace es solo para algunos artículos de pedido, actualice la cantidad de nota de abono únicamente para los artículos que se van a reembolsar.

* **Devolución ya reembolsada a través de Walmart Marketplace**-En algunos casos, se procesa un reembolso el [!DNL Walmart Marketplace] antes de procesar la devolución en Channel Manager. Por ejemplo, si un pedido de Commerce no es reembolsado dentro de la ventana de procesamiento de devoluciones de 48 horas requerida por Walmart, Walmart reembolsa automáticamente el pedido. Cuando esto sucede, Channel Manager sigue sincronizando la solicitud de devolución con Adobe Commerce para que pueda procesar la devolución y emitir el abono. Este flujo de trabajo garantiza que el detalle del pedido de [!DNL Commerce] coincida con la información del pedido de Walmart Marketplace.

>[!NOTE]
>
> Las actualizaciones de reembolso pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Puede comprobar el estado de retorno actual desde el panel [!DNL Channel Manager] [!UICONTROL Returns].

## Procesar una solicitud de reembolso

1. Abra el tablero [!UICONTROL Returns] de su tienda de canales de ventas.

   * En el Administrador, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

   * Puede revisar los resultados seleccionando la ficha **[!UICONTROL Returns]**.

     También puede acceder a la información devuelta desde la página [!UICONTROL Orders]. Busque [!UICONTROL Shipped] pedidos que tengan una solicitud de devolución. A continuación, seleccione el vínculo `Return requested` en la columna [!UICONTROL Status Details] para ver y procesar la solicitud.

1. En la tabla Devoluciones, busque una devolución con el estado *[!UICONTROL Received]*.

1. En la columna artículos, revise la lista de artículos de pedido y la cantidad que se va a devolver.

1. Procese la devolución emitiendo una nota de abono.

   * En la columna [!UICONTROL Status Details], seleccione **[!UICONTROL Create credit memo]** para abrir la página de detalles Pedido en [!DNL Commerce].

     Si el pedido no se ha facturado, la página de detalles del pedido muestra un mensaje de error en el que se le solicita que cree uno. Seleccione **[!UICONTROL Create invoice]**. A continuación, [cree y guarde la factura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * En la página Detalles del pedido, seleccione **[!UICONTROL Credit Memo]**.

   * En la sección [!UICONTROL Items to Refund] de [!UICONTROL Credit Memo], actualice la información de **[!UICONTROL Qty to refund]** y **[!UICONTROL Return to Stock]** para los elementos incluidos en la solicitud de devolución.

     Asegúrese de devolver solo los elementos enumerados en la solicitud de devolución.

   * Para agregar un comentario, escriba el texto en **[!UICONTROL Credit Memo Comments]**

   * Seleccione **[!UICONTROL Refund Offline]**.

Después de completar el reembolso, [!DNL Channel Manager] actualiza el estado de devolución en el panel [!UICONTROL Returns] a [!UICONTROL Refunded] y sincroniza la actualización a Walmart para actualizar el estado de devolución en Marketplace.


## Ver información de devolución de una devolución

Puede ver información sobre las solicitudes de devolución y el procesamiento de devoluciones en el panel [!UICONTROL Returns].

1. Abra el panel Devoluciones de su tienda de canales de ventas.

   * En el Administrador, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

   * Seleccione **[!UICONTROL Returns]**.

1. Ver pedidos reembolsados seleccionando la tarjeta de estado **[!UICONTROL Refunded]**.

1. Ver detalles de devolución de una devolución seleccionando **[!UICONTROL View credit memo]**.

   ![Nota de crédito para reembolsar artículos devueltos por un pedido de [!DNL Walmart Marketplace]](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Después de reembolsar un pedido, el panel [!UICONTROL Orders] no muestra la información de devolución. Para ver la información devuelta, use el panel [!DNL Channel Manager] devoluciones. También encontrará información más detallada sobre devoluciones y reembolsos en la página de detalles del pedido.

## Corrección de errores de devolución

Pueden producirse errores cuando se recibe la información de retorno de [!DNL Walmart Marketplace], o cuando [!DNL Channel Manager] sincroniza las actualizaciones de estado de [!DNL Commerce] a [!DNL Walmart Marketplace].

Si falla la operación de sincronización para una actualización de retorno, el panel [!DNL Channel Manager] Devuelve muestra un estado *[!UICONTROL Error]* para la entrada de retorno. Para asegurarse de que la información de devolución y reembolso se refleje con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su tienda [!DNL Walmart Marketplace].
