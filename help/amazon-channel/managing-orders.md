---
title: Administrar pedidos
description: Puede habilitar la importación de pedidos en Configuración de pedidos para administrar más fácilmente los pedidos de Amazon de su administrador de comercio.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Administrar pedidos

Puede ver la información de pedidos de Amazon, tal como se recibió de Amazon, en la _[!UICONTROL Recent Orders]_de la sección [tablero de tienda](./amazon-store-dashboard.md) o en el_[!UICONTROL Amazon orders]_ (también denominada _[!UICONTROL All Orders]_vista).

La forma de administrar los pedidos de Amazon depende de si la importación de pedidos está habilitada o deshabilitada en su [Configuración de pedidos](./order-settings.md#configure-order-settings).

## Con la importación de pedidos habilitada

Después [integración de tienda](./store-integration.md), el [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) la configuración es `Enabled` de forma predeterminada. Con esta configuración, las [!DNL Commerce] los pedidos se crean para los pedidos de Amazon y se pueden administrar en [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} flujo de trabajo.

>[!NOTE]
>
>Independientemente de la configuración de importación de pedidos, los pedidos de Amazon que existían en su [!DNL Amazon Seller Central] cuenta antes de su [integración de tienda](./store-integration.md) no se importan.

Los pedidos de Amazon importados se administran en [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} workflow, just like your other [!DNL Commerce] stores. Click the Amazon order number in the *[!UICONTROL Order Number]* column to open the order in the [[!DNL Commerce] order process](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target="_blank"}. Consulte [Ver pedidos de Amazon](./amazon-orders-all.md).

### Proceso de importación de pedidos

Cuando se realiza un pedido en Amazon y [importación de pedidos](./order-settings.md) está activada, comienza el siguiente proceso.

| Cambiar | Acciones |
|---|---|
| Se realiza un pedido en Amazon. | <ul><li>Amazon establece el estado del pedido en `Pending`.</li><li>La información del pedido se envía a [!DNL Commerce].</li><li>El pedido se ha añadido a [_Pedidos de Amazon_ tabla](./amazon-orders-all.md) con un `Pending` estado.</li></ul> |
| Amazon cambia el estado del pedido a `Unshipped`. | <ul><li>El cambio de estado se envía a [!DNL Commerce].</li><li>En el [_Pedidos de Amazon_ tabla](./amazon-orders-all.md), el estado del pedido cambia a `Unshipped`.</li><li>En el [[!DNL Commerce] flujo de trabajo pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}, un correspondiente [!DNL Commerce] El pedido se crea con una `Processing` estado.</li></ul> |
| Entrada [[!DNL Commerce] flujo de trabajo pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}, el [!DNL Commerce] el pedido se procesa y el estado cambia a `Shipped`. | <ul><li>En el [_Pedidos de Amazon_ tabla](./amazon-orders-all.md), el estado del pedido cambia a `Shipped`.</li><li>En el siguiente trabajo cron, el estado del pedido cambia a `Complete` en el [[!DNL Commerce] flujo de trabajo pedidos](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.</li></ul> |

### Bloqueadores de creación de pedidos

Hay algunos escenarios que impiden la creación de los correspondientes [!DNL Commerce] pedido. [!DNL Commerce] los pedidos no se crean para pedidos que se reciben cuando se produce cualquiera de los siguientes problemas.

| Escenario | Solución |
|---|---|
| El elemento no existe en [!DNL Commerce] catálogo. | [Crear el producto](./creating-assigning-catalog-products.md) en su [!DNL Commerce] catálogo y [coincidencia manual](./creating-assigning-catalog-products.md) se envía al producto. |
| El elemento del catálogo está desactivado. | Asegúrese de que la variable [estado del producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} está activada. |
| El artículo pedido está agotado. | Actualizar o configurar el [opciones de producto](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} para cantidad y origen. |

Cuando no se pueden importar pedidos, aparece un mensaje del sistema similar al siguiente en la parte superior de la pantalla:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Cuando se resuelva el problema, la variable [!DNL Commerce] el pedido se crea en la siguiente sincronización.

## Con la importación de pedidos deshabilitada

Si no desea importar y administrar sus pedidos de Amazon en [!DNL Commerce], puede cambiar el [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) configurando en `Disabled`. Esta configuración significa que, cuando se reciben nuevos pedidos desde Amazon, los [!DNL Commerce] no se crean pedidos.

Cuando está desactivada, la información de pedidos recibida de Amazon aparece en la _[!UICONTROL Recent Orders]_del panel de tienda y en la sección_[!UICONTROL All Orders]_ vista. Esta información de pedido es de solo lectura y debe administrar estos pedidos en [!DNL Amazon Seller Central]. Para abrir los detalles del pedido en [!DNL Amazon Seller Central], haga clic en el número de pedido de Amazon en la _[!UICONTROL Order Number]_columna.

Consulte también [Ver pedidos de Amazon](./amazon-orders-all.md), [Ver detalles del pedido de Amazon](./amazon-order-details.md), y [Tareas de procesamiento de orden común](./common-order-processing.md).
