---
title: Actualizar información requerida (lista incompleta)
description: El canal de ventas de Amazon proporciona la pestaña Incomplete para monitorizar los productos del catálogo de comercio que no tienen la información requerida por Amazon.
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Actualizar información requerida (lista incompleta)

Los anuncios mostrados en la pestaña _[!UICONTROL Incomplete]_incluyen los productos de catálogo de [!DNL Commerce] que cumplen los requisitos de elegibilidad de Amazon definidos en las reglas de listado, pero que carecen de la información requerida por Amazon antes de su inclusión en la lista.

## Actualizar la información necesaria (no se puede asignar a la lista de Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Vea los listados en la pestaña _[!UICONTROL Incomplete]_en [Administrar listados](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para ver el listado que desea actualizar.

1. Revise la información del producto del catálogo (SKU y nombre de producto) para la que está intentando coincidir con un anuncio de Amazon.

1. Para **[!UICONTROL Assign ASIN]**, introduzca el ASIN asignado por Amazon para la lista que desea que coincida con el producto del catálogo.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

El listado ahora coincide con su catálogo y luego se actualiza y publica en Amazon en función de su configuración de cron y listado. También se elimina de la pestaña _[!UICONTROL Incomplete]_.

![Asignar ASIN manualmente para que no coincida con el listado](assets/amazon-listing-update-assign-asin.png)

## Actualizar la información necesaria (se encontraron varias coincidencias) {#update-required-info-multiple-matches-found}

1. Vea los listados en la pestaña _[!UICONTROL Incomplete]_en [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. En la columna _Action_, haga clic en **Select** > **Update Required Info** para ver la lista que desea actualizar.

1. Revise la información del producto del catálogo (SKU y nombre de producto) para la que está intentando coincidir con un anuncio de Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, elija el ASIN correcto para la lista que desea que coincida con este producto.

   Las opciones enumeradas aquí incluyen productos de catálogo que se identifican como posibles coincidencias. Si ninguna de las opciones es correcta, puede elegir `Manually Enter Correct ASIN` e introducir manualmente el ASIN para el producto.

1. Si introduce el ASIN manualmente, introduzca el ASIN correcto para **[!UICONTROL Manually Assign ASIN]**.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

![Seleccione ASIN manualmente entre varias coincidencias posibles](assets/amazon-listing-update-multiple-matches.png)

## Actualizar la información necesaria (tiene variantes) {#update-required-info-has-variants}

1. Vea los listados en la pestaña _[!UICONTROL Incomplete]_en [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para ver el listado que desea actualizar.

1. Revise la información del producto del catálogo (SKU y nombre de producto) para la que está intentando coincidir con un anuncio de Amazon.

1. Para **[!UICONTROL Select Correct Amazon Listing]**, elija el ASIN correcto para la lista que desea que coincida con este producto.

   Las opciones enumeradas aquí incluyen productos de catálogo que se identifican como posibles coincidencias. Si ninguna de las opciones es correcta, puede seleccionar `Manually Enter Correct ASIN` e introducir manualmente el ASIN para el producto.

1. Si introduce el ASIN manualmente, introduzca el ASIN correcto para **[!UICONTROL Manually Assign ASIN]**.

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]**.

![Seleccionar ASIN manualmente de posibles coincidencias de variantes](assets/amazon-listing-update-multiple-matches.png)

## Actualizar la información necesaria (condición que falta) {#update-required-info-missing-condition}

1. Vea los listados en la pestaña _[!UICONTROL Incomplete]_en [Administrar listados](./managing-product-listings.md).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**para ver el listado que desea actualizar.

1. Revise la información del producto del catálogo (SKU y nombre de producto) para la que está intentando coincidir con un anuncio de Amazon.

1. Para **[!UICONTROL Condition]**, elija la condición adecuada.

   La lista de opciones disponibles depende de la configuración de [Condición de lista de productos](./product-listing-condition.md).

1. Para guardar la coincidencia del producto, haga clic en **[!UICONTROL Save Listing Update]** .

![Actualizar manualmente la condición que falta](assets/amazon-update-listing-missing-condition.png)
