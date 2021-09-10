---
title: Administrar pedidos
description: Puede habilitar la importación de pedidos en la Configuración de pedidos para administrar más fácilmente sus pedidos de Amazon desde el administrador de comercio.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Administrar pedidos

Puede ver la información de su pedido de Amazon, tal como se recibió de Amazon, en la sección _[!UICONTROL Recent Orders]_del [panel de almacenamiento](./amazon-store-dashboard.md) o en la página_[!UICONTROL Amazon orders]_ (también denominada vista _[!UICONTROL All Orders]_).

La forma de administrar los pedidos de Amazon depende de si la importación de pedidos está habilitada o deshabilitada en la [Configuración de pedidos](./order-settings.md#configure-order-settings).

## Con la importación de pedidos habilitada

Después de la [integración del almacén](./store-integration.md), la configuración [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) es `Enabled` de forma predeterminada. Con esta configuración, se crean los [!DNL Commerce] pedidos correspondientes para sus pedidos de Amazon y se pueden administrar en el flujo de trabajo [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Independientemente de la configuración de importación del pedido, los pedidos de Amazon que existían en su cuenta [!DNL Amazon Seller Central] antes de la [integración del almacén](./store-integration.md) no se importan.

Los pedidos de Amazon importados se administran en el flujo de trabajo [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, al igual que sus otros [!DNL Commerce] almacenes. Haga clic en el número de orden de Amazon en la columna *[!UICONTROL Order Number]* para abrir el pedido en el [[!DNL Commerce] proceso de pedido](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Consulte [Ver pedidos de Amazon](./amazon-orders-all.md).

### Proceso de importación de pedidos

Cuando se coloca un pedido en Amazon y [order import](./order-settings.md) está habilitado, se inicia el siguiente proceso.

| Cambiar | Acciones |
|---|---|
| Se coloca un pedido en Amazon. | <ul><li>Amazon establece el estado de pedido en `Pending`.</li><li>La información del pedido se envía a [!DNL Commerce].</li><li>El pedido se agrega a la [_tabla_ órdenes de Amazon](./amazon-orders-all.md) con estado `Pending`.</li></ul> |
| Amazon cambia el estado de pedido a `Unshipped`. | <ul><li>El cambio de estado se envía a [!DNL Commerce].</li><li>En la tabla [_Amazon orders_](./amazon-orders-all.md), el estado del pedido cambia a `Unshipped`.</li><li>En el [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}, se crea un orden [!DNL Commerce] correspondiente con el estado `Processing`.</li></ul> |
| En el [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}, se procesa el pedido [!DNL Commerce] y el estado cambia a `Shipped`. | <ul><li>En la tabla [_Amazon orders_](./amazon-orders-all.md), el estado del pedido cambia a `Shipped`.</li><li>En el siguiente trabajo cron, el estado del pedido cambia a `Complete` en el [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.</li></ul> |

### Bloqueadores de creación de pedidos

Hay algunos escenarios que impiden la creación del orden [!DNL Commerce] correspondiente. [!DNL Commerce] los pedidos no se crean para pedidos que se reciben cuando se produce cualquiera de los siguientes problemas.

| Situación | Solución |
|---|---|
| El elemento no existe en el catálogo [!DNL Commerce]. | [Cree la ](./creating-assigning-catalog-products.md) producción en el  [!DNL Commerce] catálogo y  [haga coincidir manualmente ](./creating-assigning-catalog-products.md) con el producto. |
| El elemento del catálogo está desactivado. | Asegúrese de que el [estado del producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} esté habilitado. |
| El artículo solicitado no está en existencias. | Actualice o configure las [opciones de producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} para la cantidad y el origen. |

Cuando no se pueden importar los pedidos, aparece un mensaje del sistema similar al siguiente en la parte superior de la pantalla:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Cuando se resuelve el problema, el orden [!DNL Commerce] se crea en la siguiente sincronización.

## Con la importación de pedidos deshabilitada

Si no desea importar y administrar sus pedidos de Amazon en [!DNL Commerce], puede cambiar la configuración [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) a `Disabled`. Esta configuración significa que cuando se reciben nuevos pedidos de Amazon, no se crean los [!DNL Commerce] pedidos correspondientes.

Cuando está desactivado, la información de pedido recibida de Amazon aparece en la sección _[!UICONTROL Recent Orders]_del panel de almacenamiento y en la vista_[!UICONTROL All Orders]_. Esta información de pedido es de solo vista y debe administrar estos pedidos en [!DNL Amazon Seller Central]. Para abrir los detalles del pedido en [!DNL Amazon Seller Central], haga clic en el número de pedido de Amazon en la columna _[!UICONTROL Order Number]_.

Consulte también [Ver pedidos de Amazon](./amazon-orders-all.md), [Ver detalles de pedidos de Amazon](./amazon-order-details.md) y [Tareas comunes de procesamiento de pedidos](./common-order-processing.md).
