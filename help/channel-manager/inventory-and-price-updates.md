---
title: Actualizaciones de inventario y precios
description: '''[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre las variables [!DNL Commerce] almacenar y [!DNL Walmart Marketplace] para que pueda administrar las operaciones de canal de ventas desde el [!DNL Commerce] Admin'''
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Actualizar inventario y precios

[!DNL Channel Manager] realiza un seguimiento del inventario y los precios de los productos en la variable [!DNL Commerce] catálogo de productos y sincroniza las actualizaciones del canal de ventas conectado y [!DNL Walmart Marketplace]. La operación de sincronización garantiza que las listas de productos reflejen la cantidad de existencias y los precios actuales.


>[!IMPORTANT]
>
>Después [!DNL Channel Manager] está instalado y configurado, todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. Si ya vende en Walmart Marketplace, asegúrese de desactivar cualquier otra integración que actualice los datos de productos y pedidos. A continuación, verifique que los niveles y precios de las existencias de inventario estén en el [!DNL Commerce] las tiendas son precisas y coinciden con los datos de [!DNL Walmart Marketplace] antes de conectarse [!DNL Channel Manager] a la tienda de mercado en directo.


## Actualizaciones de inventario

Cuando los niveles de inventario de productos cambian en [!DNL Commerce], [!DNL Channel Manager] sincroniza las actualizaciones de [!DNL Walmart Marketplace]. Las actualizaciones de inventario pueden tardar hasta 10 minutos en sincronizarse entre el canal de ventas y el [!DNL Walmart marketplace].

* **Actualizaciones de la cantidad de existencias en el catálogo de productos**—When [!DNL Commerce] cambios en la cantidad de stock debido a [cambios en la cantidad de stock manual](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), reembolsos o cancelaciones, [!DNL Channel Manager] sincroniza el cambio con canales conectados y [!DNL Walmart Marketplace].

* **Reducir la cantidad de existencias para reflejar [!DNL Walmart Marketplace] pedidos**—Después de un [!DNL Walmart Marketplace] solicitar sincronizaciones a [!DNL Channel Manager], [!DNL Channel Manager] envía la actualización al [!DNL Commerce] sistema de pedidos. [!DNL Commerce] ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con [!DNL Walmart Marketplace]. Hasta que se hayan completado las operaciones de sincronización, es posible que vea cantidades diferentes en los listados del canal de ventas y [!DNL Walmart].

>[!IMPORTANT]
>
>Después de un [!DNL Walmart Marketplace] solicitar sincronizaciones a [!DNL Channel Manager], las cantidades de inventario y la información de pedidos se actualizan solo para los reembolsos y cancelaciones iniciadas a partir de [!DNL Commerce]. Si se reembolsa o cancela un pedido de la [!DNL Walmart marketplace], procesar el cambio de [!DNL Commerce] para garantizar la exactitud de [!DNL Commerce] cantidades de inventario e información de pedido.

## Actualizaciones de precios

Cuando el precio del producto cambia en [!DNL Commerce], [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace]. El cambio de precio puede tardar hasta cinco minutos en mostrarse en la variable [!DNL Walmart Marketplace] listado.

### Administrar precios de un producto conectado

1. En el [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula del producto, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

Para obtener ayuda sobre la administración de la configuración de precios de productos en [!DNL Commerce], consulte [Administrar precios](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
