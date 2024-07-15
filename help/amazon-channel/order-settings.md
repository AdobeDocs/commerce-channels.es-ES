---
title: Configuración de pedidos de Amazon
description: Utilice la configuración de Pedidos para determinar cómo se importan y procesan los pedidos de Amazon en su tienda de Commerce.
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Configuración de pedidos de Amazon

La configuración de pedidos define si los pedidos de Amazon se importan y procesan en [!DNL Commerce] y cómo se puede tener acceso a ellos en el [tablero de la tienda](./amazon-store-dashboard.md).

La configuración de importación de pedidos está establecida en `Enabled` de forma predeterminada, lo que significa que los pedidos de Amazon aparecerán en el panel de almacenamiento y crearán los [!DNL Commerce] pedidos correspondientes. Los pedidos importados se pueden administrar en el flujo de trabajo [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Independientemente de la configuración de pedidos, los pedidos de Amazon que existían antes de la integración con la tienda no se importan.

Una vez completada la [integración de la tienda](./store-integration.md), puede cambiar la configuración de su pedido. Si establece la configuración de pedidos en `Disabled`, los pedidos de Amazon se mostrarán en el panel de la tienda, pero deberán administrarse en su cuenta de [!DNL Amazon Seller Central].

Cuando se crea un pedido en Amazon, no se importa inmediatamente a [!DNL Commerce]. Amazon asigna un estado `Pending` a los pedidos recién creados. Una vez que Amazon verifica el pedido y el método de pago, el estado del pedido cambia a `Unshipped`. Este cambio de estado déclencheur la importación de pedidos y [!DNL Commerce] crea un pedido correspondiente y coincidente.

Los pedidos importados de Amazon se pueden administrar en el [!DNL Commerce] [flujo de trabajo de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Consulte también [Administrar pedidos](./managing-orders.md).

## Configuración de pedidos {#configure-order-settings}

1. Haga clic en **[!UICONTROL Order Settings]** en el tablero del almacén.

1. Para **[!UICONTROL Import Amazon Orders]** (obligatorio), elija una opción:

   - `Disabled`: elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciban nuevos pedidos de Amazon. Si se selecciona, el resto de campos de esta página se desactivan.

   - `Enabled` - (Predeterminado) Elija cuándo desea crear los [!DNL Commerce] pedidos correspondientes cuando se reciban nuevos pedidos desde Amazon. [!DNL Commerce] pedidos se crean según el estado de Amazon y los niveles de stock.

     >[!NOTE]
     >
     >Importar pedidos Amazon debe establecerse en `Enabled` para administrar los pedidos Amazon en el flujo de trabajo [!DNL Commerce] [pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Cuando se establece en `Disabled`, los pedidos de Amazon no tienen un número de pedido [!DNL Commerce] correspondiente y no se pueden administrar en [!DNL Commerce]. Usted administra estos pedidos en su cuenta de [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, elija a qué [!DNL Commerce] almacenar los pedidos de Amazon están asociados cuando se crea el pedido correspondiente en [!DNL Commerce].

   Esta configuración toma como valor predeterminado la Vista de tienda del sitio web seleccionado cuando [agregó la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de los almacenes de [!DNL Commerce] que haya configurado en la configuración. Ver [Tiendas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Para **[!UICONTROL Customer Creation]**, elija una opción:

   - `No Customer Creation (guest)` - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] con los datos de cliente importados del pedido de Amazon. Cuando se elige, [!DNL Commerce] procesa un pedido de Amazon importado del mismo modo que procesa un cierre de compra de invitado en [!DNL Commerce].

   - `Build New Customer Account`: elija cuándo desea crear una nueva cuenta de cliente en [!DNL Commerce] mediante los datos de cliente importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes a partir de los pedidos de Amazon.

1. Para **[!UICONTROL Order Number Source]**, elija una opción:

   - `Build Using Magento Order Number` - (Predeterminado) Elija cuándo desea crear un número de pedido [!DNL Commerce] único para el pedido de Amazon correspondiente mediante el ID de pedido asignado de forma incremental [!DNL Commerce].

   - `Build Using Amazon Order Number`: elija cuándo desea crear el número de pedido [!DNL Commerce] mediante el número de pedido asignado por Amazon correspondiente.

   >[!NOTE]
   >
   >Después de importar un pedido, el número de pedido de Amazon se muestra en la lista _[!UICONTROL Recent Orders]_del panel de almacén. El número de pedido [!DNL Commerce] se muestra al ver los detalles del pedido en el área de trabajo [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

1. Para **[!UICONTROL Order Status]** (obligatorio), elija una opción:

   - `Default Order Status` - (Predeterminado) Elija cuándo desea que los pedidos recién creados importados de Amazon se asignen al estado de pedido predeterminado definido para los nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para nuevos pedidos) es `Pending`. Consulte [Órdenes de procesamiento](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status`: elija cuándo desea que los pedidos recién creados importados de Amazon se asignen a un estado distinto del predeterminado.

   - `Processing Order Status` - Habilitado cuando **[!UICONTROL Order Status]** está establecido en `Custom Order Status`. Elija el estado que desea utilizar para los pedidos recién creados importados de Amazon. Las opciones de este campo se basan en las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). También puede crear un estado de pedido personalizado para mostrarlo aquí para su selección. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Una vez finalizado, haga clic en **[!UICONTROL Save order settings]**.

![Configuración de pedidos](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Campo | Descripción |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | Opciones:<ul><li>**[!UICONTROL Disabled]**: elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciban nuevos pedidos de Amazon. Si se selecciona, el resto de campos de esta página se desactivan.</li><li>**[!UICONTROL Enabled]** - (Predeterminado) Elija cuándo desea crear los [!DNL Commerce] pedidos correspondientes cuando se reciban nuevos pedidos desde Amazon. [!DNL Commerce] pedidos se crean según el estado de Amazon y los niveles de stock.</li></ul><br><br>`Enabled` debe elegirse para administrar los pedidos de Amazon en [!DNL Commerce]. Cuando se elige `Disabled`, los pedidos de Amazon se muestran en el panel de la tienda, pero los pedidos deben administrarse en su cuenta de [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Elija con qué almacén de [!DNL Commerce] se asocian los pedidos de Amazon cuando se crean en el área de trabajo de [!DNL Commerce] [Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Esta configuración toma como valor predeterminado la Vista de tienda del sitio web [!DNL Commerce] seleccionado cuando [agregó la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de los almacenes de [!DNL Commerce] que haya configurado en la configuración. Ver [Tiendas](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Opciones:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] con los datos de cliente importados del pedido de Amazon. Cuando se elige, esta opción indica a [!DNL Commerce] que procese un pedido de Amazon importado del mismo modo que procesa un cierre de compra de invitado.</li><li>**[!UICONTROL Build New Customer Account]**: elija cuándo desea crear una nueva cuenta de cliente en la base de datos de clientes de [!DNL Commerce] mediante los datos de clientes importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes de [!DNL Commerce] a partir de los pedidos de Amazon.</li></ul> |
| Número de pedido Source | Opciones:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Predeterminado) Elija cuándo desea crear un número de pedido [!DNL Commerce] único para el pedido de Amazon correspondiente mediante el ID de pedido asignado de forma incremental [!DNL Commerce]. </li><li>**Generar con el número de pedido de Amazon**: elija cuándo desea crear el número de pedido [!DNL Commerce] con el número de pedido asignado de Amazon correspondiente.</li></ul> |
| Pedidos pendientes | Opciones:<ul><li>**[!UICONTROL Do Not Reserve Quantity]**: elija cuándo no desea que la cantidad de existencias [!DNL Commerce] se vea afectada por los pedidos de Amazon. Elija si utiliza Amazon para el proceso de cumplimiento (FBA). Cuando se selecciona y recibe un pedido de Amazon, la cantidad solicitada no afecta a la cantidad de existencias de [!DNL Commerce].</li><li>**[!UICONTROL Reserve Quantity]**: elija cuándo desea que la cantidad del pedido de Amazon se &quot;reserve&quot; en la cantidad de existencias de [!DNL Commerce]. Cuando se selecciona y recibe un pedido de Amazon, la cantidad pedida se &quot;reservará&quot; en la cantidad de existencias [!DNL Commerce] para evitar que las existencias de [!DNL Commerce] se &quot;vendan en exceso&quot;. La cantidad &quot;reservada&quot; no está disponible para la compra a través de la tienda [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Opciones:<ul><li>**[!UICONTROL Default Order Status]** - (Predeterminado) Elija cuándo desea que los pedidos recién creados importados de Amazon se asignen a su estado de pedido predeterminado para nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para nuevos pedidos) es `Pending`. Consulte [Órdenes de procesamiento](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]**: elija cuándo desea que los pedidos recién creados importados de Amazon se asignen a un estado distinto del predeterminado. Si se elige, **[!UICONTROL Processing Order Status]** le permite elegir el estado que desea utilizar para los pedidos recién creados importados de Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Se habilitó cuando _[!UICONTROL Order Status]_está establecido en `Custom Order Status`. Seleccione el estado del pedido que desea asignar a los nuevos pedidos. Las opciones de este campo dependen de las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). También puede crear un estado de pedido personalizado para mostrar aquí. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado] |

## [!DNL Commerce] creación de pedido

[!DNL Commerce] pedidos se han creado para pedidos Amazon en función del estado y las condiciones de inventario siguientes.

### Creación de pedidos con Inventory management

>[!NOTE]
>
>Compatible solo con integraciones de Adobe Commerce y Magento Open Source 2.3.x.

| Canal de cumplimiento | [!DNL Commerce] estado de inventario | Estado de pedidos de Amazon | Configuración de [!UICONTROL Create Magento Order] | Inventario reservado |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | En existencias<br>Agotado<br>No administrar | Pendiente | No | No |
| FBA | En existencias<br>Agotado<br>No administrar | PendingAvailability | No | No |
| FBA | En existencias<br>Agotado<br>No administrar | Cancelado | No | No |
| FBA | En existencias<br>Agotado<br>No administrar | Error | No | No |
| FBA | En existencias<br>Agotado<br>No administrar | No enviado | No | No |
| FBA | En existencias<br>Agotado<br>No administrar | Parcialmente enviado | No | No |
| FBA | En existencias<br>No administrar | Enviado | Sí | No |
| FBA | Agotado | Enviado | No | No |
| FBM | En existencias<br>Agotado<br>No administrar | Pendiente | No | No |
| FBM | En existencias<br>Agotado<br>No administrar | PendingAvailability | No | No |
| FBM | En existencias<br>Agotado<br>No administrar | Cancelado | No | No |
| FBM | En existencias<br>Agotado<br>No administrar | Error | No | No |
| FBM | En existencias<br>No administrar | No enviado | Sí | Sí |
| FBM | Agotado | No enviado | No | No |
| FBM | En existencias<br>No administrar | Parcialmente enviado | Sí | Sí |
| FBM | Agotado | Parcialmente enviado | No | No |
| FBM | En existencias<br>No administrar | Enviado | Sí | Sí |
| FBM | Agotado | Enviado | No | No |

>[!NOTE]
>Si se importa un pedido de Amazon en un estado `Partially Shipped` o `Shipped`, la reserva de inventario que se crea es para todos los artículos del pedido. El canal de ventas de Amazon no compensa los artículos que se han enviado anteriormente.
>
>Si un pedido es Satisfecho por Amazon (FBA) pero un elemento está en estado `out of stock`, [!DNL Commerce] no puede crear un pedido correspondiente. Esto es una limitación de las integraciones de Inventory management.
