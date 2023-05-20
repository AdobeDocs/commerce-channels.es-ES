---
title: Órdenes de devolución y reembolso
description: Instrucciones para la expedición de restituciones totales o parciales por las solicitudes de devolución recibidas de [!DNL Walmart Marketplace] de [!DNL Channel Manager] para Adobe Commerce y Magento Open Source.
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Órdenes de devolución y reembolso

Cuando un comprador solicita una devolución por artículos de pedido comprados a través de [!DNL Walmart Marketplace], Walmart crea una solicitud de devolución. [!DNL Channel Manager] supervisa el canal del mercado para estas solicitudes y sincroniza automáticamente la información de la solicitud de devolución con el Administrador de canales.

En el lado del comercio, la solicitud de retorno inicia el siguiente flujo de trabajo:

1. Channel Manager crea una solicitud de retorno correspondiente con un estado recibido y añade el número de ID de retorno ([!UICONTROL RMA #]) a la [!UICONTROL Returns] panel. En el [!DNL Orders] panel, el detalle de estado del pedido asociado con las actualizaciones de devolución para incluir un [!UICONTROL Return requested] para ver y procesar la devolución.

1. Los comerciantes procesan la devolución asociada con la devolución creando una nota de abono siguiendo el [Flujo de trabajo de Adobe Commerce return](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). Todos los reembolsos se procesan mediante el método sin conexión.

1. [!DNL Channel Manager] envía una actualización de reembolso a Walmart Marketplace para que el estado de devolución se pueda actualizar para reflejar el reembolso completado de Adobe Commerce.

En el Administrador de tienda, puede ver y procesar las devoluciones de Channel Manager abriendo el almacén del canal de ventas y seleccionando **[!UICONTROL Returns]**.

![El administrador de canales devuelve el panel para procesar las devoluciones de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>Solo puede procesar reembolsos para pedidos enviados. Entrada [!DNL Channel Manager], el estado del pedido debe ser [!UICONTROL Shipped]. Entrada [!DNL Walmart Marketplace] Cuenta de vendedor, el pedido debe ser [!UICONTROL Delivered].

## Devuelve controles y descripciones de columnas

En las tablas siguientes se describen los controles y las columnas disponibles para [!DNL Channel Manager] devuelve.

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
<td>Para las entradas de devolución con [!UICONTROL Received] o [!UICONTROL Refunded] estado, puede crear o consultar la nota de abono de la devolución seleccionando el texto enlazado en la columna Detalles de Estado.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para ver los detalles del pedido, seleccione [!DNL Commerce] número de pedido en [!UICONTROL Order] para abrir el pedido de Commerce.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar la configuración del canal, seleccione las credenciales de la conexión Walmart del canal, los atributos asignados o los identificadores de envío, la configuración seleccione el [!DNL Commerce] número de pedido en [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] opciones de pedido para procesar el pedido.</td>
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
<td>El número de autorización de devolución de mercancía asociado con la solicitud de devolución recibida de [!DNL Walmart Marketplace]. Este número lo genera Walmart Marketplace [!UICONTROL Returns] cuando se inicia el proceso de devolución.</td>
</tr>
<tr>
<td>[!DNL Commerce] Nº de pedido</td>
<td>El [!DNL Commerce] Número de pedido asociado con los artículos incluidos en la solicitud de devolución de Walmart Marketplace. Consultar los detalles del pedido seleccionando el número de pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>La fecha en la que se solicitó la devolución [!DNL Walmart Marketplace]
convertido a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>La fecha en la que debe reembolsarse la devolución para cumplir [!DNL Walmart Marketplace] [requisitos](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) se convirtió a la hora local.</td>
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
<td>Indica el estado de retorno actual en [!DNL Commerce] flujo de trabajo de devolución<i>Recibido</i>, <i>Reembolsado</i>, o <i>Error</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Para las entradas de devolución recibidas y reembolsadas, los detalles de estado proporcionan un enlace para acceder a la nota de abono para el procesamiento de devoluciones. Si se produce un error durante la [!DNL Channel Manager] proceso de sincronización entre Adobe Commerce y [!DNL Walmart marketplace], este campo proporciona la descripción del error.</td>
</tr>
</table>

## Estado de devolución

[!UICONTROL Return Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] solicitudes de devolución administradas desde Adobe Commerce o Magento Open Source.

Las actualizaciones de estado de devolución se producen cuando [!DNL Channel Manager] recibe una solicitud de devolución del [!DNL Walmart Marketplace] o cuando la variable [!DNL Commerce] nota de abono se crea para procesar la devolución de los artículos devueltos.

Las devoluciones pueden tener los siguientes estados:

* **[!UICONTROL Received]**-Este es el estado inicial de la solicitud de devolución recibida del [!DNL Walmart Marketplace] tienda. El comerciante puede procesar el reembolso de la devolución seleccionando **[!UICONTROL Create credit memo]** en el [!UICONTROL Status details].

* **[!UICONTROL Refunded]**: indica que se ha creado una nota de abono para emitir un reembolso por los artículos devueltos. Los comerciantes pueden ver la información de los reembolsos seleccionando **[!UICONTROL View credit memo]** en el [!UICONTROL Status details].

* **[!UICONTROL Error]**: permite devolver solicitudes con errores. Pueden producirse errores cuando la solicitud de devolución de Walmart contiene datos incorrectos o que faltan. O bien, si [!DNL Channel Manager] no puede enviar la notificación de actualización de reembolso a Walmart.

## Situaciones de retorno

Los siguientes escenarios describen cómo emitir reembolsos para diferentes tipos de solicitudes de devolución de [!DNL Channel Manager].

* **Retorno total**: si la solicitud de devolución de Walmart Marketplace es para todos los artículos del pedido, actualice la cantidad de nota de abono para reembolsar todos los artículos.

* **Retorno parcial**-Si la solicitud de devolución de Walmart Marketplace es solo para algunos artículos de pedido, actualice la cantidad de nota de abono solo para los artículos que se van a reembolsar.

* **Devolución ya reembolsada a través de Walmart Marketplace**-En algunos casos, se procesa un reembolso el [!DNL Walmart Marketplace] antes de procesar la devolución en el Administrador de canales. Por ejemplo, si una orden de Commerce no es reembolsada dentro de la ventana de procesamiento de devoluciones de 48 horas requerida por Walmart, Walmart reembolsa automáticamente la orden. Cuando esto sucede, Channel Manager sigue sincronizando la solicitud de devolución con Adobe Commerce para que pueda procesar la devolución y emitir el abono. Este flujo de trabajo garantiza que los detalles del pedido en [!DNL Commerce] coincide con la información del pedido en Walmart Marketplace.

>[!NOTE]
>
> Las actualizaciones de reembolso pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Puede comprobar el estado de retorno actual desde el [!DNL Channel Manager] [!UICONTROL Returns] panel.

## Procesar una solicitud de reembolso

1. Abra el [!UICONTROL Returns] tablero de su tienda de canales de ventas.

   * En Admin, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

   * Puede revisar las devoluciones seleccionando la **[!UICONTROL Returns]** pestaña.

      También puede acceder a la información de retorno desde el [!UICONTROL Orders] página. Buscar: [!UICONTROL Shipped] pedidos que tienen una solicitud de devolución. A continuación, seleccione la `Return requested` vínculo en el [!UICONTROL Status Details] para ver y procesar la solicitud.

1. En la tabla Devuelve, busque una devolución con el *[!UICONTROL Received]* estado.

1. En la columna artículos, revise la lista de artículos de pedido y la cantidad que se va a devolver.

1. Procese la devolución emitiendo una nota de abono.

   * Desde el [!UICONTROL Status Details] columna, seleccione **[!UICONTROL Create credit memo]** para abrir la página de detalles de pedidos en [!DNL Commerce].

      Si el pedido no se ha facturado, la página de detalles del pedido muestra un mensaje de error en el que se le solicita que cree uno. Seleccionar **[!UICONTROL Create invoice]**. A continuación, [crear y guardar la factura](https://docs.magento.com/user-guide/sales/invoices.html).

   * En la página Detalles del pedido, seleccione **[!UICONTROL Credit Memo]**.

   * Entrada [!UICONTROL Items to Refund] de la sección [!UICONTROL Credit Memo], actualice el **[!UICONTROL Qty to refund]** y **[!UICONTROL Return to Stock]** información sobre los artículos incluidos en la solicitud de devolución.

      Asegúrese de devolver solo los elementos enumerados en la solicitud de devolución.

   * Para añadir un comentario, escriba el texto en la **[!UICONTROL Credit Memo Comments]**

   * Seleccionar **[!UICONTROL Refund Offline]**.

Después de completar el reembolso, [!DNL Channel Manager] actualiza el estado de retorno en la [!UICONTROL Returns] panel a [!UICONTROL Refunded] y sincroniza la actualización con Walmart para actualizar el estado de retorno en Marketplace.


## Ver información de devolución de una devolución

Puede ver información sobre las solicitudes de devolución y el procesamiento de devoluciones en [!UICONTROL Returns] panel.

1. Abra el panel Devoluciones de su tienda de canales de ventas.

   * En Admin, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono en forma de ojo de una tienda de canales de ventas.

   * Seleccionar **[!UICONTROL Returns]**.

1. Ver pedidos reembolsados seleccionando la **[!UICONTROL Refunded]** tarjeta de estado.

1. Ver detalles de devolución de una devolución seleccionando **[!UICONTROL View credit memo]**.

   ![Nota de abono para reembolsar los artículos devueltos de una [!DNL Walmart Marketplace] pedido](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>Una vez reembolsado un pedido, la [!UICONTROL Orders] el panel no muestra información de retorno. Para ver la información devuelta, utilice el [!DNL Channel Manager] Devuelve el panel. También encontrará información más detallada sobre devoluciones y reembolsos en la página de detalles del pedido.

## Corrección de errores de devolución

Pueden producirse errores cuando se recibe la información de retorno de [!DNL Walmart Marketplace], o cuando [!DNL Channel Manager] sincroniza las actualizaciones de estado de [!DNL Commerce] hasta [!DNL Walmart Marketplace].

Si la operación de sincronización para una actualización de retorno falla, la variable [!DNL Channel Manager] El panel Devuelve o muestra un *[!UICONTROL Error]* estado de la entrada de retorno. Para garantizar que la información de devolución y reembolso se refleje con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su [!DNL Walmart Marketplace] tienda.
