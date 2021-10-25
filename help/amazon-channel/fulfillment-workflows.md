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
| 1 | **Se coloca en Amazon un pedido cumplido por el comerciante.** Amazon asigna un estado de `Pending` hasta que se verifique la información de la tarjeta de crédito del cliente. Pedidos en `Pending` el estado se importa automáticamente al canal de ventas de Amazon, pero no se muestra en la variable _[!UICONTROL Orders]_pestaña . |
| 2 | **Amazon verifica el pedido.** Cuando se verifica, Amazon cambia el estado a `Unshipped`. Con este cambio de estado, el pedido se actualiza en el canal de ventas de Amazon y aparece en la variable _[!UICONTROL Orders]_pestaña . |
| 3 | **Se actualizan los detalles del pedido.** El canal de ventas de Amazon actualiza los detalles del pedido con el precio, el correo electrónico del cliente y el nombre del cliente. Durante esta actualización, la solicitud de Amazon crea la [!DNL Commerce] en la página de gestión de pedidos. La variable [!DNL Commerce] el número de pedido se muestra con la información de pedido en la _[!UICONTROL Orders]_pestaña . |
| 4 | **Se crea una nueva cuenta de cliente.** Si está configurado en la configuración del pedido y el cliente no existe en su [!DNL Commerce] base de datos, se crea un cliente nuevo en su [!DNL Commerce] base de datos utilizando la información de cliente correspondiente del pedido de Amazon. Si elige `No Customer Creation (guest)` en la configuración del pedido, el orden sigue a la [!DNL Commerce] proceso de invitado y no crear un cliente en la base de datos. En este punto, si su [!DNL Commerce] El sistema está integrado con un sistema ERP/OMS/WMS, el pedido se recoge por la integración de un nuevo pedido que se está colocando y creando dentro de [!DNL Commerce]. |
| 5 | **Se envía el pedido.** En el [!DNL Commerce] en la página de procesamiento de pedidos, envíe el pedido y añada un número de seguimiento. Cuando todos los elementos estén marcados en un `Shipped` estado:<ul><li>El estado de la variable [!DNL Commerce] cambios de pedidos a `Complete`.</li><li>El estado del pedido del canal de ventas de Amazon cambia a `Shipped`.</li><li>El número de seguimiento se sincroniza con Amazon y el estado del pedido en Amazon cambia a `Shipped`.</li><li>Las notificaciones de envío se envían al cliente a través de Amazon, no desde [!DNL Commerce] (según las políticas de Amazon). |

## Ejemplo: cumplido por Amazon (FBA)

| Paso | Descripción |
|---|---|
| 1 | **En Amazon se coloca un pedido cumplido por Amazon.** |
| 2 | **Se importa el pedido.** El pedido no se importa en el canal de ventas de Amazon hasta que se asigna al pedido el valor `Shipped` por Amazon. Como Amazon tiene el inventario para este producto, evita interferencias con la administración del almacén/inventario. |
| 3 | **Se actualizan los detalles del pedido.** Si está configurado en su [configuración de pedidos](./order-settings.md), el orden de Amazon crea el [!DNL Commerce] solicite y se cree como un pedido con el estado de `Complete`. |
