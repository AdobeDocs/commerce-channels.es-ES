---
title: '"Administrar [!DNL Walmart Marketplace] Pedidos"'
description: '"Ver y administrar [!DNL Walmart Marketplace] pedidos con [!DNL Channel Manager] para Adobe Commerce y Magento Open Source."'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Administrar [!DNL Walmart Marketplace] pedidos

[!DNL Walmart Marketplace] pedidos [!DNL Commerce] las listas de productos se sincronizan automáticamente con [!DNL Channel Manager] after [!DNL Walmart] procesa el pedido. Cuando finalice la sincronización, puede ver la información de pedido seleccionando **[!UICONTROL Orders]** desde la vista de almacén de canales conectada en [!DNL Channel Manager].

![Administrador de canales vista Pedidos para administrar [!DNL Walmart Marketplace] pedidos](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Puede tardar hasta 35 minutos durante un [!DNL Walmart Marketplace] orden de visualización en la variable [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] requiere aproximadamente 30 minutos para procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager]. Una vez que el Administrador de canales recibe el pedido, tardan aproximadamente cinco minutos más en crear y mostrar el pedido en Adobe Commerce o Magento Open Source.

## Revisar pedidos

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir el [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono de lápiz en una fila de entrada de tienda.

1. Para ver la información de pedido, seleccione *[!UICONTROL *Orders]**.

1. Obtenga información sobre el pedido y determine los pasos siguientes comprobando la variable **[Estado](#about-order-status)** para obtener información sobre los pedidos.

## Ver detalle de pedido

Una vez que se recibe un pedido del mercado y se importa a Adobe Commerce o al Magento Open Source, utilice la variable [!DNL Commerce] ID de pedido para ver el pedido en Adobe Commerce.

De **[!UICONTROL Orders]**, seleccione **[!UICONTROL Commerce Order Number]** para abrir el [!DNL Commerce] detalles del pedido.

![Vista de detalles de pedidos de comercio para un [!DNL Walmart Marketplace] pedido](assets/order-detail-with-external-order-id.png)

### Controles de pedidos y descripciones de columnas

Las siguientes tablas describen los controles y las columnas disponibles para Pedidos.

**Controles para[!UICONTROL Orders]**
| **Control**                    | **Descripción**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     | Ordene la vista seleccionando una de las [!UICONTROL Order Status] tarjetas.                                                                                        | | Detalles del mensaje de error | Pase el ratón sobre el [!UICONTROL Error Status] para ver el mensaje de error detallado.                                                                      | | [!UICONTROL View order detail] | Para ver los detalles del pedido, seleccione [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] ordenar opciones para procesar el pedido. |

**Descripciones de columnas**

| Campo | Descripción |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | El número de orden de compra asignado al pedido en la variable [!DNL Walmart Marketplace]. Cuando se importa inicialmente un pedido a [!DNL Channel Manager], solo el [!DNL Walmart] número de pedido. Cuando la variable [!DNL Commerce] se crea el [!DNL Walmart] el número de pedido se almacena en la variable [!UICONTROL External ID] atributo de producto. |
| [!DNL Commerce]  Número de pedido | El número asignado a la variable [!DNL Commerce]  pedido creado a partir de [!DNL Walmart Marketplace] pedido. |
| Elementos | Número de artículos pedidos en [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Coste total de los artículos pedidos. |
| [!UICONTROL Date Created] | La fecha en la que se creó el pedido en la variable [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Fecha en la que debe enviarse el pedido para cumplir [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Deliver By Date] | Fecha en la que se debe entregar el pedido al cliente para que se cumpla [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Last Update At] | Marca de tiempo que indica la última vez que se actualizaron los datos del pedido en [!DNL Channel Manager] |
| [!UICONTROL Status] | Indica el estado del pedido actual en la variable [!DNL Commerce] flujo de trabajo de pedido. El estado se actualiza cuando se agregan productos correctamente a [!DNL Channel Manager] y cuando coincida con productos en la variable [!DNL Walmart Marketplace]. Si falla una operación, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |
| [!UICONTROL Error Description] | Proporciona información más detallada sobre los pedidos con una *Error* estado. |

### Acerca del estado del pedido


[!UICONTROL Order Status] proporciona información sobre el estado actual de [!DNL Walmart Marketplace] pedidos administrados desde Adobe Commerce o Magento Open Source. Las actualizaciones de estado del pedido se producen cuando [!DNL Channel Manager] recibe información de pedido actualizada de [!DNL Walmart Marketplace] o [!DNL Commerce] sistema de pedidos. Los pedidos pueden tener los siguientes estados:

* **[!UICONTROL Open]**-Pedidos recibidos del [!DNL Walmart Marketplace] listo para revisarse y procesarse en Adobe Commerce o Magento Open Source.

   Después de que un cliente solicite un producto de la variable [!DNL Walmart Marketplace], el orden de apertura puede tardar hasta 35 minutos en mostrarse en el espacio de trabajo del pedido del canal conectado. [!DNL Commerce] requiere aproximadamente 30 minutos para procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager]. Una vez que el Administrador de canales recibe el pedido, tardan 5 minutos más en crear y mostrar la variable [!DNL Commerce] pedido.

* **[!UICONTROL Processed]**-Pedidos que se han enviado, cancelado o reembolsado desde el [!DNL Commerce] tienda.

   Para mostrar todos los pedidos enviados, cancelados y reembolsados, seleccione la opción **Procesado** tarjeta de estado.

* **[!UICONTROL Canceled]**-Pedidos que se han cancelado del [!DNL Commerce] tienda.

   Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] la cantidad de stock se actualiza para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]**-Pedidos que han sido reembolsados desde el [!DNL Commerce] tienda.

   Una vez finalizada la devolución, la variable [!DNL Commerce] actualizaciones de la cantidad de stock para reflejar los artículos reembolsados. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace].

* **[!UICONTROL Error]**- Pedidos que tienen errores. Pueden producirse errores cuando falla una operación de actualización de pedidos. Por ejemplo, se producen errores si [!DNL Channel Manager] no puede recibir un nuevo pedido de Walmart. También pueden producirse si [!DNL Channel Manager] no se puede enviar un envío de pedido o una actualización de cancelación a la [!DNL Walmart Marketplace].

* **[!UICONTROL Error description]**-Proporciona información detallada sobre los errores de pedidos que se producen debido a problemas como falta de información o valores no válidos, detalles de envío incorrectos o una cancelación de pedido fallida. La descripción ayuda a determinar si se ha producido un error en la variable [!DNL Commerce] o en la [!DNL Walmart Marketplace].
