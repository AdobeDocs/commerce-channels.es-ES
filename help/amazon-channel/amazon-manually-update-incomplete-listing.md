---
title: Actualizar la información necesaria de Amazon
description: El canal de ventas de Amazon proporciona la pestaña Incompleto para controlar los productos del catálogo de Commerce que carecen de la información requerida por Amazon.
feature: Sales Channels, Merchandising, Catalog Management, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Actualizar la información necesaria (anuncio incompleto)

Los anuncios mostrados en la ficha _[!UICONTROL Incomplete]_incluyen los productos del catálogo [!DNL Commerce] que cumplen los requisitos de idoneidad para Amazon definidos en las reglas del anuncio, pero no contienen la información que Amazon necesita antes de ponerlo en venta.

## Actualizar la información necesaria (no se puede asignar a un anuncio de Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Ver los anuncios de la ficha _[!UICONTROL Incomplete]_en [Administrar anuncios](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para el listado que desea actualizar.

1. Revise la información de producto del catálogo (SKU y nombre del producto) que quiere relacionar con un anuncio de Amazon.

1. Para **[!UICONTROL Assign ASIN]**, introduzca el ASIN asignado por Amazon para el listado que desea hacer coincidir con el producto del catálogo.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

El anuncio ahora coincide con el catálogo y, a continuación, se actualiza y publica en Amazon en función de la configuración de cron y del anuncio. También se eliminará de la ficha _[!UICONTROL Incomplete]_.

![Asignar ASIN manualmente para que no haya coincidencias con el listado](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## Actualizar la información necesaria (se encontraron varias coincidencias) {#update-required-info-multiple-matches-found}

1. Ver los listados de la ficha _[!UICONTROL Incomplete]_en [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. En la columna _Acción_, haga clic en **Seleccionar** > **Actualizar la información necesaria** para el listado que desea actualizar.

1. Revise la información de producto del catálogo (SKU y nombre del producto) que quiere relacionar con un anuncio de Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, elija el ASIN correcto para el listado que desea que coincida con este producto.

   Las opciones enumeradas aquí incluyen productos de catálogo que se identifican como posibles coincidencias. Si ninguna de las opciones es correcta, puede elegir `Manually Enter Correct ASIN` e introducir manualmente el ASIN para el producto.

1. Si escribe el ASIN manualmente, escriba el ASIN correcto para **[!UICONTROL Manually Assign ASIN]**.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

![Seleccione manualmente ASIN entre varias coincidencias posibles](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## Actualizar la información necesaria (tiene variantes) {#update-required-info-has-variants}

1. Ver los listados de la ficha _[!UICONTROL Incomplete]_en [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para el listado que desea actualizar.

1. Revise la información de producto del catálogo (SKU y nombre del producto) que quiere relacionar con un anuncio de Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, elija el ASIN correcto para el listado que desea que coincida con este producto.

   Las opciones enumeradas aquí incluyen productos de catálogo que se identifican como posibles coincidencias. Si ninguna de las opciones es correcta, puede seleccionar `Manually Enter Correct ASIN` e introducir manualmente el ASIN para el producto.

1. Si escribe el ASIN manualmente, escriba el ASIN correcto para **[!UICONTROL Manually Assign ASIN]**.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

## Actualizar la información necesaria (falta la condición) {#update-required-info-missing-condition}

1. Ver los anuncios de la ficha _[!UICONTROL Incomplete]_en [Administrar anuncios](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para el listado que desea actualizar.

1. Revise la información de producto del catálogo (SKU y nombre del producto) que quiere relacionar con un anuncio de Amazon.

1. Para **[!UICONTROL Condition]**, elija la condición apropiada.

   La lista de opciones disponibles depende de la configuración de [Condición de la lista de productos](./product-listing-condition.md).

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**

![Actualizar manualmente la condición que falta](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
