---
title: Flujos de trabajo de Amazon Fulfillment
description: El cumplimiento de un pedido de un anuncio de Amazon sigue una secuencia específica desde la entrega del pedido hasta el envío.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Flujos de trabajo de Amazon Fulfillment

## Ejemplo: completado por el comerciante

| Etapa | Descripción |
|----|----|
| 1 | **Se realiza un pedido completado por el comerciante en Amazon.** Amazon asigna un estado de `Pending` hasta que se verifique la información de la tarjeta de crédito del cliente. Pedidos en `Pending` estado se importa automáticamente en el canal de ventas de Amazon, pero no se muestra en la _[!UICONTROL Orders]_pestaña. |
| 2 | **Amazon verifica el pedido.** Cuando se verifica, Amazon cambia el estado a `Unshipped`. Con este cambio de estado, el pedido se actualiza en el canal de ventas de Amazon y aparece en la _[!UICONTROL Orders]_pestaña. |
| 3 | **Se actualizan los detalles del pedido.** Amazon Sales Channel actualiza los detalles del pedido con el precio, el correo electrónico del cliente y el nombre del cliente. Durante esta actualización, el pedido de Amazon crea el correspondiente [!DNL Commerce] orden en la página de gestión de pedidos. El [!DNL Commerce] el número de pedido se muestra con la información del pedido en la _[!UICONTROL Orders]_pestaña. |
| 4 | **Se crea una nueva cuenta de cliente.** Si está configurado en la configuración del pedido y el cliente no existe en su [!DNL Commerce] base de datos, se crea un nuevo cliente en su [!DNL Commerce] base de datos utilizando la información de cliente correspondiente del pedido de Amazon. Si elige `No Customer Creation (guest)` en la configuración de su pedido, el orden sigue el [!DNL Commerce] proceso invitado y no crear un cliente en la base de datos. En este punto, si su [!DNL Commerce] El sistema está integrado con un ERP/OMS/WMS, el pedido se recoge según la integración de un nuevo pedido que se está realizando y creando en su interior [!DNL Commerce]. |
| 5 | **El pedido se envía.** Desde el [!DNL Commerce] En la página de procesamiento de pedidos, se envía el pedido y se añade un número de seguimiento. Cuando todos los elementos se marcan en una `Shipped` estado:<ul><li>El estado del [!DNL Commerce] cambios de pedido en `Complete`.</li><li>El estado del pedido del canal de ventas de Amazon cambia a `Shipped`.</li><li>El número de seguimiento se sincroniza con Amazon y el estado del pedido en Amazon cambia a `Shipped`.</li><li>Las notificaciones de envío se envían al cliente a través de Amazon, no desde [!DNL Commerce] (según las políticas de Amazon). |

## Ejemplo: completado por Amazon (FBA)

| Etapa | Descripción |
|---|---|
| 1 | **Se realiza un pedido completado por Amazon en Amazon.** |
| 2 | **Se importa el pedido.** El pedido no se importa en el canal de ventas de Amazon hasta que se asigne al pedido el `Shipped` estado por Amazon. Dado que Amazon tiene el inventario para este producto, evita interferencias con la administración del almacén/inventario. |
| 3 | **Se actualizan los detalles del pedido.** Si está configurado en su [configuración de pedidos](./order-settings.md), el orden de Amazon crea el correspondiente [!DNL Commerce] y se creará como un pedido con un estado de `Complete`. |
