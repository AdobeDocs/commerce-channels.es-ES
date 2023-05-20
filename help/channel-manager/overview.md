---
title: 'Introducción a [!DNL Channel Manager]'
description: '"Aprenda a instalar y utilizar [!DNL Channel Manager] integrar tiendas Adobe Commerce y Magento Open Source con Walmart Marketplace y crear un canal de ventas para administrar listados de marketplace, precios, inventario y ventas sin problemas desde su administrador de comercio".'
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Introducción a [!DNL Channel Manager]

[!DNL Channel Manager] ayuda a los comerciantes a aumentar sus ventas, llegar a nuevos clientes, optimizar las operaciones de ventas y ahorrar tiempo mediante la integración de un catálogo de productos Adobe Commerce o de Magento Open Source con [!DNL Walmart Marketplace].

![[!DNL Channel Manager] vista de administración de extensiones](assets/channel-manager-home.png)

[!DNL Channel Manager] admite comerciantes Adobe Commerce o Magento Open Source que deseen vender en [!DNL Walmart Marketplace] ampliando el [!DNL Commerce] Administrador. Con [!DNL Channel Manager] instalado, los administradores de tienda y el personal de operaciones pueden gestionar [!DNL Walmart Marketplace] ventas, inventario y precios de productos sin problemas desde el entorno de Commerce.

El administrador ampliado optimiza las operaciones porque los comerciantes pueden utilizar los mismos flujos de trabajo y procesos para administrar las ventas de ambos [!DNL Commerce] tiendas y el mercado Walmart.

Después de instalar y configurar [!DNL Channel Manager], puede utilizar las siguientes capacidades para administrar los pedidos de ventas de Walmart Marketplace:

* **Administración de listados**-Conecte fácilmente listados de productos haciendo coincidir productos de su [!DNL Commerce] catálogo a existente [!DNL Walmart Marketplace] anuncios.

* **Inventory management**-Los artículos de la cuenta de vendedor de marketplace del comerciante se sincronizan y actualizan automáticamente a partir de [!DNL Commerce] para garantizar niveles de inventario precisos.

* **Actualizaciones de precios**: permite mantener unos precios precisos para los anuncios del mercado con sincronización automática de precios. Cuando un precio cambia en Adobe Commerce, los cambios se reflejan en el mercado.

* **Order Management**: cuando se crean nuevos pedidos en el mercado, [!DNL Channel Manager] sincroniza pedidos con Adobe Commerce y envía confirmaciones de pedidos al mercado. Esta confirmación garantiza que el inventario se reserve para cada pedido. El paso final es crear los pedidos correspondientes en la [!DNL Commerce] Sistema de Order Management para el procesamiento.

* **Administración de envíos**: cuando los pedidos se marcan como enviados en Adobe Commerce, la actualización del envío se envía a [!DNL Walmart Marketplace]. Esta notificación garantiza que los vendedores cumplan los requisitos de SLA y que los clientes reciban notificaciones de actualización de envío para sus pedidos actuales.

* **Cancelaciones**—Cuando los pedidos se cancelan en Adobe Commerce, [!DNL Channel Manager] envía información de pedido actualizada al mercado para replicar la acción del pedido del mercado correspondiente. Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] las actualizaciones de cantidad de existencias para reflejar los artículos devueltos y las actualizaciones de inventario se sincronizan automáticamente con [!DNL Walmart Marketplace].

* **Devoluciones y reembolsos**: cuando Walmart Marketplace solicita una devolución para los artículos pedidos a través del canal de ventas de Adobe Commerce o del Magento Open Source, [!DNL Channel Manager] envía la información de la solicitud de devolución al almacén del canal de ventas de Commerce para replicar la solicitud de devolución. A continuación, el reembolso se puede procesar utilizando el [!DNL Commerce] [flujo de trabajo de reembolsos](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow), método sin conexión. Una vez completado el reembolso, [!DNL Channel Manager] sincroniza la actualización a Walmart para que el estado de devolución en la cuenta de vendedor del marketplace se pueda actualizar para reflejar el reembolso.

## Latencia esperada para [!DNL Channel Manager] operaciones

Los procesos de sincronización de datos entre [!DNL Channel Manager] y un vínculo [!DNL Walmart Marketplace] la tienda requiere algún tiempo para completarse. Revise el tiempo de procesamiento esperado para [!DNL Channel Manager] operaciones para planificar el funcionamiento de las operaciones del canal de ventas.

**Latencia estimada para [!DNL Channel Manager] operaciones**

| **Operación** | **Descripción** | **Retraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Añadir productos a [!DNL Channel Manager] | Seleccione productos de la [!DNL Commerce] catálogo de productos e importarlos en [!DNL Channel Manager]. | **Hasta cinco minutos**-Si selecciona muchos productos, por ejemplo, un catálogo de productos completo, el proceso de importación tarda más. |
| Hacer coincidir productos en [!DNL Walmart Marketplace] | Seleccionar listados de productos en [!DNL Channel Manager] y enviar a Walmart para buscar coincidencias. | **Hasta 30 minutos**-Si selecciona muchos productos, el proceso de coincidencia tarda más en función de la cantidad seleccionada. |
| Actualizaciones de inventario | Cuando cambie la cantidad de inventario en Commerce, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta 10 minutos** |
| Actualizaciones de precios | Cuando cambia el precio de un producto, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta cinco minutos** |
| Ordenar sincronizaciones de Walmart a [!DNL Commerce] | El cliente solicita un [!DNL Commerce] producto en Walmart Marketplace. Walmart envía el pedido a [!DNL Channel Manager]. El orden se muestra en el panel de orden. | **Hasta 30 minutos** |
| Pedido creado en [!DNL Commerce] Order Management | [!DNL Channel Manager] crea el [!DNL Commerce] pedido de Walmart y actualiza el panel de pedidos para incluir el [!DNL Commerce] número de pedido. | **Hasta cinco minutos** |
| Actualización del estado de envío en [!DNL Commerce] Order Management | Cuando se envía un pedido desde Commerce, [!DNL Channel Manager] actualiza el estado de Envío en el panel de pedidos y envía la actualización a Walmart Marketplace para que se pueda notificar al cliente. | **Hasta cinco minutos** |
| Actualización de cancelación de pedidos en Commerce Order Management | Cuando se cancela un pedido desde Commerce, [!DNL Channel Manager] actualiza el estado del pedido en el panel de pedidos y envía la actualización a Walmart Marketplace para que se pueda notificar al cliente. Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] actualizaciones de cantidad de stock para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con el [!DNL Walmart Marketplace]. | **Hasta cinco minutos** |


