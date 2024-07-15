---
title: Flujos de trabajo de Amazon Fulfillment
description: El cumplimiento de un pedido de un anuncio de Amazon sigue una secuencia específica desde la entrega del pedido hasta el envío.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Flujos de trabajo de Amazon Fulfillment

## Ejemplo: completado por el comerciante

| Etapa | Descripción |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Se ha realizado un pedido completado por un comerciante en Amazon.** Amazon asigna el estado `Pending` hasta que se verifique la información de la tarjeta de crédito del cliente. Los pedidos con estado `Pending` se importan automáticamente al canal de ventas de Amazon, pero no se muestran en la ficha _[!UICONTROL Orders]_. |
| 2 | **Amazon ha verificado el pedido.** Cuando se verifica, Amazon cambia el estado a `Unshipped`. Con este cambio de estado, el pedido se actualiza en el canal de ventas de Amazon y aparece en la pestaña _[!UICONTROL Orders]_. |
| 3 | **Se han actualizado los detalles del pedido.** El canal de ventas de Amazon actualiza los detalles del pedido con el precio, el correo electrónico del cliente y el nombre del cliente. Durante esta actualización, el pedido de Amazon crea el pedido de [!DNL Commerce] correspondiente en la página de administración de pedidos. El número de pedido [!DNL Commerce] se muestra con la información del pedido en la ficha _[!UICONTROL Orders]_. |
| 4 | **Se crea una nueva cuenta de cliente.** Si está configurado en la configuración del pedido y el cliente no existe en la base de datos [!DNL Commerce], se crea un nuevo cliente en la base de datos [!DNL Commerce] utilizando la información de cliente correspondiente del pedido de Amazon. Si eligió `No Customer Creation (guest)` en la configuración de su pedido, el pedido sigue el proceso de invitado [!DNL Commerce] y no crea un cliente en la base de datos. En este punto, si el sistema [!DNL Commerce] está integrado con un ERP/OMS/WMS, el pedido se recoge por la integración de un nuevo pedido que se está realizando y creando dentro de [!DNL Commerce]. |
| 5 | **Se ha enviado el pedido.** Desde la página de procesamiento de pedidos [!DNL Commerce], envía el pedido y agrega un número de seguimiento. Cuando todos los elementos se marquen con un estado `Shipped`:<ul><li>El estado del pedido [!DNL Commerce] cambia a `Complete`.</li><li>El estado del pedido del canal de ventas de Amazon cambia a `Shipped`.</li><li>El número de seguimiento se sincroniza con Amazon y el estado del pedido en Amazon cambia a `Shipped`.</li><li>Las notificaciones de envío se envían al cliente a través de Amazon, no desde [!DNL Commerce] (según las políticas de Amazon). |

## Ejemplo: completado por Amazon (FBA)

| Etapa | Descripción |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Se ha realizado un pedido completado por Amazon en Amazon.** |
| 2 | **El pedido se ha importado.** El pedido no se importa al canal de ventas de Amazon hasta que Amazon asigne el estado `Shipped` al pedido. Dado que Amazon tiene el inventario para este producto, evita interferencias con la administración del almacén/inventario. |
| 3 | **Se han actualizado los detalles del pedido.** Si está configurado en su [configuración de pedido](./order-settings.md), el pedido de Amazon crea el pedido de [!DNL Commerce] correspondiente y se creará como un pedido con un estado de `Complete`. |
