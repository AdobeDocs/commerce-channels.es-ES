---
title: Actualizaciones de inventario y precios
description: '"[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre Commerce store y [!DNL Walmart Marketplace] para que pueda administrar sus operaciones de canal de ventas desde su administrador de comercio"'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# Actualizaciones de inventario y precios

Channel Manager realiza un seguimiento del inventario y los precios de los productos publicados y sincroniza los cambios en Channel Manager y en el mercado Walmart para reflejar la cantidad de acciones y los precios actuales en las listas de productos.**

## Actualizaciones de inventario

Cuando cambian los niveles de inventario, Channel Manager sincroniza las actualizaciones entre el catálogo de productos de Commerce y Walmart Marketplace para que tanto Channel Manager como Walmart Marketplace muestren la cantidad de existencias actual.

Los cambios de inventario pueden tardar hasta 5 minutos en mostrarse en Channel Manager y Walmart Marketplace.

* **Actualizaciones de la cantidad de existencias en el catálogo de productos**-Si la cantidad de acciones de Commerce cambia para un producto que se vende en Walmart debido a un [cambio manual de cantidad de stock](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) Para un reembolso o cancelación de pedido, Channel Manager sincroniza el cambio con el canal de ventas conectado y el [!DNL Walmart Marketplace].

* **Reduzca la cantidad de existencias para reflejar los pedidos de Walmart Marketplace**-Después de sincronizar un pedido de Walmart Marketplace con Channel Manager, Channel Manager envía la actualización al sistema de pedidos de comercio. El comercio ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con Walmart Marketplace. puede haber algunas diferencias en la cantidad de stock que se muestran en el Administrador de canales y en Marketplace hasta que se completen las operaciones de sincronización.

>[!IMPORTANT]
>
> Después de que un pedido de Walmart Marketplace se sincroniza con Channel Manager, las cantidades de inventario y otra información de procesamiento de pedidos se actualiza solamente para los reembolsos y cancelaciones iniciadas desde Commerce. Si un pedido es reembolsado o cancelado desde el mercado Walmart, procese el cambio desde Commerce para asegurarse de que las cantidades de inventario de Commerce y la información de pedidos sean precisas.

## Actualizaciones de precios

Cuando el precio del producto cambia en Commerce, Channel Manager sincroniza la actualización del catálogo de productos de Commerce con Walmart Marketplace. Los cambios de inventario pueden tardar hasta 5 minutos en mostrarse.

### Administrar precios de un producto publicado

1. En el [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula del producto, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

El Administrador de canales sincroniza cualquier actualización de precios en el almacén de canales y [!DNL Walmart Marketplace]. Esta operación puede tardar hasta 5 minutos.

Para obtener más información sobre la administración de la configuración de precios de productos en Commerce, consulte [Administrar precios](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
