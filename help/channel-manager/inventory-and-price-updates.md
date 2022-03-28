---
title: Actualizaciones de inventario y precios
description: '''[!DNL Channel Manager] sincroniza las actualizaciones de inventario y precio entre Commerce store y [!DNL Walmart Marketplace] para que pueda administrar sus operaciones de canal de ventas desde el administrador de comercio'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Actualizaciones de inventario y precios

[!DNL Channel Manager] realiza un seguimiento del inventario y los precios de los productos en el almacén de canales. Cuando cambia el inventario o el precio, las actualizaciones se sincronizan con ambas [!DNL Channel Manager] y [!DNL Walmart Marketplace] para reflejar la cantidad de stock actual y los precios en las listas de productos.

## Actualizaciones de inventario

Cuando cambian los niveles de inventario, Channel Manager sincroniza las actualizaciones entre Commerce y Walmart Marketplace para garantizar que Channel Manager y Walmart Marketplace tengan la cantidad de stock correcta.

Las actualizaciones de inventario pueden tardar hasta 10 minutos en sincronizarse entre el Administrador de canales y el mercado.

* **Actualizaciones de la cantidad de existencias en el catálogo de productos**-Cuando la cantidad de existencias de comercio cambia debido a [cambios en la cantidad de stock manual](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), reembolsos o cancelaciones, el Administrador de canales sincroniza el cambio con los canales conectados y [!DNL Walmart Marketplace].

* **Reduzca la cantidad de existencias para reflejar los pedidos de Walmart Marketplace**-Después de sincronizar un pedido de Walmart Marketplace con Channel Manager, Channel Manager envía la actualización al sistema de pedidos de comercio. El comercio ajusta las cantidades de stock según el pedido. A continuación, la cantidad actualizada se sincroniza con Walmart Marketplace. Hasta que se completen las operaciones de sincronización, es posible que vea diferencias de cantidad entre Channel Manager y Marketplace.

>[!IMPORTANT]
>
> Después de sincronizar los pedidos de Walmart Marketplace con Channel Manager, las cantidades de inventario y la información de los pedidos se actualizan solo para los reembolsos y cancelaciones iniciadas desde Commerce. Si un pedido es reembolsado o cancelado desde el mercado Walmart, procese el cambio desde Commerce para garantizar la precisión de las cantidades de inventario de Commerce y la información de pedidos.

## Actualizaciones de precios

Cuando el precio del producto cambia en Commerce, Channel Manager sincroniza la actualización desde el [!DNL Commerce] catálogo de productos a [!DNL Walmart Marketplace]. El mercado puede tardar hasta cinco minutos en mostrar los cambios de precios.

### Administrar precios de un producto publicado

1. En el [!UICONTROL Admin], seleccione **[!UICONTROL Catalog > Products]**.
1. En la cuadrícula del producto, busque el producto que desea actualizar y seleccione **[!UICONTROL Edit]**.
1. Revise y actualice el precio según sea necesario.
1. **[!UICONTROL Save]** el cambio.

Para obtener más información sobre la administración de la configuración de precios de productos en Commerce, consulte [Administrar precios](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
