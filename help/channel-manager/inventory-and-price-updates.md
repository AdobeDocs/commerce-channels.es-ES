---
title: Actualizaciones de inventario y precio
description: '[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre [!DNL Commerce] tienda y [!DNL Walmart Marketplace] para que pueda administrar las operaciones de canal de ventas desde [!DNL Commerce] Administrador'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Actualizar inventario y precios

[!DNL Channel Manager] realiza un seguimiento del inventario y los precios de los productos en la [!DNL Commerce] catálogo de productos y sincroniza las actualizaciones con el canal de ventas conectado y [!DNL Walmart Marketplace]. La operación de sincronización garantiza que las listas de productos reflejen la cantidad de stock y los precios actuales.


>[!IMPORTANT]
>
>Después [!DNL Channel Manager] está instalado y configurado, todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. Si ya vende en Walmart Marketplace, asegúrese de desactivar cualquier otra integración que actualice los datos del producto y del pedido. A continuación, compruebe que los niveles y precios de existencias de inventario en la variable [!DNL Commerce] tienda son precisos y coinciden con los datos de [!DNL Walmart Marketplace] antes de conectarse [!DNL Channel Manager] a la tienda del mercado en directo.


## Actualizaciones de inventario

Cuando los niveles de inventario de productos cambian en [!DNL Commerce], [!DNL Channel Manager] sincroniza actualizaciones con el [!DNL Walmart Marketplace]. Las actualizaciones de inventario pueden tardar hasta 10 minutos en sincronizarse en todo el canal de ventas con [!DNL Walmart marketplace].

* **Actualizaciones de la cantidad de stock en el catálogo de productos**: cuando [!DNL Commerce] la cantidad de existencias cambia debido a [cambios manuales de cantidad de stock](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), reembolsos o cancelaciones, [!DNL Channel Manager] sincroniza el cambio con los canales conectados y [!DNL Walmart Marketplace].

* **Reducir la cantidad de stock para reflejar [!DNL Walmart Marketplace] pedidos**: después de un [!DNL Walmart Marketplace] sincronizaciones de pedidos a [!DNL Channel Manager], [!DNL Channel Manager] envía la actualización a [!DNL Commerce] sistema de pedidos. [!DNL Commerce] ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con [!DNL Walmart Marketplace]. Hasta que se completen las operaciones de sincronización, es posible que vea cantidades diferentes en los listados de canales de ventas y [!DNL Walmart].

>[!IMPORTANT]
>
>Después de un [!DNL Walmart Marketplace] sincronizaciones de pedidos a [!DNL Channel Manager], las cantidades de inventario y la información de pedidos solo se actualizan para devoluciones y cancelaciones iniciadas desde [!DNL Commerce]. Si un pedido es reembolsado o cancelado de la [!DNL Walmart marketplace], procesar el cambio de [!DNL Commerce] para garantizar la precisión de [!DNL Commerce] cantidades de inventario e información de pedidos.

## Actualizaciones de precios

Cuando el precio del producto cambie en [!DNL Commerce], [!DNL Channel Manager] sincroniza la actualización con el [!DNL Walmart Marketplace]. El cambio de precio puede tardar hasta cinco minutos en mostrarse en la [!DNL Walmart Marketplace] listado.

### Administración de precios de un producto conectado

1. Desde el [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula de productos, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

Para obtener ayuda sobre la administración de la configuración de precios de productos en [!DNL Commerce], consulte [Administrar precios](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
