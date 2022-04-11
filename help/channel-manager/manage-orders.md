---
title: Administrar pedidos de Walmart Marketplace
description: Ver y administrar [!DNL Walmart Marketplace] pedidos con [!DNL Channel Manager] para Adobe Commerce y Magento Open Source.
source-git-commit: c6c204fa5f72a68c814f48163cb037f558a41de4
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# Administrar pedidos de Walmart Marketplace

[!DNL Walmart Marketplace] pedidos [!DNL Commerce] las listas de productos se sincronizan automáticamente con [!DNL Channel Manager] después de que Walmart procese el pedido. Cuando finalice la sincronización, puede ver la información de pedido seleccionando **[!UICONTROL Orders]** desde la vista de almacén de canales conectada en [!DNL Channel Manager].

![Administrador de canales Vista Pedidos para administrar pedidos de Walmart Marketplace](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Puede tardar hasta 35 minutos durante un [!DNL Walmart Marketplace] orden de visualización en la variable [!DNL Channel Manager] lista de pedidos. [!DNL Walmart] requiere aproximadamente 30 minutos para procesar los pedidos entrantes y enviarlos a [!DNL Channel Manager].  Una vez que el Administrador de canales recibe el pedido, tardan 5 minutos más en crear y mostrar el pedido en Adobe Commerce o Magento Open Source.

## Revisar pedidos

1. En Administración, seleccione **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** para abrir el [!UICONTROL Channel Manager Marketplace Stores] página.

1. Abra la vista de tienda seleccionando el icono de lápiz en una fila de entrada de tienda.

1. Para ver la información de pedido, seleccione *[!UICONTROL *Orders]**.

## Ver detalle de pedido

Una vez que se recibe un pedido del mercado y se importa a Adobe Commerce o al Magento Open Source, utilice la variable [!DNL Commerce] ID de pedido para ver el pedido en Adobe Commerce.

De **[!UICONTROL Orders]**, seleccione [!UICONTROL Commerce Order Number] para abrir el [!DNL Commerce]  detalles del pedido.

![Vista de detalles de un pedido de Walmart Marketplace](assets/order-detail-with-external-order-id.png)

### Controles de pedidos y descripciones de columnas

Las siguientes tablas describen los controles y las columnas disponibles para Pedidos.

**Controles para[!UICONTROL Orders]**
| **Control**                    | **Descripción**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     | Ordene la vista seleccionando una de las [!UICONTROL Order Status] tarjetas.                                                                                        | | Detalles del mensaje de error | Pase el ratón sobre el [!UICONTROL Error Status] para ver el mensaje de error detallado.                                                                      | | [!UICONTROL View order detail] | Para ver los detalles del pedido, seleccione [!DNL Commerce] número de pedido de la variable [!UICONTROL Order] tabla. A continuación, utilice [!DNL Commerce] ordenar opciones para procesar el pedido. |

**Descripciones de columnas**

| **Campo** | **Descripción** |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | El número de orden de compra asignado al pedido en la variable [!DNL Walmart Marketplace]. Cuando se importa inicialmente un pedido a [!DNL Channel Manager], solo se muestra el número de pedido de Walmart. Cuando la variable [!DNL Commerce] se crea el [!DNL Walmart] el número de pedido se almacena en la variable [!UICONTROL External ID] atributo de producto. |
| [!DNL Commerce]  Número de pedido | El número asignado a la variable [!DNL Commerce]  pedido creado a partir de [!DNL Walmart Marketplace] pedido. |
| Elementos | Número de artículos pedidos en [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Coste total de los artículos pedidos. |
| [!UICONTROL Date Created] | La fecha en la que se creó el pedido en la variable [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Fecha en la que debe enviarse el pedido para cumplir [!DNL Walmart Marketplace] requisitos. |
| [!UICONTROL Order Status] | Indica el estado del pedido actual en la variable [!DNL Commerce] flujo de trabajo de pedido. El estado se actualiza cuando se agregan productos correctamente a [!DNL Channel Manager] y cuando coincida con productos en la variable [!DNL Walmart Marketplace]. Si falla una operación, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |

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

* **[!UICONTROL Error]**- Pedidos que no se han importado al repositorio de pedidos debido a la falta de información u otros problemas.

   Para ver los detalles del mensaje de error, pase el ratón sobre el *[!UICONTROL Error]* indicador de estado. Una vez resuelto el error, el pedido se actualiza automáticamente para mostrar la información y el estado actuales.

