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

El _[!UICONTROL Product Listings]_Esta página contiene varias pestañas desde las que puedes ver los estados de todos tus anuncios y hacer coincidir tus productos con los de Amazon.

Las tareas de listado disponibles difieren ligeramente en cada pestaña, pero la variable [controles de workspace](./workspace-controls.md) son iguales y permiten personalizar los datos que se muestran en los anuncios.

Opciones en **[!UICONTROL Actions]** puede aplicar la acción a varios anuncios, mientras que las opciones de **[!UICONTROL Select]** en el _[!UICONTROL Action]_aplica la acción solo a la lista individual.

Consulte también [Administrar anuncios por acción](./managing-listings-by-action.md).

![Fichas de listados de productos](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| Ficha | Descripción | Acciones |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Muestra su [!DNL Commerce] los productos de catálogo que cumplen la configuración de anuncio definida pero que carecen de la información requerida por Amazon para un anuncio.<br><br>If _[!UICONTROL Automatic List Action]_se establece en `Automatically List Eligible Products` en su [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración, estos elementos son sus **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Muestra los anuncios de Amazon existentes (según la información recibida de Amazon) que no coinciden con ningún producto de su [!DNL Commerce] catálogo. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Intentar coincidencia automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Muestra los productos del catálogo que están listos para crear anuncios de Amazon, pero tu tienda no está configurada para publicar automáticamente nuevos anuncios. Esta pestaña se utiliza para publicar manualmente los nuevos anuncios.<br><br>If _[!UICONTROL Automatic List Action]_se establece en `Do Not Automatically List Eligible Products` en su [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración, estos elementos son sus **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Muestra los productos de catálogo que se han publicado en Amazon pero que Amazon no ha aprobado para el estado Activo. | [Fin Anuncio(s) en Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Muestra los anuncios de Amazon que coinciden con un producto de su [!DNL Commerce] catálogo, se han publicado en Amazon y Amazon los ha publicado para el estado Activo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Muestra los anuncios de Amazon que cumplen los criterios para una anulación definida y a los que se ha aplicado dicha anulación. Las invalidaciones tienen prioridad sobre cualquier otra configuración de cuenta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Muestra los anuncios existentes de Amazon que ya no cumplen los requisitos según las [configuración de listado](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Muestra tus anuncios de Amazon que se han finalizado (eliminado) manualmente en Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acceder a listados de productos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clic **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el tablero de la tienda, haga clic en **[!UICONTROL Manage Listings]** en el _[!UICONTROL Store Listings]_sección.
