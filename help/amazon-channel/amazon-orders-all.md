---
title: Ver pedidos de Amazon
description: Consulte sus pedidos de Amazon Marketplace en el administrador de Adobe Commerce o Magento Open Source.
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Ver pedidos de Amazon

Existen dos formas de ver los pedidos de Amazon: _[!UICONTROL Recent Orders]_y_[!UICONTROL All Orders]_.

Ambas opciones muestran la información básica de los pedidos, tal como la recibe de Amazon, que incluye:

- Fecha de compra
- Número de pedido
- Estado
- Nombre del comprador
- Total general
- Notas del pedido

_[!UICONTROL All Orders]_view agrega opciones de filtrado para búsquedas de pedidos.

>[!NOTE]
>
>Excepto para el _[!UICONTROL Order Notes]_, la variable_[!UICONTROL Amazon orders]_ se rellena con información de pedido recibida de Amazon. La variable _Notas del pedido_ se actualiza con [!DNL Commerce] como el proceso de pedido.

## Pedidos recientes

Puede ver los pedidos más recientes en la _[!UICONTROL Recent Orders]_de la sección [tablero de almacenamiento](./amazon-store-dashboard.md).

![Pedidos recientes](assets/amazon-recent-orders-imported.png)

### Ver pedidos recientes de Amazon

1. Haga clic en **[!UICONTROL View Store]** en una tarjeta de la tienda.

1. Vea sus pedidos en la _[!UICONTROL Recent Orders]_para obtener más información.

1. Para ver los detalles del pedido, haga clic en el número de pedido de Amazon en la _[!UICONTROL Order Number]_para abrir el Navegador.

   La variable _[!UICONTROL Amazon Order Details]_para abrir el formulario de solicitud.

## Ver todos los pedidos

Puede ver todos sus pedidos de Amazon en la _[!UICONTROL Amazon orders]_(también denominada_[!UICONTROL All Orders]_ vista). La tabla Pedidos de Amazon es similar a la del _[!UICONTROL Recent Orders]_del panel de la tienda, pero le permite ver todos sus pedidos de Amazon y reducir la lista de pedidos con las siguientes opciones de filtro:

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Pedidos de Amazon](assets/amazon-orders-list-all.png)

### Ver todos los pedidos de Amazon

1. Haga clic en **[!UICONTROL View Store]** en una tarjeta de la tienda.

1. Haga clic en **[!UICONTROL All Orders]** en el _[!UICONTROL Recent Orders]_para obtener más información.

1. Para reducir la lista o buscar un número de orden específico, complete la **[!UICONTROL Filter by]** parámetros y haga clic en **[!UICONTROL Apply filters]**.

1. Para ver los detalles del pedido, haga clic en el número de pedido de Amazon en la _[!UICONTROL Order Number]_para abrir el Navegador.

   La variable _[!UICONTROL Amazon Order Details]_para abrir el formulario de solicitud.

## Uso de filtros

Puede aplicar filtros a la lista de pedidos en la _[!UICONTROL Filter by]_para obtener más información. Realice las selecciones y haga clic en **[!UICONTROL Apply filters]**. Los filtros aplicados aparecen encima de la cuadrícula de pedidos.

![Filtros para ver pedidos de Amazon](assets/amazon-orders-filter-view.png)

### Cambio de los filtros aplicados

- Puede añadir o cambiar los filtros en la variable _[!UICONTROL Filter by]_para obtener más información. Haga clic en **[!UICONTROL Apply filters]**para actualizar la lista de pedidos y las opciones de filtro que aparecen encima de la cuadrícula de pedidos.

- Puede quitar los filtros de uno en uno haciendo clic en el botón `x` para el filtro o todo a la vez haciendo clic en **[!UICONTROL Clear all filters]**. Al quitar un filtro, se actualiza la lista de pedidos y las opciones de filtro que aparecen encima de la cuadrícula de pedidos.

- Si la lista de pedidos es larga, puede utilizar los controles de paginación situados debajo de la cuadrícula para ver más pedidos.

>[!TIP]
>
>Algunas sugerencias sobre la vista de pedidos:
>
>- Si tiene varias integraciones de la tienda de Amazon, podría ser necesario actualizar la vista de la página al cambiar entre vistas de la tienda para actualizar la lista de pedidos y las vistas de paginación del almacén actual.
>- Al ordenar por columna, la ordenación solo se aplica a la vista de lista actual. Filtrar la lista y luego ordenar la página que está viendo es una práctica recomendada.
>- Según el ancho de la ventana de vista, puede ver texto superpuesto en las columnas. Para expandir las columnas para que el texto se ajuste, amplíe la vista de la ventana.
>- Al filtrar por _[!UICONTROL Total]_, filtre por números enteros. La introducción de una cantidad decimal puede causar errores en los resultados.


### Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Filter by] | Disponible solo en la variable _[!UICONTROL All Orders]_vista.<br>Reducir la lista de pedidos en función de:<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | La fecha de la compra, tal como se recibió de Amazon. |
| [!UICONTROL Order Number] | Número de pedido que Amazon genera y recibe. Para ver la pantalla Detalles del pedido de Amazon, haga clic en el vínculo . |
| [!UICONTROL Status] | El estado del pedido, tal como lo recibió Amazon. Opciones: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Nombre de la persona que realizó el pedido, tal como se recibió de Amazon. |
| [!UICONTROL Grand Total] | El valor monetario total del pedido, según se recibió de Amazon. |
| [!UICONTROL Order Notes] | Acción más reciente registrada para la solicitud mientras se procesa en [!DNL Commerce]. La información incluye, entre otros, errores de importación de pedidos y actualizaciones de procesamiento de pedidos.<br>**Nota**: Este campo se actualiza mediante [!DNL Commerce] como el proceso de pedido. |
