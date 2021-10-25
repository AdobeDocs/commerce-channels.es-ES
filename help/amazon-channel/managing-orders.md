---
title: Administrar pedidos
description: Puede habilitar la importación de pedidos en la Configuración de pedidos para administrar más fácilmente sus pedidos de Amazon desde el administrador de comercio.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 1d1b888db4de4f6e3658af768cd6f5cf30828788
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Administrar pedidos

Puede ver la información de pedidos de Amazon, tal como se recibió de Amazon, en la _[!UICONTROL Recent Orders]_de la sección [tablero de almacenamiento](./amazon-store-dashboard.md) o en el_[!UICONTROL Amazon orders]_ (también denominada _[!UICONTROL All Orders]_vista).

La forma en que gestione sus pedidos de Amazon depende de si la importación de pedidos está habilitada o deshabilitada en su [Configuración de pedidos](./order-settings.md#configure-order-settings).

## Con la importación de pedidos habilitada

Después [integración de tiendas](./store-integration.md), el [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) configurar es `Enabled` de forma predeterminada. Con esta configuración, corresponde a [!DNL Commerce] los pedidos se crean para sus pedidos de Amazon y se pueden administrar en la variable [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} flujo de trabajo.

>[!NOTE]
>
>Independientemente de la configuración de importación de pedidos, los pedidos de Amazon que existían en su [!DNL Amazon Seller Central] la cuenta antes de [integración de tiendas](./store-integration.md) no se importan.

Los pedidos de Amazon importados se administran en la variable [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} flujo de trabajo, igual que el resto [!DNL Commerce] tiendas. Haga clic en el número de pedido de Amazon en la *[!UICONTROL Order Number]* para abrir el orden en la [[!DNL Commerce] proceso de pedido](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Consulte [Ver pedidos de Amazon](./amazon-orders-all.md).

### Proceso de importación de pedidos

Cuando se realiza un pedido en Amazon y [importación de pedidos](./order-settings.md) se habilita, se inicia el siguiente proceso.

| Cambiar | Acciones |
|---|---|
| Se coloca un pedido en Amazon. | <ul><li>Amazon establece el estado de pedido en `Pending`.</li><li>La información del pedido se envía a [!DNL Commerce].</li><li>El pedido se agrega a [_Pedidos de Amazon_ tabla](./amazon-orders-all.md) con un `Pending` estado.</li></ul> |
| Amazon cambia el estado de pedido a `Unshipped`. | <ul><li>El cambio de estado se envía a [!DNL Commerce].</li><li>En el [_Pedidos de Amazon_ tabla](./amazon-orders-all.md), el estado del pedido cambia a `Unshipped`.</li><li>En el [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, una [!DNL Commerce] el pedido se crea con un `Processing` estado.</li></ul> |
| En [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, la variable [!DNL Commerce] se procesa el pedido y el estado cambia a `Shipped`. | <ul><li>En el [_Pedidos de Amazon_ tabla](./amazon-orders-all.md), el estado del pedido cambia a `Shipped`.</li><li>En el siguiente trabajo cron, el estado de pedido cambia a `Complete` en el [[!DNL Commerce] flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.</li></ul> |

### Bloqueadores de creación de pedidos

Hay algunos escenarios que impiden la creación de la [!DNL Commerce] pedido. [!DNL Commerce] los pedidos no se crean para pedidos que se reciben cuando se produce cualquiera de los siguientes problemas.

| Situación | Solución |
|---|---|
| El elemento no existe en la variable [!DNL Commerce] catálogo. | [Crear el producto](./creating-assigning-catalog-products.md) en su [!DNL Commerce] catálogo y [coincidencia manual](./creating-assigning-catalog-products.md) al producto. |
| El elemento del catálogo está desactivado. | Asegúrese de que la variable [estado del producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} está habilitado. |
| El artículo solicitado no está en existencias. | Actualice o configure el [opciones de producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} para la cantidad y el origen. |

Cuando no se pueden importar los pedidos, aparece un mensaje del sistema similar al siguiente en la parte superior de la pantalla:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Cuando se resuelve el problema, la variable [!DNL Commerce] se crea en la siguiente sincronización.

## Con la importación de pedidos deshabilitada

Si no desea importar y administrar sus pedidos de Amazon en [!DNL Commerce], puede cambiar el [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) configurar como `Disabled`. Esta configuración significa que cuando se reciben nuevos pedidos de Amazon, los correspondientes [!DNL Commerce] no se crean los pedidos.

Cuando está desactivado, la información de pedido recibida de Amazon aparece en la sección _[!UICONTROL Recent Orders]_del panel de almacenamiento y en la sección_[!UICONTROL All Orders]_ vista. Esta información de pedido es de solo consulta y debe administrar estos pedidos en [!DNL Amazon Seller Central]. Para abrir los detalles del pedido en [!DNL Amazon Seller Central], haga clic en el número de orden de Amazon en la _[!UICONTROL Order Number]_para abrir el Navegador.

Consulte también [Ver pedidos de Amazon](./amazon-orders-all.md), [Ver detalles de pedidos de Amazon](./amazon-order-details.md)y [Tareas comunes de procesamiento de pedidos](./common-order-processing.md).
