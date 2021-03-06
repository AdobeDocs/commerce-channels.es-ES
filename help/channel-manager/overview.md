---
title: '''Acerca de [!DNL Channel Manager]'''
description: '''Obtenga información sobre cómo instalar y utilizar [!DNL Channel Manager] para integrar las tiendas de Adobe Commerce y Magento Open Source con mercados de terceros y crear un canal de ventas para administrar las ofertas de venta, los precios, el inventario y las ventas de Marketplace sin problemas desde el administrador de comercio.'''
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Acerca de [!DNL Channel Manager]

[!DNL Channel Manager] ayuda a los comerciantes a aumentar las ventas, llegar a nuevos clientes, optimizar las operaciones de ventas y ahorrar tiempo integrando un catálogo de productos Adobe Commerce o Magento Open Source con [!DNL Walmart Marketplace].

![[!DNL Channel Manager] vista de administración de extensiones](assets/channel-manager-home.png)

[!DNL Channel Manager] admite comerciantes de Adobe Commerce o Magento Open Source que deseen realizar ventas en [!DNL Walmart Marketplace] ampliando el [!DNL Commerce] Administrador. con [!DNL Channel Manager] el personal de operaciones y los administradores de almacén instalados puede administrar [!DNL Walmart Marketplace] ventas, inventario y precios de productos sin problemas desde el entorno Commerce.

El administrador ampliado optimiza las operaciones porque los comerciantes pueden utilizar los mismos flujos de trabajo y procesos para administrar las ventas desde ambos [!DNL Commerce] tiendas y Walmart Marketplace.

Después de instalar y configurar [!DNL Channel Manager], puede utilizar las siguientes capacidades para administrar los pedidos de ventas de Walmart Marketplace:

* **Administración de listas**- Conecta fácilmente las listas de productos haciendo coincidir los productos de su [!DNL Commerce] catálogo a existente [!DNL Walmart Marketplace] anuncios.

* **Inventory management**-Los artículos de la cuenta de vendedor de mercado del comerciante se sincronizan y actualizan automáticamente desde [!DNL Commerce] para garantizar niveles de inventario precisos.

* **Actualizaciones de precios**-Mantener precios precisos para anuncios de mercado con sincronización automática de precios. Cuando un precio cambia en Adobe Commerce, los cambios se reflejan en el mercado.

* **Gestión de pedidos**-Cuando se crean nuevos pedidos en un mercado, [!DNL Channel Manager] sincroniza los pedidos con Adobe Commerce y envía los acuses de recibo de los pedidos al mercado. Este reconocimiento garantiza que el inventario se reserva para cada pedido. El paso final es crear los pedidos correspondientes en la [!DNL Commerce] Sistema de gestión de pedidos para su procesamiento.

* **Administración de envíos**-Cuando los pedidos se marcan como enviados en Adobe Commerce, la actualización del envío se envía al [!DNL Walmart Marketplace]. Esta notificación garantiza que los vendedores cumplan los requisitos del SLA de cumplimiento y que los clientes reciban notificaciones de actualización de envío para sus pedidos actuales.

* **Cancelaciones**-Cuando los pedidos se cancelan en Adobe Commerce, [!DNL Channel Manager] envía información actualizada del pedido al mercado para replicar la acción del pedido de mercado correspondiente. Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] las actualizaciones de cantidad de stock para reflejar los artículos devueltos y las actualizaciones de inventario se sincronizan automáticamente con [!DNL Walmart Marketplace].

## Latencia esperada para [!DNL Channel Manager] operaciones

Los procesos de sincronización de datos entre [!DNL Channel Manager] y un [!DNL Walmart Marketplace] la tienda requiere un poco de tiempo para completarse. Revise el tiempo de procesamiento esperado para [!DNL Channel Manager] para ayudar a planificar las operaciones del canal de ventas.

**Latencia estimada para [!DNL Channel Manager] operaciones**

| **Operación** | **Descripción** | **Retraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Añadir productos a [!DNL Channel Manager] | Seleccione los productos de [!DNL Commerce] catálogo de productos e impórtelos en [!DNL Channel Manager]. | **Hasta cinco minutos**-Si selecciona muchos productos, por ejemplo, un catálogo completo de productos, el proceso de importación tarda más. |
| Hacer coincidir productos [!DNL Walmart Marketplace] | Seleccione las listas de productos en [!DNL Channel Manager] y envíelo a Walmart para buscar coincidencias. | **Hasta 30 minutos**-Si selecciona muchos productos, el proceso de coincidencia tardará más en función de la cantidad seleccionada. |
| Actualizaciones de inventario | Cuando cambia la cantidad de inventario en Commerce, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta 10 minutos** |
| Actualizaciones de precios | Cuando cambia el precio de un producto, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta cinco minutos** |
| Solicite sincronizaciones de Walmart a [!DNL Commerce] | El cliente solicita un [!DNL Commerce] en el mercado Walmart. Walmart envía el pedido a [!DNL Channel Manager]. El orden se muestra en el panel de pedidos. | **Hasta 30 minutos** |
| Pedido creado en [!DNL Commerce] Administración de pedidos | [!DNL Channel Manager] crea el [!DNL Commerce] pedido del pedido de Walmart y actualiza el panel de pedidos para incluir el [!DNL Commerce] número de pedido. | **Hasta cinco minutos** |
| Actualización de estado de envío en [!DNL Commerce] Administración de pedidos | Cuando se envía un pedido desde Commerce, [!DNL Channel Manager] actualiza el estado de Envío en el panel de pedidos y envía la actualización al mercado Walmart para que se pueda notificar al cliente. | **Hasta cinco minutos** |
| Actualización de cancelación de pedidos en Commerce Order Management | Cuando se cancela un pedido de Commerce, [!DNL Channel Manager] actualiza el estado del pedido en el panel de pedidos y envía la actualización a Walmart marketplace para que se pueda notificar al cliente. Una vez finalizada la cancelación del pedido, la variable [!DNL Commerce] la cantidad de stock se actualiza para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace]. | **Hasta cinco minutos** |


