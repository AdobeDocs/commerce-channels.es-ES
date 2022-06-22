---
title: '''Ver y rastrear pedidos de [!DNL Channel Manager]'''
description: '''Ver y administrar [!DNL Walmart Marketplace] pedidos con [!DNL Channel Manager] para Adobe Commerce y Magento Open Source.'''
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Ver y rastrear pedidos de [!DNL Channel Manager]

[!DNL Walmart Marketplace] datos de pedido para [!DNL Commerce] products se sincroniza automáticamente con [!DNL Channel Manager] after [!DNL Walmart] procesa el pedido.

En el [!DNL Commerce] además, una sincronización correcta déclencheur las siguientes acciones:

- [!DNL Channel Manager] envía un acuse de recibo de pedido a Walmart.

- A [!DNL Commerce] el pedido se crea a partir del pedido de Walmart.

- La información de pedido actualizada se muestra en la [!DNL Channel Manager] Panel de pedidos.

En el administrador de tienda, puede ver los datos de pedidos desde [!DNL Channel Manager] abriendo el almacén de canales de ventas y seleccionando **[!UICONTROL Orders]**.

![Administrador de canales vista Pedidos para administrar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Puede tardar hasta 35 minutos durante un [!DNL Walmart Marketplace] orden de visualización en la variable [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] requiere aproximadamente 30 minutos para procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager]. Una vez que el Administrador de canales recibe el pedido, tardan aproximadamente cinco minutos más en crear y mostrar el pedido en Adobe Commerce o Magento Open Source.

## Controles de pedidos y descripciones de columnas

Las siguientes tablas describen los controles y las columnas disponibles para Pedidos.

**Controles para[!UICONTROL Orders]**
| **Control**                    | **Descripción**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     | Ordene la vista seleccionando una de las [!UICONTROL Order Status] tarjetas.                                                                                                                                                                                                           | | Descripción del error | Proporciona información más detallada sobre los pedidos con un estado de error.                                                                                                                                                                                                            | | [!UICONTROL View order detail] | Para ver los detalles del pedido, seleccione [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] ordenar opciones para procesar el pedido.                                                                                                                    | | [!UICONTROL Channel Settings]  | Para modificar la configuración del canal, seleccione credenciales de conexión Walmart de canal, atributos asignados o identificadores de envío, la configuración seleccione [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] ordenar opciones para procesar el pedido. |


**Descripciones de columnas**

| Campo | Descripción |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | El número de orden de compra asignado al pedido en la variable [!DNL Walmart Marketplace]. Cuando se importa inicialmente un pedido a [!DNL Channel Manager], solo el [!DNL Walmart] número de pedido. Cuando la variable [!DNL Commerce] se crea el [!DNL Walmart] el número de pedido se almacena en la variable [!UICONTROL External ID] atributo de producto. |
| [!DNL Commerce] Número de pedido | El número asignado a la variable [!DNL Commerce] pedido creado a partir de [!DNL Walmart Marketplace] pedido. |
| Elementos | Número de artículos pedidos en [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Coste total de los artículos pedidos. |
| [!UICONTROL Date Ordered] | La fecha en la que se presentó la solicitud [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Fecha en la que debe enviarse el pedido para cumplir [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Deliver By Date] | Fecha en la que se debe entregar el pedido al cliente para que se cumpla [!DNL Walmart Marketplace] requisitos en formato UTC. |
| [!UICONTROL Ship Method] | La variable [[!DNL Walmart Marketplace] Método de envío](https://sellerhelp.walmart.com/s/guide?article=000007893) seleccionado para el orden. |
| [!UICONTROL Last Update At] | Marca de tiempo que indica la última vez que se actualizaron los datos del pedido en [!DNL Channel Manager] en formato UTC. |
| [!UICONTROL Status] | Indica el estado del pedido actual en la variable [!DNL Commerce] flujo de trabajo de pedido. El estado inicial de un pedido importado de [!DNL Walmart Marketplace] es _Apertura_. Se producen actualizaciones de estado adicionales al [!DNL Commerce] los pedidos se procesan y [!DNL Channel Manager] sincroniza correctamente las actualizaciones de envío, envío parcial y cancelación a la variable [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | Proporciona información más detallada sobre los pedidos con una _[!UICONTROL Error]_estado. |

## Estado del pedido


[!UICONTROL Order Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] pedidos administrados desde Adobe Commerce o Magento Open Source. Las actualizaciones de estado del pedido se producen cuando [!DNL Channel Manager] recibe información de pedido actualizada de [!DNL Walmart Marketplace] o [!DNL Commerce] sistema de pedidos. Los pedidos pueden tener los siguientes estados:

- **[!UICONTROL Shipped]**-Pedidos que se han enviado desde el [!DNL Commerce] tienda. Cuando se envía el pedido, [!DNL Channel Manager] envía una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío en Walmart y proporcionar el número de seguimiento del pedido para el envío.

- **[!UICONTROL Partially Shipped]**: pedidos que tienen algunos artículos marcados como enviados y otros esperando ser enviados. Cuando se envían artículos en el pedido, [!DNL Channel Manager] envía una actualización a [!DNL Walmart Marketplace] para actualizar el estado de envío a _[!DNL Partially Shipped]_en Walmart y proporcione el número de seguimiento del pedido para el envío.

- **[!UICONTROL Canceled]**-Pedidos que se han cancelado del [!DNL Commerce] tienda.

   Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] la cantidad de stock se actualiza para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace].

- **[!UICONTROL Error]**- Pedidos que tienen errores. Pueden producirse errores cuando falla una operación de actualización de pedidos. Por ejemplo, se producen errores si [!DNL Channel Manager] no puede recibir un nuevo pedido de Walmart. También pueden producirse si [!DNL Channel Manager] no se puede enviar un envío de pedido o una actualización de cancelación a la [!DNL Walmart Marketplace]. Si se produce un error en una operación, la página Pedidos muestra una _Error_ para el pedido. Para obtener más información, consulte [Corrección de errores de orden](process-orders.md#fix-Shipping-and-cancelation- errors).

- **[!UICONTROL Error description]**-Proporciona información detallada sobre los errores de pedidos que se producen debido a problemas como falta de información o valores no válidos, detalles de envío incorrectos o una cancelación de pedido fallida. La descripción ayuda a determinar si se ha producido un error en la variable [!DNL Commerce] o en la [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si los artículos del pedido se envían en varios envíos, el estado del pedido en [!DNL Channel Manager] refleja el último estado de pedido disponible. Por ejemplo, si el primer artículo se envía y no se devuelven errores cuando las actualizaciones del pedido se sincronizan con [!DNL Channel Manager] y [!DNL Walmart Marketplace], el [!DNL Channel Manager] el estado del pedido es _[!UICONTROL Partially Shipped]_. Si se envía un segundo artículo y [!DNL Channel Manager] devuelve un error, el estado del pedido se actualiza a_[!UICONTROL Error]_.

## Revisar pedidos

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir el [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono de ojo en una fila de entrada de tienda.

1. Para ver la información de pedido, seleccione *[!UICONTROL *Orders]**.

1. Obtenga información sobre el pedido y determine los pasos siguientes comprobando la variable **[Estado](#about-order-status)** para abrir el Navegador.

## Ver detalle de pedido

Una vez que se recibe un pedido del mercado y se importa a Adobe Commerce o al Magento Open Source, utilice la variable [!DNL Commerce] ID de pedido para ver el pedido en Adobe Commerce.

De **[!UICONTROL Orders]**, seleccione **[!UICONTROL Commerce Order Number]** para abrir el [!DNL Commerce] detalles del pedido.

![Vista de detalles de pedidos de comercio para un [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

En la tienda de comercio, los pedidos importados de [!DNL Walmart Marketplace] incluir la siguiente información adicional en los datos de pedido:

- **Información de Pago y Método de Envío**-Los pedidos importados de Walmart incluyen los siguientes valores para los campos de pago y envío:

   - **[!UICONTROL Offline Channel Payment]**: indica que el pago del pedido se procesa sin conexión por [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**: muestra la variable [!DNL Walmart Marketplace] número de pedido.

   - **[!UICONTROL Channel Shipping - Value]**-Indica que los gastos de envío se gestionan mediante [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Este campo solo se muestra si se ha importado un pedido de [!DNL Walmart Marketplace] se cancela. Las razones de cancelación incluyen:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

