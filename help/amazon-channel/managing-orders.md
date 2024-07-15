---
title: Administrar pedidos de Amazon
description: Puede habilitar la importación de pedidos en Configuración de pedidos para administrar más fácilmente los pedidos de Amazon de su administrador de Commerce.
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Administrar pedidos de Amazon

Puede ver la información de pedidos de Amazon, tal como se recibió de Amazon, en la sección _[!UICONTROL Recent Orders]_del [panel de almacén](./amazon-store-dashboard.md) o en la página_[!UICONTROL Amazon orders]_ (también denominada vista _[!UICONTROL All Orders]_).

La forma de administrar los pedidos de Amazon depende de si la importación de pedidos está habilitada o deshabilitada en la [Configuración de pedidos](./order-settings.md#configure-order-settings).

## Con la importación de pedidos habilitada

Después de [integración de tienda](./store-integration.md), la configuración de [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) es `Enabled` de manera predeterminada. Con esta configuración, se crean los [!DNL Commerce] pedidos correspondientes para sus pedidos de Amazon y se pueden administrar en el flujo de trabajo [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Independientemente de la configuración de importación de tus pedidos, los pedidos de Amazon que existían en tu cuenta de [!DNL Amazon Seller Central] antes de tu [integración con la tienda](./store-integration.md) no se importan.

Los pedidos Amazon importados se administran en el flujo de trabajo [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), al igual que las otras tiendas [!DNL Commerce]. Haga clic en el número de pedido de Amazon en la columna *[!UICONTROL Order Number]* para abrir el pedido en el [[!DNL Commerce] proceso de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Consulte [Ver pedidos de Amazon](./amazon-orders-all.md).

### Proceso de importación de pedidos

Cuando se realiza un pedido en Amazon y [order import](./order-settings.md) está habilitado, comienza el siguiente proceso.

| Cambiar | Acciones |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Se realiza un pedido en Amazon. | <ul><li>Amazon establece el estado del pedido en `Pending`.</li><li>La información del pedido se ha enviado a [!DNL Commerce].</li><li>El pedido se ha agregado a [_pedidos Amazon_ tabla](./amazon-orders-all.md) con un estado `Pending`.</li></ul> |
| Amazon cambia el estado del pedido a `Unshipped`. | <ul><li>El cambio de estado se envió a [!DNL Commerce].</li><li>En la tabla [_Amazon orders_](./amazon-orders-all.md), el estado del pedido cambia a `Unshipped`.</li><li>En el flujo de trabajo [[!DNL Commerce] pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), se crea un pedido [!DNL Commerce] correspondiente con un estado `Processing`.</li></ul> |
| En [[!DNL Commerce] flujo de trabajo de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), el pedido [!DNL Commerce] se procesa y el estado cambia a `Shipped`. | <ul><li>En la tabla [_Amazon orders_](./amazon-orders-all.md), el estado del pedido cambia a `Shipped`.</li><li>En el siguiente trabajo cron, el estado del pedido cambia a `Complete` en el [[!DNL Commerce] flujo de trabajo de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Bloqueadores de creación de pedidos

Hay algunos escenarios que impiden la creación del orden [!DNL Commerce] correspondiente. [!DNL Commerce] pedidos no se crean para pedidos que se reciben cuando se produce cualquiera de los siguientes problemas.

| Escenario | Solución |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El elemento no existe en el catálogo [!DNL Commerce]. | [Cree el producto](./creating-assigning-catalog-products.md) en su catálogo [!DNL Commerce] y [empareje](./creating-assigning-catalog-products.md) manualmente con el producto. |
| El elemento del catálogo está desactivado. | Asegúrese de que el [estado del producto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) esté habilitado. |
| El artículo pedido está agotado. | Actualice o configure las [opciones de producto](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) para la cantidad y el origen. |

Cuando no se pueden importar pedidos, aparece un mensaje del sistema similar al siguiente en la parte superior de la pantalla:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Cuando se resuelva el problema, el pedido de [!DNL Commerce] se creará en la siguiente sincronización.

## Con la importación de pedidos deshabilitada

Si no desea importar y administrar sus pedidos de Amazon en [!DNL Commerce], puede cambiar la configuración de [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) a `Disabled`. Esta configuración significa que cuando se reciben nuevos pedidos desde Amazon, no se crean los [!DNL Commerce] pedidos correspondientes.

Cuando está deshabilitada, la información de pedidos recibida de Amazon aparece en la sección _[!UICONTROL Recent Orders]_del panel de almacén y en la vista_[!UICONTROL All Orders]_. Esta información de pedido es de solo lectura y debe administrar estos pedidos en [!DNL Amazon Seller Central]. Para abrir los detalles del pedido en [!DNL Amazon Seller Central], haga clic en el número de pedido de Amazon en la columna _[!UICONTROL Order Number]_.

Consulte también [Ver pedidos Amazon](./amazon-orders-all.md), [Ver detalles de pedidos Amazon](./amazon-order-details.md) y [Tareas de procesamiento de pedidos comunes](./common-order-processing.md).
