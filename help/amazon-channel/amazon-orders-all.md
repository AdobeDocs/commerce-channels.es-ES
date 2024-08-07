---
title: Ver pedidos de Amazon
description: Vea sus pedidos de Amazon Marketplace en Adobe Commerce o en el administrador de Magento Open Source.
feature: Sales Channels, Orders
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Ver pedidos de Amazon

Existen dos formas de ver sus pedidos de Amazon: _[!UICONTROL Recent Orders]_y_[!UICONTROL All Orders]_.

Ambas opciones muestran información básica del pedido, tal como se recibe de Amazon, como:

- Fecha de compra
- Número de pedido
- Estado
- Nombre del comprador
- Total general
- Notas del pedido

La vista _[!UICONTROL All Orders]_agrega opciones de filtrado para las búsquedas de pedidos.

>[!NOTE]
>
>Excepto en la columna _[!UICONTROL Order Notes]_, la tabla_[!UICONTROL Amazon orders]_ se rellena con la información de pedidos recibida de Amazon. [!DNL Commerce] actualiza la columna _Notas de pedido_ a medida que se procesa el pedido.

## Pedidos recientes

Puede ver sus pedidos más recientes en la sección _[!UICONTROL Recent Orders]_del [panel de almacenamiento](./amazon-store-dashboard.md).

![Pedidos recientes](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### Ver pedidos recientes de Amazon

1. Haga clic en **[!UICONTROL View Store]** en una tarjeta de tienda.

1. Vea sus pedidos en la sección _[!UICONTROL Recent Orders]_.

1. Para ver los detalles del pedido, haga clic en el número de pedido Amazon en la columna _[!UICONTROL Order Number]_.

   Se abre la página _[!UICONTROL Amazon Order Details]_del pedido.

## Ver todos los pedidos

Puede ver todos sus pedidos de Amazon en la página _[!UICONTROL Amazon orders]_(también denominada vista_[!UICONTROL All Orders]_). La tabla Pedidos de Amazon es similar a la sección _[!UICONTROL Recent Orders]_del panel de almacén, pero le permite ver todos sus pedidos de Amazon y reducir la lista de pedidos con las siguientes opciones de filtro:

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Pedidos de Amazon](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### Ver todos los pedidos de Amazon

1. Haga clic en **[!UICONTROL View Store]** en una tarjeta de tienda.

1. Haga clic en **[!UICONTROL All Orders]** en la sección _[!UICONTROL Recent Orders]_.

1. Para reducir la lista o buscar un número de pedido específico, complete los **[!UICONTROL Filter by]** parámetros y haga clic en **[!UICONTROL Apply filters]**.

1. Para ver los detalles del pedido, haga clic en el número de pedido Amazon en la columna _[!UICONTROL Order Number]_.

   Se abre la página _[!UICONTROL Amazon Order Details]_del pedido.

## Uso de filtros

Puede aplicar filtros a la lista de pedidos en la sección _[!UICONTROL Filter by]_. Realice sus selecciones y haga clic en **[!UICONTROL Apply filters]**. Los filtros aplicados aparecerán encima de la cuadrícula de pedidos.

![Filtros para ver pedidos de Amazon](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### Cambio de los filtros aplicados

- Puede agregar o cambiar los filtros en la sección _[!UICONTROL Filter by]_. Haga clic en **[!UICONTROL Apply filters]**para actualizar la lista de pedidos y las opciones de filtro que aparecen sobre la cuadrícula de pedidos.

- Puede quitar filtros de uno en uno haciendo clic en `x` para el filtro o de uno en uno haciendo clic en **[!UICONTROL Clear all filters]**. Al eliminar un filtro, se actualiza la lista de pedidos y las opciones de filtro que aparecen encima de la cuadrícula de pedidos.

- Si la lista de pedidos es larga, puede utilizar los controles de paginación situados debajo de la cuadrícula para ver más pedidos.

>[!TIP]
>
>Algunas sugerencias sobre la vista de pedidos:
>
>- Si tiene varias integraciones de tienda Amazon, podría ser necesario actualizar la vista de página al cambiar entre las vistas de tienda para actualizar tanto la lista de pedidos como las vistas de paginación de la tienda actual.
>- Al ordenar por columna, el orden solo se aplica a la vista de lista actual. Se recomienda filtrar la lista y ordenar la página que está viendo.
>- Según el ancho de la ventana de vista, puede ver texto superpuesto en las columnas. Para expandir las columnas para que el texto se ajuste, amplíe la vista de la ventana.
>- Al filtrar por _[!UICONTROL Total]_, filtrar por números enteros. La introducción de una cantidad decimal puede provocar errores en los resultados.

### Columnas predeterminadas

| Columna | Descripción |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | Disponible solamente en la vista _[!UICONTROL All Orders]_.<br>Reduzca la lista de pedidos según:<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | La fecha de la compra tal como se recibió de Amazon. |
| [!UICONTROL Order Number] | El número de pedido generado por Amazon y recibido de. Para ver la pantalla Detalles del pedido de Amazon, haga clic en el vínculo. |
| [!UICONTROL Status] | El estado del pedido tal como lo recibió Amazon. Opciones: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | El nombre de la persona que realizó el pedido, tal como se recibió de Amazon. |
| [!UICONTROL Grand Total] | El valor de divisa total del pedido, tal como se recibió de Amazon. |
| [!UICONTROL Order Notes] | La acción más reciente registrada para el pedido mientras se procesa en [!DNL Commerce]. La información incluye, entre otros, errores de importación de pedidos y actualizaciones de procesamiento de pedidos.<br>**Nota**: este campo lo actualiza [!DNL Commerce] a medida que se procesa el pedido. |
