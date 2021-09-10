---
title: Flujos de trabajo de cumplimiento de Amazon
description: El cumplimiento de un pedido de una lista de Amazon sigue una secuencia específica desde el envío del pedido hasta el envío.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Flujos de trabajo de cumplimiento de Amazon

## Ejemplo: cumplido por el comerciante

| Paso | Descripción |
|----|----|
| 1 | **Se coloca en Amazon un pedido cumplido por el comerciante.** Amazon asigna un estado de  `Pending` hasta que se verifica la información de la tarjeta de crédito del cliente. Los pedidos en estado `Pending` se importan automáticamente al canal de ventas de Amazon, pero no se muestran en la pestaña _[!UICONTROL Orders]_. |
| 2 | **Amazon verifica el pedido.** Cuando se verifica, Amazon cambia el estado a  `Unshipped`. Con este cambio de estado, el pedido se actualiza en el canal de ventas de Amazon y aparece en la pestaña _[!UICONTROL Orders]_. |
| 1 | **Se actualizan los detalles del pedido.** El canal de ventas de Amazon actualiza los detalles del pedido con el precio, el correo electrónico del cliente y el nombre del cliente. Durante esta actualización, el pedido de Amazon crea el orden [!DNL Commerce] correspondiente en la página de gestión de pedidos. El número de pedido [!DNL Commerce] se muestra con la información de pedido en la pestaña _[!UICONTROL Orders]_. |
| 4 | **Se crea una nueva cuenta de cliente.** Si está configurado en la configuración de pedidos y el cliente no existe en la  [!DNL Commerce] base de datos, se crea un nuevo cliente en la  [!DNL Commerce] base de datos con la información de cliente correspondiente del pedido de Amazon. Si elige `No Customer Creation (guest)` en la configuración del pedido, el pedido sigue el proceso de invitado [!DNL Commerce] y no crea un cliente en la base de datos. En este punto, si su sistema [!DNL Commerce] está integrado con un ERP/OMS/WMS, el pedido se recoge según la integración de un nuevo pedido que se está colocando y creando dentro de [!DNL Commerce]. |
| 5 | **Se envía el pedido.** Desde la página de procesamiento de  [!DNL Commerce] pedidos, envíe el pedido y agregue un número de seguimiento. Cuando todos los elementos están marcados en un estado `Shipped`:<ul><li>El estado del pedido [!DNL Commerce] cambia a `Complete`.</li><li>El estado del pedido del canal de ventas de Amazon cambia a `Shipped`.</li><li>El número de seguimiento se sincroniza con Amazon y el estado del pedido en Amazon cambia a `Shipped`.</li><li>Las notificaciones de envío se envían al cliente a través de Amazon, no desde [!DNL Commerce] (según las políticas de Amazon). |

## Ejemplo: cumplido por Amazon (FBA)

| Paso | Descripción |
|---|---|
| 1 | **En Amazon se coloca un pedido cumplido por Amazon.** |
| 2 | **Se importa el pedido.** El pedido no se importa en el canal de ventas de Amazon hasta que Amazon asigna el  `Shipped` estado al pedido. Como Amazon tiene el inventario para este producto, evita interferencias con la administración del almacén/inventario. |
| 1 | **Se actualizan los detalles del pedido.** Si se configura en la configuración de  [pedido](./order-settings.md), el pedido de Amazon crea el  [!DNL Commerce] pedido correspondiente y se crea como un pedido con el estado  `Complete`. |
