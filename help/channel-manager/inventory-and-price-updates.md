---
title: Actualizaciones de inventario y precios
description: '''[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre Commerce store y [!DNL Walmart Marketplace] para que pueda administrar sus operaciones de canal de ventas desde el administrador de comercio'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 71ad5e3bc9ff6b909943a161472e4db7d375683f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Actualizar inventario y precios

[!DNL Channel Manager] realiza un seguimiento del inventario y los precios de los productos en la variable [!DNL Commerce] catálogo de productos y sincroniza las actualizaciones del canal de ventas conectado y [!DNL Walmart Marketplace]. La sincronización garantiza que las listas de productos reflejen la cantidad de existencias y los precios actuales.

## Actualizaciones de inventario

Cuando los niveles de inventario de productos cambian en [!DNL Commerce], [!DNL Channel Manager] sincroniza las actualizaciones del canal de ventas y del [!DNL Walmart Marketplace]. Las actualizaciones de inventario pueden tardar hasta 10 minutos en sincronizarse entre el canal de ventas y el [!DNL Walmart marketplace].

* **Actualizaciones de la cantidad de existencias en el catálogo de productos**—When [!DNL Commerce] cambios en la cantidad de stock debido a [cambios en la cantidad de stock manual](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), reembolsos o cancelaciones, [!DNL Channel Manager] sincroniza el cambio con canales conectados y [!DNL Walmart Marketplace].

* **Reducir la cantidad de existencias para reflejar [!DNL Walmart Marketplace] pedidos**—Después de un [!DNL Walmart Marketplace] solicitar sincronizaciones a [!DNL Channel Manager], [!DNL Channel Manager] envía la actualización al [!DNL Commerce] sistema de pedidos. [!DNL Commerce] ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con [!DNL Walmart Marketplace]. Hasta que se hayan completado las operaciones de sincronización, es posible que vea cantidades diferentes en los listados del canal de ventas y [!DNL Walmart].

>[!IMPORTANT]
>
>Después de un [!DNL Walmart Marketplace] solicitar sincronizaciones a [!DNL Channel Manager], las cantidades de inventario y la información de pedidos se actualizan solo para los reembolsos y cancelaciones iniciadas a partir de [!DNL Commerce]. Si se reembolsa o cancela un pedido de la [!DNL Walmart marketplace], procesar el cambio de [!DNL Commerce] para garantizar la exactitud de [!DNL Commerce] cantidades de inventario e información de pedido.

## Actualizaciones de precios

Cuando el precio del producto cambia en [!DNL Commerce], [!DNL Channel Manager] sincroniza la actualización con [!DNL Walmart Marketplace]. El cambio de precio puede tardar hasta cinco minutos en mostrarse en la variable [!DNL Walmart Marketplace] listado.

### Administrar precios de un producto publicado

1. En el [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula del producto, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

Para obtener ayuda sobre la administración de la configuración de precios de productos en [!DNL Commerce], consulte [Administrar precios](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
