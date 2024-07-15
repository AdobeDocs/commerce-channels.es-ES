---
title: Administrar listados de productos de Amazon por estado/pestaña
description: Al administrar los anuncios de Amazon, puedes aplicar acciones a los anuncios según su estado.
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Administrar listados de productos de Amazon por estado/pestaña

La página _[!UICONTROL Product Listings]_contiene varias fichas desde las cuales puede ver los estados de todos los anuncios y hacer coincidir los productos con los anuncios de Amazon.

Las tareas de listado disponibles difieren ligeramente en cada ficha, pero los [controles del espacio de trabajo](./workspace-controls.md) son iguales y le permiten personalizar los datos que se muestran para sus listados.

Las opciones de **[!UICONTROL Actions]** pueden aplicar la acción a varios listados, mientras que las de **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_aplican la acción únicamente a un listado individual.

Ver también [Administrar anuncios por acción](./managing-listings-by-action.md).

![fichas de listados de productos](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| Ficha | Descripción | Acciones |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Muestra los productos del catálogo [!DNL Commerce] que cumplen la configuración de anuncio definida pero que carecen de la información requerida por Amazon para un anuncio.<br><br>Si _[!UICONTROL Automatic List Action]_está establecido en `Automatically List Eligible Products` en su configuración de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md), estos elementos son sus **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Muestra los listados de Amazon existentes (según la información recibida de Amazon) que no coinciden con un producto del catálogo [!DNL Commerce]. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Intentar coincidencia automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Muestra los productos del catálogo que están listos para crear anuncios de Amazon, pero tu tienda no está configurada para publicar automáticamente nuevos anuncios. Esta pestaña se utiliza para publicar manualmente los nuevos anuncios.<br><br>Si _[!UICONTROL Automatic List Action]_está establecido en `Do Not Automatically List Eligible Products` en su configuración de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md), estos elementos son sus **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Muestra los productos de catálogo que se han publicado en Amazon pero que Amazon no ha aprobado para el estado Activo. | [Finalizar anuncio(s) en Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Muestra los listados de Amazon que coinciden con un producto del catálogo [!DNL Commerce], que se han publicado en Amazon y que Amazon ha publicado para el estado Activo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambio a completado por Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Muestra los anuncios de Amazon que cumplen los criterios para una anulación definida y a los que se ha aplicado dicha anulación. Las invalidaciones tienen prioridad sobre cualquier otra configuración de cuenta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Muestra los anuncios existentes de Amazon que ya no cumplen los requisitos, según la configuración definida para el [anuncio](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambio a completado por Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Muestra tus anuncios de Amazon que se han finalizado (eliminado) manualmente en Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acceder a listados de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el tablero del almacén, haga clic en **[!UICONTROL Manage Listings]** en la sección _[!UICONTROL Store Listings]_.
