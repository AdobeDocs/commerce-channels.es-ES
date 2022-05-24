---
title: Acerca de [!DNL Channel Manager]
description: Obtenga información sobre cómo instalar y utilizar [!DNL Channel Manager] para integrar las tiendas de Adobe Commerce y de Magento Open Source con mercados de terceros, y crear un canal de ventas para administrar las ofertas, los precios, el inventario y las ventas de Marketplace sin problemas desde el administrador de comercio.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 9ccd205ccd4f4b3f4e6b9fed2c4d16893f4b0da8
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Acerca de [!DNL Channel Manager]

[!DNL Channel Manager] le ayuda a aumentar las ventas y a llegar a nuevos clientes integrando su catálogo de productos de Adobe Commerce o de Magento Open Source con el [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] vista de administración de extensiones](assets/channel-manager-home.png)

Channel Manager es compatible con los vendedores de Adobe Commerce o Magento Open Source que desean vender en Walmart Marketplace.

Después de instalar y configurar [!DNL Channel Manager], el [!DNL Commerce] El administrador se ha ampliado para que pueda administrar [!DNL Walmart Marketplace] operaciones de ventas sin problemas desde su entorno de comercio.

* **Administración de listas**-Publica fácilmente listados de productos al hacer coincidir productos de tu catálogo de comercio con los listados existentes de Walmart Marketplace.

* **Inventory management**-Los artículos de la cuenta de vendedor de mercado del comerciante se sincronizan y actualizan automáticamente desde Commerce para garantizar niveles de inventario precisos.

* **Actualizaciones de precios**-Mantener precios precisos para anuncios de mercado con sincronización automática de precios. Cuando un precio cambia en Adobe Commerce, los cambios se reflejan en el mercado en 10 minutos.

* **Gestión de pedidos**-Cuando se crean nuevos pedidos en un mercado, el Administrador de canales sincroniza los pedidos con Adobe Commerce y envía los acuses de recibo al mercado para garantizar que el inventario se reserva para cada pedido.

* **Administración de envíos**-Cuando los pedidos se marcan como enviados en Adobe Commerce, la actualización del envío se envía al [!DNL Walmart Marketplace]. Esta notificación garantiza que los vendedores cumplan los requisitos del SLA de cumplimiento y que los clientes reciban notificaciones de actualización de envío para sus pedidos actuales.

* **Cancelaciones**-Cuando los pedidos se cancelan en Adobe Commerce, el Administrador de canales envía información actualizada del pedido al mercado para replicar la acción del pedido de mercado correspondiente.

## Latencia esperada para las operaciones del Administrador de canales

Los procesos de sincronización de datos entre [!DNL Channel Manager] y un [!DNL Walmart Marketplace] la tienda requiere un poco de tiempo para completarse. Revise el tiempo de procesamiento esperado para [!DNL Channel Manager] para ayudar a planificar las operaciones del canal de ventas.

**Latencia estimada para operaciones del Administrador de canales**

| **Operación** | **Descripción** | **Retraso esperado** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Agregar productos al Administrador de canales | Seleccione productos del catálogo de productos de Commerce e impórtelos en el Administrador de canales. | **Hasta cinco minutos**-Si selecciona muchos productos, por ejemplo, un catálogo completo de productos, el proceso de importación tarda más. |
| Hacer coincidir productos en Walmart Marketplace | Seleccione las listas de productos en Channel Manager y envíelas a Walmart para que coincidan. | **Hasta 30 minutos**-Si selecciona muchos productos, el proceso de coincidencia tardará más en función de la cantidad seleccionada. |
| Actualizaciones de inventario | Cuando cambia la cantidad de inventario en Commerce, [!DNL Channel Manager] sincroniza la actualización con Walmart. | **Hasta 10 minutos** |
| Actualizaciones de precios | Cuando el precio de un producto cambia, Channel Manager sincroniza la actualización con Walmart. | **Hasta cinco minutos** |
| Solicite sincronizaciones de Walmart a Commerce | El cliente solicita un producto Commerce en el mercado Walmart. Walmart envía el pedido a Channel Manager. El orden se muestra en el panel de pedidos. | **Hasta 30 minutos** |
| Pedido creado en Commerce Order Management | Channel Manager crea el pedido de comercio a partir del pedido de Walmart y actualiza el panel de pedidos para incluir el número de pedido de comercio. | **Hasta cinco minutos** |

