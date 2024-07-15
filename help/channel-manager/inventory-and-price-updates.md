---
title: Actualizaciones de inventario y precio
description: '[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre el almacén  [!DNL Commerce] y [!DNL Walmart Marketplace] para que puedas administrar tus operaciones de canal de ventas desde el administrador [!DNL Commerce] Administrador'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Actualizar inventario y precios

[!DNL Channel Manager] realiza un seguimiento del inventario y los precios de los productos en el catálogo de productos [!DNL Commerce] y sincroniza las actualizaciones con el canal de ventas conectado y [!DNL Walmart Marketplace]. La operación de sincronización garantiza que las listas de productos reflejen la cantidad de stock y los precios actuales.


>[!IMPORTANT]
>
>Después de instalar y configurar [!DNL Channel Manager], todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. Si ya vende en Walmart Marketplace, asegúrese de desactivar cualquier otra integración que actualice los datos del producto y del pedido. A continuación, compruebe que los niveles y precios de existencias de inventario de la tienda [!DNL Commerce] son precisos y coinciden con los datos de [!DNL Walmart Marketplace] antes de conectar [!DNL Channel Manager] a la tienda en directo del mercado.


## Actualizaciones de inventario

Cuando cambia el nivel de inventario de productos en [!DNL Commerce], [!DNL Channel Manager] sincroniza las actualizaciones con [!DNL Walmart Marketplace]. Las actualizaciones de inventario pueden tardar hasta 10 minutos en sincronizarse en todo el canal de ventas con [!DNL Walmart marketplace].

* **Actualizaciones de la cantidad de existencias en el catálogo de productos**: cuando [!DNL Commerce] cambia la cantidad de existencias debido a [cambios manuales en la cantidad de existencias](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), reembolsos o cancelaciones, [!DNL Channel Manager] sincroniza el cambio con los canales conectados y [!DNL Walmart Marketplace].

* **Reducir la cantidad de existencias para reflejar [!DNL Walmart Marketplace] pedidos**—Después de que un pedido de [!DNL Walmart Marketplace] se sincronice con [!DNL Channel Manager], [!DNL Channel Manager] envía la actualización al sistema de pedidos de [!DNL Commerce]. [!DNL Commerce] ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con [!DNL Walmart Marketplace]. Hasta que se completen las operaciones de sincronización, es posible que vea cantidades diferentes en los listados de canales de ventas y en [!DNL Walmart].

>[!IMPORTANT]
>
>Después de que un pedido de [!DNL Walmart Marketplace] se sincronice con [!DNL Channel Manager], las cantidades de inventario y la información del pedido se actualizan solamente para los reembolsos y cancelaciones iniciados desde [!DNL Commerce]. Si se devuelve o cancela un pedido de [!DNL Walmart marketplace], procese el cambio de [!DNL Commerce] para garantizar la precisión de [!DNL Commerce] cantidades de inventario e información del pedido.

## Actualizaciones de precios

Cuando el precio del producto cambia en [!DNL Commerce], [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace]. El cambio de precio puede tardar hasta cinco minutos en mostrarse en el anuncio [!DNL Walmart Marketplace].

### Administración de precios de un producto conectado

1. En [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula de productos, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

Para obtener ayuda para administrar la configuración de precios de productos en [!DNL Commerce], consulte [Administrar precios](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
