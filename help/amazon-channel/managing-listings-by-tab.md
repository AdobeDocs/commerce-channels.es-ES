---
title: Administrar listas de productos por estado/ficha
description: A medida que administra sus anuncios de Amazon, puede aplicar acciones a sus anuncios según el estado.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Administrar listas de productos por estado/ficha

La variable _[!UICONTROL Product Listings]_contiene varias pestañas desde las que puede ver los estados de todos sus listados y hacer coincidir sus productos con los listados de Amazon.

Las tareas de listado disponibles difieren ligeramente en cada pestaña, pero la variable [controles del espacio de trabajo](./workspace-controls.md) son los mismos y permiten personalizar los datos que se muestran para sus anuncios.

Opciones en **[!UICONTROL Actions]** puede aplicar la acción a varios listados, mientras que las opciones de **[!UICONTROL Select]** en el _[!UICONTROL Action]_aplicar la acción solo a la lista individual.

Consulte también [Administrar anuncios por acción](./managing-listings-by-action.md).

![Pestañas de listas de productos](assets/amazon-product-listings-tabs.png)

| Tabulación | Descripción | Acciones |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Muestra su [!DNL Commerce] catálogo de productos que cumplen con la configuración de listado definida pero que carecen de la información requerida por Amazon para un listado.<br><br>If _[!UICONTROL Automatic List Action]_está configurado como `Automatically List Eligible Products` en su [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración, estos elementos son su **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Muestra los anuncios de Amazon existentes (según la información recibida de Amazon) que no coinciden con un producto de su [!DNL Commerce] catálogo. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Intentar coincidencia automática<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Muestra los productos de catálogo que están listos para crear anuncios de Amazon, pero la tienda no está configurada para publicar automáticamente nuevos anuncios. Esta pestaña se utiliza para publicar manualmente los nuevos anuncios.<br><br>If _[!UICONTROL Automatic List Action]_está configurado como `Do Not Automatically List Eligible Products` en su [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración, estos elementos son su **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Muestra los productos del catálogo que se han publicado en Amazon, pero Amazon no ha aprobado el listado para el estado Activo. | [Fin Listing(s) en Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Muestra los anuncios de Amazon que han coincidido con un producto de su [!DNL Commerce] , se han publicado en Amazon y Amazon lo ha hecho para obtener el estado Activo. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Muestra los anuncios de Amazon que cumplen los criterios de una anulación definida y a los que se ha aplicado la anulación. Las anulaciones tienen prioridad sobre cualquier otra configuración de cuenta. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Muestra los anuncios de Amazon existentes que ya no son aptos, según su [configuración de listado](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Cambiar a Satisfecho por Amazon/Comerciante<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Muestra los anuncios de Amazon que se han finalizado (eliminado) manualmente de Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Acceso a listas de productos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

1. En el panel de la tienda, haga clic en **[!UICONTROL Manage Listings]** en el _[!UICONTROL Store Listings]_para obtener más información.
