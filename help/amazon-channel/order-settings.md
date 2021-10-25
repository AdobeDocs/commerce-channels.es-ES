---
title: Configuración de pedidos
description: Utilice la configuración de pedidos para determinar cómo se importan y procesan los pedidos de Amazon en la tienda de comercio.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Configuración de pedidos

La configuración de pedidos define si los pedidos de Amazon se importan a y se procesan en [!DNL Commerce] y se puede acceder a en el [tablero de almacenamiento](./amazon-store-dashboard.md).

La configuración de importación del pedido se establece en `Enabled` de forma predeterminada, lo que significa que sus pedidos de Amazon aparecen en el panel de la tienda y crean los correspondientes [!DNL Commerce] pedidos. Los pedidos importados se pueden administrar en la variable [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} flujo de trabajo.

>[!NOTE]
>
>Independientemente de la configuración del pedido, los pedidos de Amazon que existían antes de la integración de la tienda no se importan.

Después [integración de tiendas](./store-integration.md) se ha completado, puede cambiar la configuración del pedido. Si establece la configuración de pedido en `Disabled`, los pedidos de Amazon se muestran en el panel de la tienda, pero deben administrarse en su [!DNL Amazon Seller Central] cuenta.

Cuando se crea un pedido en Amazon, no se importa inmediatamente en [!DNL Commerce]. Amazon asigna un `Pending` a pedidos recién creados. Después de que Amazon verifique el pedido y el método de pago, el estado del pedido se cambia a `Unshipped`. Este cambio de estado déclencheur la importación de pedidos y [!DNL Commerce] crea un pedido correspondiente y coincidente.

Los pedidos importados de Amazon se pueden administrar en la [!DNL Commerce] [flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}. Consulte también [Administrar pedidos](./managing-orders.md).

## Configuración de los ajustes de orden {#configure-order-settings}

1. Haga clic en **[!UICONTROL Order Settings]** en el panel de la tienda.

1. Para **[!UICONTROL Import Amazon Orders]** (obligatorio), elija una opción:

   - `Disabled` - Elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciben nuevos pedidos de Amazon. Cuando se elige, todos los demás campos de esta página se desactivan.

   - `Enabled` - (Predeterminado) Elija cuándo desea crear la [!DNL Commerce] pedidos cuando se reciben nuevos pedidos de Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y los niveles de stock.

      >[!NOTE]
      >
      >Importar pedidos de Amazon debe estar establecido en `Enabled` para administrar los pedidos de Amazon en la variable [!DNL Commerce] [pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} flujo de trabajo. Cuando se configura como `Disabled`, sus pedidos de Amazon no tienen un [!DNL Commerce] número de pedido y no se pueden administrar en [!DNL Commerce]. Administra estos pedidos en su [!DNL Amazon Seller Central] cuenta.

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, elija cuál [!DNL Commerce] almacenar los pedidos de Amazon con los que están asociados cuando se crea el pedido correspondiente en [!DNL Commerce].

   Este valor predeterminado es la vista de tienda del sitio web seleccionado al [se ha añadido la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de la variable [!DNL Commerce] tiendas que ha configurado en su configuración. Consulte [Almacenes](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Customer Creation]**, elija una opción:

   - `No Customer Creation (guest)` - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados del pedido de Amazon. Cuando se elige, [!DNL Commerce] procesa un pedido de Amazon importado del mismo modo que procesa un cierre de compra de un invitado [!DNL Commerce].

   - `Build New Customer Account` - Elija cuándo desea crear una nueva cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes a partir de los pedidos de Amazon.

1. Para **[!UICONTROL Order Number Source]**, elija una opción:

   - `Build Using Magento Order Number` - (Predeterminado) Elija cuándo desea crear un [!DNL Commerce] número de pedido del pedido de Amazon correspondiente utilizando la variable [!DNL Commerce] ID de pedido asignado de forma incremental.

   - `Build Using Amazon Order Number` - Elija cuándo desea crear la variable [!DNL Commerce] número de pedido con el número de pedido asignado por Amazon correspondiente.
   >[!NOTE]
   >
   >Después de importar un pedido, el número de pedido de Amazon se muestra en la variable _[!UICONTROL Recent Orders]_en el panel de almacenamiento. La variable [!DNL Commerce] el número de pedido se muestra al ver los detalles del pedido en la [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Espacio de trabajo de {target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Order Status]** (obligatorio), elija una opción:

   - `Default Order Status` - (Predeterminado) Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne el estado de pedido predeterminado definido para los nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para los nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

   - `Custom Order Status` - Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne un estado distinto al predeterminado.

   - `Processing Order Status` - Habilitado cuando **[!UICONTROL Order Status]** está configurado como `Custom Order Status`. Elija el estado que desea utilizar para los pedidos recién creados importados de Amazon. Las opciones de este campo se basan en las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://docs.magento.com/user-guide/sales/order-status.html). También puede crear un estado de pedido personalizado para mostrarlo aquí para su selección. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}.

1. Cuando termine, haga clic en **[!UICONTROL Save order settings]**.

![Configuración de pedidos](assets/amazon-order-settings.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Import Amazon Orders] | Opciones:<ul><li>**[!UICONTROL Disabled]** - Elija cuándo no desea crear los pedidos correspondientes en [!DNL Commerce] cuando se reciben nuevos pedidos de Amazon. Cuando se elige, todos los demás campos de esta página se desactivan.</li><li>**[!UICONTROL Enabled]** - (Predeterminado) Elija cuándo desea crear la [!DNL Commerce] pedidos cuando se reciben nuevos pedidos de Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y los niveles de stock.</li></ul><br><br>`Enabled` debe elegirse para administrar los pedidos de Amazon en [!DNL Commerce]. When `Disabled` se elige, los pedidos de Amazon se muestran en el panel de la tienda, pero los pedidos deben administrarse en su [!DNL Amazon Seller Central] cuenta. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Elija cuál [!DNL Commerce] almacene los pedidos de Amazon a los que están asociados cuando se crean en la variable [!DNL Commerce] [Pedidos](https://docs.magento.com/user-guide/sales/orders.html)Espacio de trabajo de {target=&quot;_blank&quot;}. De forma predeterminada, esta configuración se establece en la vista de tienda para la variable [!DNL Commerce] sitio web seleccionado al [se ha añadido la tienda Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de la variable [!DNL Commerce] tiendas que ha configurado en su configuración. Consulte [Almacenes](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Opciones:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente en [!DNL Commerce] uso de los datos de cliente importados del pedido de Amazon. Cuando se elige, esta opción indica [!DNL Commerce] para procesar un pedido de Amazon importado del mismo modo que procesa un cierre de compra de invitado.</li><li>**[!UICONTROL Build New Customer Account]** - Elija cuándo desea crear una nueva cuenta de cliente en su [!DNL Commerce] base de datos de clientes utilizando los datos de clientes importados con el pedido de Amazon. Esta opción le ayuda a crear su [!DNL Commerce] base de datos de clientes de sus pedidos de Amazon.</li></ul> |
| Origen de número de pedido | Opciones:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Predeterminado) Elija cuándo desea crear un [!DNL Commerce] número de pedido del pedido de Amazon correspondiente utilizando la variable [!DNL Commerce] ID de pedido asignado de forma incremental. </li><li>**Generar con número de orden de Amazon** - Elija cuándo desea crear la variable [!DNL Commerce] número de pedido con el número de pedido asignado por Amazon correspondiente.</li></ul> |
| Pedidos pendientes | Opciones:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Elija cuándo no desea que su [!DNL Commerce] cantidad de stock afectada por los pedidos de Amazon. Elija si utiliza Amazon para su proceso de cumplimiento (FBA). Cuando se selecciona y recibe un pedido de Amazon, la cantidad solicitada no afecta a su [!DNL Commerce] cantidad de stock.</li><li>**[!UICONTROL Reserve Quantity]** - Elija cuándo desea que la cantidad de pedido del pedido de Amazon se &quot;reserve&quot; en su [!DNL Commerce] cantidad de stock. Cuando se elija y reciba un pedido de Amazon, la cantidad solicitada se &quot;reservará&quot; en su [!DNL Commerce] cantidad de stock para evitar que [!DNL Commerce] acciones de &quot;sobreventa&quot;. La cantidad &quot;reservada&quot; no está disponible para su compra a través de su [!DNL Commerce] tienda.</li></ul> |
| [!UICONTROL Order Status] | Opciones:<ul><li>**[!UICONTROL Default Order Status]** - (Predeterminado) Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne el estado de pedido predeterminado para nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para los nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne un estado distinto al predeterminado. Cuando se elige, **[!UICONTROL Processing Order Status]** permite elegir el estado que desea utilizar para los pedidos recién creados importados de Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Habilitado cuando _[!UICONTROL Order Status]_está configurado como `Custom Order Status`. Elija el estado de pedido que desea asignar a los nuevos pedidos. Las opciones de este campo dependen de las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://docs.magento.com/user-guide/sales/order-status.html){target=&quot;_blank&quot;}. También puede crear un estado de pedido personalizado para mostrarlo aquí. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}. |

## [!DNL Commerce] creación de pedidos

[!DNL Commerce] los pedidos se crean para los pedidos de Amazon en función del estado y las condiciones de inventario siguientes.

### Creación de Pedidos con Administración de Inventario

>[!NOTE]
>
>Solo se admite en integraciones de Adobe Commerce y Magento Open Source 2.3.x.

| Canal de cumplimiento | [!DNL Commerce] Estado de inventario | Estado del pedido de Amazon | [!UICONTROL Create Magento Order] Configuración | Inventario reservado |
|---|---|---|---|---|
| FBA | En existencias<br>Fuera de existencias<br>No administrar | Pendiente | No | No |
| FBA | En existencias<br>Fuera de existencias<br>No administrar | PendingAvailability | No | No |
| FBA | En existencias<br>Fuera de existencias<br>No administrar | Cancelado | No | No |
| FBA | En existencias<br>Fuera de existencias<br>No administrar | Error | No | No |
| FBA | En existencias<br>Fuera de existencias<br>No administrar | Sin enviar | No | No |
| FBA | En existencias<br>Fuera de existencias<br>No administrar | Parcialmente enviado | No | No |
| FBA | En existencias<br>No administrar | Enviado | Sí | No |
| FBA | Fuera de existencias | Enviado | No | No |
| FBM | En existencias<br>Fuera de existencias<br>No administrar | Pendiente | No | No |
| FBM | En existencias<br>Fuera de existencias<br>No administrar | PendingAvailability | No | No |
| FBM | En existencias<br>Fuera de existencias<br>No administrar | Cancelado | No | No |
| FBM | En existencias<br>Fuera de existencias<br>No administrar | Error | No | No |
| FBM | En existencias<br>No administrar | Sin enviar | Sí | Sí |
| FBM | Fuera de existencias | Sin enviar | No | No |
| FBM | En existencias<br>No administrar | Parcialmente enviado | Sí | Sí |
| FBM | Fuera de existencias | Parcialmente enviado | No | No |
| FBM | En existencias<br>No administrar | Enviado | Sí | Sí |
| FBM | Fuera de existencias | Enviado | No | No |

>[!NOTE]
>Si se importa un pedido de Amazon en un `Partially Shipped` o `Shipped` , la reserva de inventario que se crea es para todos los artículos del pedido. El canal de ventas de Amazon no compensa los artículos que se han enviado anteriormente.
>
>Si Amazon (FBA) cumple un pedido pero hay un artículo en `out of stock` estado, [!DNL Commerce] no puede crear un pedido correspondiente. Esta es una limitación de las integraciones de Administración de inventario.
