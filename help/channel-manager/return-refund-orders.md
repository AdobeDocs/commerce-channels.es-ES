---
title: Devolución y Devolución de Pedidos
description: Instrucciones para la expedición de restituciones totales o parciales a las solicitudes de devolución recibidas de [!DNL Walmart Marketplace] from [!DNL Channel Manager] para Adobe Commerce y Magento Open Source.
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Devolución y Devolución de Pedidos

Cuando un comprador solicita una devolución para los artículos de pedido comprados a través de [!DNL Walmart Marketplace], Walmart crea una solicitud de devolución. [!DNL Channel Manager] supervisa el canal de mercado para estas solicitudes y sincroniza automáticamente la información de solicitud de devolución con el Administrador de canales.

En el lado comercial, la solicitud de retorno inicia el siguiente flujo de trabajo:

1. El Administrador de canales crea una solicitud de devolución correspondiente con un estado recibido y agrega el número de ID devuelto ([!UICONTROL RMA #]) a la variable [!UICONTROL Returns] tablero. En el [!DNL Orders] tablero, el detalle de estado del pedido asociado con las actualizaciones de devolución para incluir un [!UICONTROL Return requested] para ver y procesar el retorno.

1. Los comerciantes procesan el reembolso asociado con la devolución mediante la creación de una nota de crédito después de [Flujo de trabajo de reembolso de Adobe Commerce](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). Todos los reembolsos se procesan mediante el método sin conexión.

1. [!DNL Channel Manager] envía una actualización de reembolso al mercado de Walmart para que el estado de devolución se pueda actualizar para reflejar el reembolso completado de Adobe Commerce.

En el administrador de tienda, puede ver y procesar los retornos desde el Administrador de canales abriendo el almacén de canales de ventas y seleccionando **[!UICONTROL Returns]**.

![Administrador de canales Devuelve el panel para procesar los reembolsos de las solicitudes de devolución recibidas de [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>Solo puede procesar reembolsos para pedidos enviados. En [!DNL Channel Manager], el estado del pedido debe ser [!UICONTROL Shipped]. En [!DNL Walmart Marketplace] Cuenta de vendedor, el pedido debe ser [!UICONTROL Delivered].

## Devuelve controles y descripciones de columnas

Las tablas siguientes describen los controles y las columnas disponibles para [!DNL Channel Manager] devuelve.

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
<td>Detalles de estado</td>
<td>Para entradas de devolución con la variable [!UICONTROL Received] o [!UICONTROL Refunded] , puede crear o ver la nota de crédito para el reembolso seleccionando el texto vinculado en la columna Detalles de estado .</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Para ver los detalles del pedido, seleccione la opción [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] para abrir el orden de comercio.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Para modificar la configuración del canal, seleccione credenciales de conexión Walmart de canal, atributos asignados o identificadores de envío, la configuración seleccione [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] ordenar opciones para procesar el pedido.</td>
</tr>
</table>

**Descripciones de columnas**

<table>
<tr>
<td><strong>Campo</strong></td>
<td><strong>Descripción</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>El número de autorización de devolución de mercancías asociado con la solicitud de devolución recibida de [!DNL Walmart Marketplace]. Este número lo genera Walmart Marketplace [!UICONTROL Returns] cuando se inicia el proceso de retorno.</td>
</tr>
<tr>
<td>[!DNL Commerce] N.º de pedido</td>
<td>La variable [!DNL Commerce] número de pedido asociado con los artículos incluidos en la solicitud de devolución de Walmart Marketplace. Para ver los detalles del pedido, seleccione el número de pedido.</td>
</tr>
<tr>
<td>Solicitado</td>
<td>La fecha en la que se solicitó la devolución en el [!DNL Walmart Marketplace]
se convierte a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>La fecha en la que debe reembolsarse la devolución para satisfacer [!DNL Walmart Marketplace] [requisitos](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) se ha convertido a hora local.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Muestra el SKU y la cantidad de cada elemento enumerado en el resultado.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>El valor total que se va a reembolsar para los artículos devueltos.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indica el estado de retorno actual en la variable [!DNL Commerce] return workflow-<i>Recibido</i>, <i>Reembolsado</i>o <i>Error</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>En el caso de las entradas de devolución recibidas y reembolsadas, los detalles del estado proporcionan un vínculo para acceder a la nota de crédito para el procesamiento de reembolsos. Si se produce un error durante la [!DNL Channel Manager] proceso de sincronización entre Adobe Commerce y [!DNL Walmart marketplace], este campo proporciona la descripción del error.</td>
</tr>
</table>

## Estado de devolución

[!UICONTROL Return Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] devuelve solicitudes administradas desde Adobe Commerce o Magento Open Source.

Las actualizaciones de estado de retorno se producen cuando [!DNL Channel Manager] recibe una solicitud de devolución de la variable [!DNL Walmart Marketplace] o cuando la variable [!DNL Commerce] la nota de crédito se crea para procesar el reembolso de los artículos devueltos.

Las devoluciones pueden tener los siguientes estados:

* **[!UICONTROL Received]**-Este es el estado inicial de la solicitud de devolución recibida del [!DNL Walmart Marketplace] tienda. El comerciante puede procesar el reembolso de la devolución seleccionando **[!UICONTROL Create credit memo]** en el [!UICONTROL Status details].

* **[!UICONTROL Refunded]**: indica que se ha creado una nota de abono para emitir un reembolso por los artículos devueltos. Los comerciantes pueden ver la información de reembolsos seleccionando **[!UICONTROL View credit memo]** en el [!UICONTROL Status details].

* **[!UICONTROL Error]**: devuelve solicitudes que tienen errores. Pueden producirse errores cuando en la solicitud de devolución de Walmart faltan datos o éstos son incorrectos. O, si [!DNL Channel Manager] no puede enviar la notificación de actualización de reembolsos a Walmart.

## Situaciones de retorno

Los siguientes escenarios describen cómo emitir reembolsos para diferentes tipos de solicitudes de devolución de [!DNL Channel Manager].

* **Retorno completo**: si la solicitud de devolución de Walmart es para todos los artículos del pedido, actualice la cantidad de nota de crédito para reembolsar todos los artículos.

* **Retorno parcial**-Si la solicitud de devolución de Walmart es solo para algunos artículos de pedido, actualice la cantidad de abono sólo para los artículos que se van a reembolsar.

* **Retorno ya reembolsado a través de Walmart Marketplace**-En algunos casos, se procesa un reembolso en [!DNL Walmart Marketplace] antes de procesar el retorno en el Administrador de canales. Por ejemplo, si un pedido de comercio no es reembolsado dentro del período de procesamiento de reembolsos de 48 horas requerido por Walmart, Walmart lo devuelve automáticamente. Cuando esto sucede, el Administrador de canales sigue sincronizando la solicitud de devolución con Adobe Commerce para que pueda procesar la devolución y emitir la nota de crédito. Este flujo de trabajo garantiza que los detalles de la solicitud [!DNL Commerce] coincide con la información de pedidos en Walmart Marketplace.

>[!NOTE]
>
> Las actualizaciones de reembolsos pueden tardar hasta cinco minutos en sincronizarse con [!DNL Walmart Marketplace]. Puede comprobar el estado de devolución actual desde la [!DNL Channel Manager] [!UICONTROL Returns] tablero.

## Procesar una solicitud de reembolso

1. Abra el [!UICONTROL Returns] tablero para el almacén de canales de ventas.

   * En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de ventas.

   * Para revisar los retornos, seleccione la opción **[!UICONTROL Returns]** pestaña .

      También puede acceder a la información de devolución desde la [!UICONTROL Orders] página. Buscar [!UICONTROL Shipped] pedidos que tienen una solicitud de devolución. A continuación, seleccione la `Return requested` en el [!UICONTROL Status Details] para ver y procesar la solicitud.

1. En la tabla Devuelve, busque un retorno con la variable *[!UICONTROL Received]* estado.

1. En la columna artículos, revise la lista de artículos de pedido y la cantidad a devolver.

1. Procese el reembolso emitiendo una nota de abono.

   * En el [!UICONTROL Status Details] , seleccione **[!UICONTROL Create credit memo]** para abrir la página de detalles del pedido en [!DNL Commerce].

      Si el pedido no se ha facturado, la página de detalles del pedido muestra un mensaje de error en el que se le solicita que lo cree. Select **[!UICONTROL Create invoice]**. A continuación, [crear y guardar la factura](https://docs.magento.com/user-guide/sales/invoices.html).

   * En la página de detalles del pedido, seleccione **[!UICONTROL Credit Memo]**.

   * En [!UICONTROL Items to Refund] de la sección [!UICONTROL Credit Memo], actualice el **[!UICONTROL Qty to refund]** y **[!UICONTROL Return to Stock]** información para los elementos incluidos en la solicitud de devolución.

      Asegúrese de que devuelve solo los elementos enumerados en la solicitud de devolución.

   * Para agregar un comentario, escriba el texto en la **[!UICONTROL Credit Memo Comments]**

   * Select **[!UICONTROL Refund Offline]**.

Una vez finalizada la restitución, [!DNL Channel Manager] actualiza el estado de retorno en la variable [!UICONTROL Returns] tablero a [!UICONTROL Refunded] y sincroniza la actualización con Walmart para actualizar el estado de devolución en marketplace.


## Ver información de devolución

Puede ver información sobre las solicitudes de devolución y el procesamiento de reembolsos desde la [!UICONTROL Returns] tablero.

1. Abra el panel Devuelve para el almacén de canales de ventas.

   * En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Abra la vista de tienda seleccionando el icono de ojo para un almacén de canales de ventas.

   * Select **[!UICONTROL Returns]**.

1. Para ver los pedidos reembolsados, seleccione la opción **[!UICONTROL Refunded]** tarjeta de estado.

1. Ver detalles de devolución seleccionando **[!UICONTROL View credit memo]**.

   ![Nota de crédito para reembolsar los artículos devueltos por un [!DNL Walmart Marketplace] pedido](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>Una vez que se ha reembolsado una orden, la variable [!UICONTROL Orders] el tablero no muestra información de retorno. Para ver la información de devolución, utilice la variable [!DNL Channel Manager] Devuelve el tablero. La información más detallada sobre devoluciones y reembolsos también está disponible en la página de detalles del pedido .

## Corrección de errores devueltos

Pueden producirse errores cuando se recibe la información de retorno de [!DNL Walmart Marketplace]o cuando [!DNL Channel Manager] sincroniza las actualizaciones de estado de [!DNL Commerce] a [!DNL Walmart Marketplace].

Si falla la operación de sincronización para una actualización de retorno, la variable [!DNL Channel Manager] El panel Devuelve muestra un *[!UICONTROL Error]* para la entrada de devolución. Para garantizar que la información de devolución y reembolso se refleje con precisión en la cuenta de Walmart Marketplace, actualice manualmente el pedido en su [!DNL Walmart Marketplace] tienda.
