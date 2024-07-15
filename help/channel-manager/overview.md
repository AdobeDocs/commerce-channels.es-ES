---
title: 'Introducción a  [!DNL Channel Manager]'
description: '"Aprenda a instalar y usar [!DNL Channel Manager] para integrar tiendas Adobe Commerce y Magento Open Source con Walmart Marketplace y crear un canal de ventas para administrar listas de mercado, precios, inventario y ventas sin problemas de su administrador de Commerce".'
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Introducción a [!DNL Channel Manager]

[!DNL Channel Manager] ayuda a los comerciantes a aumentar sus ventas, llegar a nuevos clientes, optimizar las operaciones de ventas y ahorrar tiempo al integrar un catálogo de productos de Adobe Commerce o de Magento Open Source con [!DNL Walmart Marketplace].

![[!DNL Channel Manager] vista de administración de la extensión](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] admite comerciantes de Adobe Commerce o Magento Open Source que deseen vender en [!DNL Walmart Marketplace] ampliando el administrador de [!DNL Commerce]. Con [!DNL Channel Manager] instalado, los administradores de tiendas y el personal de operaciones pueden administrar [!DNL Walmart Marketplace] ventas, inventario y precios de productos sin problemas desde el entorno de Commerce.

El administrador ampliado optimiza las operaciones porque los comerciantes pueden usar los mismos flujos de trabajo y procesos para administrar las ventas tanto de las tiendas de [!DNL Commerce] como de Walmart Marketplace.

Después de instalar y configurar [!DNL Channel Manager], puede usar las siguientes capacidades para administrar los pedidos de ventas de Walmart Marketplace:

* **Administración de listados**: conecta fácilmente listados de productos haciendo coincidir productos de tu catálogo [!DNL Commerce] con listados de [!DNL Walmart Marketplace] existentes.

* **Inventory management**: los artículos de la cuenta de vendedor de marketplace del comerciante se sincronizan y actualizan automáticamente desde [!DNL Commerce] para garantizar niveles de inventario precisos.

* **Actualizaciones de precios**: mantén los precios precisos de los anuncios de mercado con sincronización automática de precios. Cuando un precio cambia en Adobe Commerce, los cambios se reflejan en el mercado.

* **Administración de pedidos**: cuando se crean nuevos pedidos en el mercado, [!DNL Channel Manager] sincroniza los pedidos con Adobe Commerce y envía confirmaciones de pedidos al mercado. Esta confirmación garantiza que el inventario se reserve para cada pedido. El paso final es crear los pedidos correspondientes en el sistema Order Management [!DNL Commerce] para su procesamiento.

* **Administración de envíos**: cuando los pedidos se marcan como enviados en Adobe Commerce, la actualización de envío se envía a [!DNL Walmart Marketplace]. Esta notificación garantiza que los vendedores cumplan los requisitos de SLA y que los clientes reciban notificaciones de actualización de envío para sus pedidos actuales.

* **Cancelaciones**: cuando se cancelan pedidos en Adobe Commerce, [!DNL Channel Manager] envía información de pedidos actualizada al mercado para replicar la acción del pedido del mercado correspondiente. Una vez finalizada la cancelación del pedido, las [!DNL Commerce] actualizaciones de cantidad de existencias para reflejar los artículos devueltos y las actualizaciones de inventario se sincronizan automáticamente con [!DNL Walmart Marketplace].

* **Devoluciones y reembolsos**: cuando Walmart Marketplace solicita una devolución de elementos pedidos a través del canal de ventas de Adobe Commerce o del Magento Open Source, [!DNL Channel Manager] envía la información de la solicitud de devolución al almacén del canal de ventas de Commerce para replicar la solicitud de devolución. A continuación, el reembolso se puede procesar mediante el [!DNL Commerce] [flujo de trabajo de reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow), método sin conexión. Una vez completado el reembolso, [!DNL Channel Manager] sincroniza la actualización con Walmart para que el estado de devolución en la cuenta de vendedor de Marketplace se pueda actualizar para reflejar el reembolso.

## Latencia esperada para [!DNL Channel Manager] operaciones

Los procesos de sincronización de datos entre [!DNL Channel Manager] y un almacén de [!DNL Walmart Marketplace] vinculado requieren algún tiempo para completarse. Revise el tiempo de procesamiento esperado de [!DNL Channel Manager] operaciones para ayudar a planificar el funcionamiento de las operaciones del canal de ventas.

**Latencia estimada para [!DNL Channel Manager] operaciones**

| **Operación** | **Descripción** | **Retraso esperado** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Agregar productos a [!DNL Channel Manager] | Seleccione productos del catálogo de productos [!DNL Commerce] e impórtelos a [!DNL Channel Manager]. | **Hasta cinco minutos**: si selecciona muchos productos, por ejemplo, un catálogo completo de productos, el proceso de importación tarda más. |
| Hacer coincidir productos en [!DNL Walmart Marketplace] | Seleccione listados de productos en [!DNL Channel Manager] y envíelos a Walmart para que se comparen. | **Hasta 30 minutos**: si selecciona muchos productos, el proceso de coincidencia tarda más en función de la cantidad seleccionada. |
| Actualizaciones de inventario | Cuando cambia la cantidad de inventario en Commerce, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta 10 minutos** |
| Actualizaciones de precios | Cuando cambia el precio de un producto, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta cinco minutos** |
| Ordenar sincronizaciones de Walmart a [!DNL Commerce] | El cliente solicita un producto [!DNL Commerce] en Walmart Marketplace. Walmart envía el pedido a [!DNL Channel Manager]. El orden se muestra en el panel de orden. | **Hasta 30 minutos** |
| Pedido creado en [!DNL Commerce] Order Management | [!DNL Channel Manager] crea el pedido [!DNL Commerce] a partir del pedido de Walmart y actualiza el panel de pedidos para incluir el número de pedido [!DNL Commerce]. | **Hasta cinco minutos** |
| Actualización del estado de envío en [!DNL Commerce] Order Management | Cuando se envía un pedido desde Commerce, [!DNL Channel Manager] actualiza el estado de envío en el panel de pedidos y envía la actualización a Walmart Marketplace para que se pueda notificar al cliente. | **Hasta cinco minutos** |
| Actualización de cancelación de pedidos en Commerce Order Management | Cuando se cancela un pedido de Commerce, [!DNL Channel Manager] actualiza el estado del pedido en el panel de pedidos y envía la actualización a Walmart Marketplace para que se pueda notificar al cliente. Una vez finalizada la cancelación del pedido, la cantidad de existencias [!DNL Commerce] se actualiza para reflejar los artículos devueltos. A continuación, [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace]. | **Hasta cinco minutos** |


