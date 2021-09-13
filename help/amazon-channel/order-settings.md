---
title: Configuración de pedidos
description: Utilice la configuración de pedidos para determinar cómo se importan y procesan los pedidos de Amazon en la tienda de comercio.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Configuración de pedidos

La configuración de pedidos define si los pedidos de Amazon se importan y procesan en [!DNL Commerce] y cómo se puede acceder a ellos en el [panel de almacenamiento](./amazon-store-dashboard.md).

La configuración de importación de pedidos se establece en `Enabled` de forma predeterminada, lo que significa que los pedidos de Amazon aparecen en el panel de almacenamiento y crean los [!DNL Commerce] pedidos correspondientes. Los pedidos importados se pueden administrar en el flujo de trabajo [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Independientemente de la configuración del pedido, los pedidos de Amazon que existían antes de la integración de la tienda no se importan.

Una vez finalizada la [integración del almacén](./store-integration.md), puede cambiar la configuración del pedido. Si establece la configuración de su pedido en `Disabled`, los pedidos de Amazon se muestran en el panel de la tienda, pero deben administrarse en su cuenta [!DNL Amazon Seller Central].

Cuando se crea un pedido en Amazon, no se importa inmediatamente en [!DNL Commerce]. Amazon asigna un estado `Pending` a los pedidos recién creados. Después de que Amazon verifique el pedido y el método de pago, el estado del pedido cambia a `Unshipped`. Este cambio de estado déclencheur la importación de pedidos y [!DNL Commerce] crea un pedido correspondiente coincidente.

Los pedidos importados de Amazon se pueden administrar en el [!DNL Commerce] [flujo de trabajo de pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Consulte también [Administrar pedidos](./managing-orders.md).

## Configuración de los ajustes de orden {#configure-order-settings}

1. Haga clic **[!UICONTROL Order Settings]** en el panel de la tienda.

1. Para **[!UICONTROL Import Amazon Orders]** (obligatorio), elija una opción:

   - `Disabled` - Elija cuándo no desea crear los pedidos correspondientes en  [!DNL Commerce] cuando se reciban nuevos pedidos de Amazon. Cuando se elige, todos los demás campos de esta página se desactivan.

   - `Enabled` - (Predeterminado) Elija cuándo desea crear los  [!DNL Commerce] pedidos correspondientes cuando se reciban nuevos pedidos de Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y los niveles de stock.

      >[!NOTE]
      >
      >Importar pedidos de Amazon debe establecerse en `Enabled` para administrar los pedidos de Amazon en el flujo de trabajo [!DNL Commerce] [pedidos](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Cuando se establece en `Disabled`, los pedidos de Amazon no tienen un número de pedido [!DNL Commerce] correspondiente y no se pueden administrar en [!DNL Commerce]. Estos pedidos se administran en su cuenta [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Import Amazon Orders Into Magento Store]**, elija a qué [!DNL Commerce] almacena los pedidos de Amazon están asociados cuando se crea el pedido correspondiente en [!DNL Commerce].

   Este valor predeterminado es la vista de la tienda del sitio web seleccionado cuando [agregó la tienda de Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de las [!DNL Commerce] tiendas que haya configurado en la configuración. Consulte [Stores](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Customer Creation]**, elija una opción:

   - `No Customer Creation (guest)` - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente  [!DNL Commerce] utilizando los datos de cliente importados del pedido de Amazon. Cuando se elige, [!DNL Commerce] procesa un pedido de Amazon importado del mismo modo que procesa un cierre de compra de invitado en [!DNL Commerce].

   - `Build New Customer Account` - Elija cuándo desea crear una cuenta de cliente nueva al  [!DNL Commerce] utilizar los datos de cliente importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes a partir de los pedidos de Amazon.

1. Para **[!UICONTROL Order Number Source]**, elija una opción:

   - `Build Using Magento Order Number` - (Predeterminado) Elija cuándo desea crear un número de  [!DNL Commerce] pedido único para el pedido de Amazon correspondiente mediante el ID de pedido asignado  [!DNL Commerce] incrementalmente.

   - `Build Using Amazon Order Number` - Elija cuándo desea crear el número de  [!DNL Commerce] pedido utilizando el número de pedido asignado por Amazon correspondiente.
   >[!NOTE]
   >
   >Después de importar un pedido, el número de pedido de Amazon se muestra en la lista _[!UICONTROL Recent Orders]_del panel de almacenamiento. El número de pedido [!DNL Commerce] se muestra al ver los detalles del pedido en el espacio de trabajo [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

1. Para **[!UICONTROL Order Status]** (obligatorio), elija una opción:

   - `Default Order Status` - (Predeterminado) Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne el estado de pedido predeterminado definido para los nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para los nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}.

   - `Custom Order Status` - Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne un estado distinto al predeterminado.

   - `Processing Order Status` - Habilitado cuando  **[!UICONTROL Order Status]** está establecido en  `Custom Order Status`. Elija el estado que desea utilizar para los pedidos recién creados importados de Amazon. Las opciones de este campo se basan en las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://docs.magento.com/user-guide/sales/order-status.html). También puede crear un estado de pedido personalizado para mostrarlo aquí para su selección. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}.

1. Cuando termine, haga clic en **[!UICONTROL Save order settings]**.

![Configuración de pedidos](assets/amazon-order-settings.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Import Amazon Orders] | Opciones:<ul><li>**[!UICONTROL Disabled]** - Elija cuándo no desea crear los pedidos correspondientes en  [!DNL Commerce] cuando se reciban nuevos pedidos de Amazon. Cuando se elige, todos los demás campos de esta página se desactivan.</li><li>**[!UICONTROL Enabled]** - (Predeterminado) Elija cuándo desea crear los  [!DNL Commerce] pedidos correspondientes cuando se reciban nuevos pedidos de Amazon. [!DNL Commerce] los pedidos se crean en función del estado de Amazon y los niveles de stock.</li></ul><br><br>`Enabled` debe elegirse para administrar los pedidos de Amazon en  [!DNL Commerce]. Cuando se elige `Disabled`, los pedidos de Amazon se muestran en el panel de almacenamiento, pero los pedidos deben administrarse en su cuenta [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Elija a qué [!DNL Commerce] almacenar los pedidos de Amazon están asociados cuando se crean en el espacio de trabajo [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Este valor predeterminado es la vista de la tienda para el sitio web [!DNL Commerce] seleccionado cuando [agregó la tienda de Amazon](./store-integration.md). Si desea cambiar esta configuración, la lista de opciones depende de las [!DNL Commerce] tiendas que haya configurado en la configuración. Consulte [Stores](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Opciones:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Predeterminado) Elija cuándo no desea crear una cuenta de cliente  [!DNL Commerce] utilizando los datos de cliente importados del pedido de Amazon. Cuando se elige, esta opción indica a [!DNL Commerce] que procese un pedido de Amazon importado del mismo modo en que procesa un cierre de compra de invitado.</li><li>**[!UICONTROL Build New Customer Account]** - Elija cuándo desea crear una nueva cuenta de cliente en la base de datos de  [!DNL Commerce] clientes utilizando los datos de cliente importados con el pedido de Amazon. Esta opción ayuda a crear la base de datos de clientes [!DNL Commerce] a partir de los pedidos de Amazon.</li></ul> |
| Origen de número de pedido | Opciones:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Predeterminado) Elija cuándo desea crear un número de  [!DNL Commerce] pedido único para el pedido de Amazon correspondiente mediante el ID de pedido asignado  [!DNL Commerce] incrementalmente. </li><li>**Generar con número de pedido de Amazon** : elija cuándo desea crear el número de  [!DNL Commerce] pedido con el número de pedido asignado a Amazon correspondiente.</li></ul> |
| Pedidos pendientes | Opciones:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Elija cuándo no desea que la cantidad de  [!DNL Commerce] stock se vea afectada por los pedidos de Amazon. Elija si utiliza Amazon para su proceso de cumplimiento (FBA). Cuando se selecciona y recibe un pedido de Amazon, la cantidad solicitada no afecta a la cantidad de stock [!DNL Commerce].</li><li>**[!UICONTROL Reserve Quantity]** - Elija cuándo desea que la cantidad de pedido del pedido de Amazon se &quot;reserve&quot; en la cantidad de  [!DNL Commerce] stock. Cuando se elija y reciba un pedido de Amazon, la cantidad solicitada se &quot;reservará&quot; en la cantidad de existencias [!DNL Commerce] para evitar que las existencias [!DNL Commerce] se vendan excesivamente. La cantidad &quot;reservada&quot; no está disponible para su compra a través de su tienda [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Opciones:<ul><li>**[!UICONTROL Default Order Status]** - (Predeterminado) Elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne el estado de pedido predeterminado para nuevos pedidos. El estado predeterminado de los nuevos pedidos (a menos que haya creado un estado de pedido personalizado para los nuevos pedidos) es `Pending`. Consulte [Procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]**: elija cuándo desea que a los pedidos recién creados importados de Amazon se les asigne un estado distinto al predeterminado. Cuando se elige, **[!UICONTROL Processing Order Status]** permite elegir el estado que desea usar para los pedidos recién creados importados de Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Habilitado cuando _[!UICONTROL Order Status]_está establecido en `Custom Order Status`. Elija el estado de pedido que desea asignar a los nuevos pedidos. Las opciones de este campo dependen de las opciones de estado predeterminadas de [!DNL Commerce]. Consulte [Estado del pedido](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}. También puede crear un estado de pedido personalizado para mostrarlo aquí. Para crear un estado de pedido personalizado, consulte [Estado de pedido personalizado](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}. |

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
>Si se importa un pedido de Amazon en los estados `Partially Shipped` o `Shipped`, la reserva de inventario que se crea es para todos los artículos del pedido. El canal de ventas de Amazon no compensa los artículos que se han enviado anteriormente.
>
>Si Amazon (FBA) cumple un pedido pero un elemento está en estado `out of stock`, [!DNL Commerce] no puede crear un pedido correspondiente. Esta es una limitación de las integraciones de Administración de inventario.
