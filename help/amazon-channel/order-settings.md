---
title: Configuración de pedidos de Amazon
description: Utilice la configuración de Pedidos para determinar cómo se importan y procesan los pedidos de Amazon en su tienda de Commerce.
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Configuración de pedidos de Amazon

La configuración de pedidos define si y cómo se importan y procesan los pedidos de Amazon en [!DNL Commerce] y se puede acceder a en la [tablero de tienda](./amazon-store-dashboard.md).

La configuración de importación de pedidos está establecida en `Enabled` de forma predeterminada, lo que significa que los pedidos de Amazon aparecen en el panel de la tienda y crean los correspondientes [!DNL Commerce] pedidos. Los pedidos importados se pueden administrar en [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) flujo de trabajo.

>[!NOTE]
>
>Independientemente de la configuración de pedidos, los pedidos de Amazon que existían antes de la integración con la tienda no se importan.

Después [integración de tienda](./store-integration.md) se ha completado, puede cambiar la configuración del pedido. Si establece la configuración del pedido en `Disabled`, los pedidos de Amazon se muestran en el panel de la tienda, pero deben administrarse en su [!DNL Amazon Seller Central] cuenta.

Cuando se crea un pedido en Amazon, no se importa inmediatamente a [!DNL Commerce]. Amazon asigna un `Pending` estado de los pedidos recién creados. Una vez que Amazon verifica el pedido y la forma de pago, el estado del pedido cambia a `Unshipped`. Este cambio de estado déclencheur la importación del pedido y [!DNL Commerce] crea un orden correspondiente.

Los pedidos importados de Amazon se pueden administrar en [!DNL Commerce] [flujo de trabajo pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Consulte también [Administrar pedidos](./managing-orders.md).

## Configuración de pedidos {#configure-order-settings}

1. Clic **[!UICONTROL Order Settings]** en el tablero de la tienda.

1. Para **[!UICONTROL Import Amazon Orders]** (obligatorio), elija una opción:

   - `Disabled` - Elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciben nuevos pedidos desde Amazon. Si se selecciona, el resto de campos de esta página se desactivan.

   - `Enabled` - (Predeterminado) Elija cuándo desea crear los elementos correspondientes [!DNL Commerce] pedidos cuando se reciben nuevos pedidos desde Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y de los niveles de stock.

     >[!NOTE]
     >
     >Importar pedidos de Amazon debe estar establecido en `Enabled` para administrar pedidos de Amazon en [!DNL Commerce] [pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) flujo de trabajo. Cuando se establece en `Disabled`, sus pedidos de Amazon no tienen un correspondiente [!DNL Commerce] número de pedido y no se pueden administrar en [!DNL Commerce]. Estos pedidos se gestionan en su [!DNL Amazon Seller Central] cuenta.

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, elija cuál [!DNL Commerce] almacenar los pedidos de Amazon asociados a cuando se crea el pedido correspondiente en [!DNL Commerce].

   Esta configuración toma como valor predeterminado la Vista de tienda del sitio web seleccionado cuando [agregó la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de la variable [!DNL Commerce] tiendas que haya configurado en su configuración. Consulte [Tiendas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Para **[!UICONTROL Customer Creation]**, elija una opción:

   - `No Customer Creation (guest)` - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados del pedido de Amazon. Cuando se elige, [!DNL Commerce] procesa un pedido de Amazon importado del mismo modo que procesa un cierre de compra de invitado en [!DNL Commerce].

   - `Build New Customer Account` - Elija cuándo desea crear una nueva cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes a partir de los pedidos de Amazon.

1. Para **[!UICONTROL Order Number Source]**, elija una opción:

   - `Build Using Magento Order Number` - (Predeterminado) Elija cuándo desea crear una variable única [!DNL Commerce] número de pedido para el pedido de Amazon correspondiente utilizando [!DNL Commerce] ID de pedido asignado de forma incremental.

   - `Build Using Amazon Order Number` : elija cuándo desea crear la variable [!DNL Commerce] número de pedido utilizando el número de pedido asignado por Amazon correspondiente.

   >[!NOTE]
   >
   >Después de importar un pedido, el número de pedido de Amazon se muestra en la _[!UICONTROL Recent Orders]_en el panel de la tienda. El [!DNL Commerce] El número de pedido se muestra al ver los detalles del pedido en la [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) workspace.

1. Para **[!UICONTROL Order Status]** (obligatorio), elija una opción:

   - `Default Order Status` - (Predeterminado) Seleccione cuándo desea que los pedidos recién creados importados de Amazon se asignen al estado de pedido predeterminado definido para los nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` : elija cuándo desea que los pedidos recién creados importados de Amazon se asignen a un estado distinto del predeterminado.

   - `Processing Order Status` - Habilitado cuando **[!UICONTROL Order Status]** se establece en `Custom Order Status`. Elija el estado que desea utilizar para los pedidos recién creados importados de Amazon. Las opciones de este campo se basan en las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). También puede crear un estado de pedido personalizado para mostrarlo aquí para su selección. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Cuando termine, haga clic en **[!UICONTROL Save order settings]**.

![Configuración de pedidos](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Campo | Descripción |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | Opciones:<ul><li>**[!UICONTROL Disabled]** - Elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciben nuevos pedidos desde Amazon. Si se selecciona, el resto de campos de esta página se desactivan.</li><li>**[!UICONTROL Enabled]** - (Predeterminado) Elija cuándo desea crear los elementos correspondientes [!DNL Commerce] pedidos cuando se reciben nuevos pedidos desde Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y de los niveles de stock.</li></ul><br><br>`Enabled` debe elegirse para administrar los pedidos de Amazon en [!DNL Commerce]. Cuándo `Disabled` se selecciona, los pedidos de Amazon se muestran en el panel de la tienda, pero los pedidos deben administrarse en su [!DNL Amazon Seller Central] cuenta. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Elegir qué [!DNL Commerce] almacenar los pedidos de Amazon asociados a cuando se crean en la variable [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) workspace. Esta configuración toma como valor predeterminado la Vista de tienda para [!DNL Commerce] sitio web seleccionado al [agregó la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de la variable [!DNL Commerce] tiendas que haya configurado en su configuración. Consulte [Tiendas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Opciones:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados del pedido de Amazon. Cuando se elige, esta opción indica [!DNL Commerce] para procesar un pedido de Amazon importado del mismo modo que se procesa un cierre de compra de invitado.</li><li>**[!UICONTROL Build New Customer Account]** - Elija cuándo desea crear una nueva cuenta de cliente en su [!DNL Commerce] base de datos de clientes que utiliza los datos de clientes importados con el pedido de Amazon. Esta opción le ayuda a crear su [!DNL Commerce] base de datos de clientes de sus pedidos de Amazon.</li></ul> |
| Origen de número de pedido | Opciones:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Predeterminado) Elija cuándo desea crear una variable única [!DNL Commerce] número de pedido para el pedido de Amazon correspondiente utilizando [!DNL Commerce] ID de pedido asignado de forma incremental. </li><li>**Número de pedido de compilación mediante Amazon** : elija cuándo desea crear la variable [!DNL Commerce] número de pedido utilizando el número de pedido asignado por Amazon correspondiente.</li></ul> |
| Pedidos pendientes | Opciones:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Elige cuando no quieras tu [!DNL Commerce] cantidad de stock afectada por sus pedidos de Amazon. Elija si utiliza Amazon para el proceso de cumplimiento (FBA). Cuando se selecciona y recibe un pedido de Amazon, la cantidad solicitada no afecta a su [!DNL Commerce] cantidad de stock.</li><li>**[!UICONTROL Reserve Quantity]** - Elija cuándo desea que la cantidad del pedido de Amazon se &quot;reserve&quot; en su [!DNL Commerce] cantidad de stock. Cuando se selecciona y recibe un pedido de Amazon, la cantidad solicitada se &quot;reserva&quot; en su [!DNL Commerce] cantidad de existencias para evitar [!DNL Commerce] acciones de &quot;venta excesiva&quot;. La cantidad &quot;reservada&quot; no se puede comprar a través de su [!DNL Commerce] tienda.</li></ul> |
| [!UICONTROL Order Status] | Opciones:<ul><li>**[!UICONTROL Default Order Status]** - (Predeterminado) Seleccione cuándo desea que los pedidos recién creados importados de Amazon se asignen a su estado de pedido predeterminado para nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** : elija cuándo desea que los pedidos recién creados importados de Amazon se asignen a un estado distinto del predeterminado. Cuando se elige, **[!UICONTROL Processing Order Status]** permite elegir el estado que desea utilizar para los pedidos recién creados importados desde Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Habilitado cuando _[!UICONTROL Order Status]_se establece en `Custom Order Status`. Seleccione el estado del pedido que desea asignar a los nuevos pedidos. Las opciones de este campo dependen de las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). También puede crear un estado de pedido personalizado para mostrar aquí. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado] |

## [!DNL Commerce] creación de pedidos

[!DNL Commerce] los pedidos se crean para pedidos Amazon en función del siguiente estado y las condiciones de inventario.

### Creación de pedidos con Inventory management

>[!NOTE]
>
>Compatible solo con integraciones de Adobe Commerce y Magento Open Source 2.3.x.

| Canal de cumplimiento | [!DNL Commerce] Estado de inventario | Estado de pedidos de Amazon | [!UICONTROL Create Magento Order] Configuración | Inventario reservado |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | En existencia<br>Agotado<br>No administrar | Pendiente | No | No |
| FBA | En existencia<br>Agotado<br>No administrar | PendingAvailability | No | No |
| FBA | En existencia<br>Agotado<br>No administrar | Cancelado | No | No |
| FBA | En existencia<br>Agotado<br>No administrar | Error | No | No |
| FBA | En existencia<br>Agotado<br>No administrar | No enviado | No | No |
| FBA | En existencia<br>Agotado<br>No administrar | Parcialmente enviado | No | No |
| FBA | En existencia<br>No administrar | Enviado | Sí | No |
| FBA | Agotado | Enviado | No | No |
| FBM | En existencia<br>Agotado<br>No administrar | Pendiente | No | No |
| FBM | En existencia<br>Agotado<br>No administrar | PendingAvailability | No | No |
| FBM | En existencia<br>Agotado<br>No administrar | Cancelado | No | No |
| FBM | En existencia<br>Agotado<br>No administrar | Error | No | No |
| FBM | En existencia<br>No administrar | No enviado | Sí | Sí |
| FBM | Agotado | No enviado | No | No |
| FBM | En existencia<br>No administrar | Parcialmente enviado | Sí | Sí |
| FBM | Agotado | Parcialmente enviado | No | No |
| FBM | En existencia<br>No administrar | Enviado | Sí | Sí |
| FBM | Agotado | Enviado | No | No |

>[!NOTE]
>Si un pedido de Amazon se importa en un `Partially Shipped` o `Shipped` estado, la reserva de inventario que se crea es para todos los artículos del pedido. El canal de ventas de Amazon no compensa los artículos que se han enviado anteriormente.
>
>Si un pedido es Satisfecho por Amazon (FBA) pero un artículo está en `out of stock` estado, [!DNL Commerce] no puede crear un pedido correspondiente. Esto es una limitación de las integraciones de Inventory management.
