---
title: Administrar listas de productos por acción
description: A medida que administra sus listados de Amazon, puede aplicar una acción a los listados individuales o múltiples.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Administrar listas de productos por acción

La página _[!UICONTROL Product Listings]_contiene varias pestañas desde las que puede ver los estados de todos sus anuncios y hacer coincidir sus productos con los listados de Amazon.

Las tareas de listado disponibles difieren ligeramente en cada ficha, pero los [controles del espacio de trabajo](./workspace-controls.md) son los mismos y le permiten personalizar los datos que se muestran para sus listados.

Las opciones de **[!UICONTROL Actions]** pueden aplicar la acción a varios listados, mientras que las opciones de **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_aplican la acción solo a los listados individuales.

Consulte también [Administrar anuncios por estado / Tab](./managing-listings-by-tab.md).

| Acción | Descripción | Pestañas |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Se utiliza para volver a mover los productos incompletos a través del proceso de coincidencia. Para intentar volver a coincidir, debe modificar las opciones [Listing](./listing-settings.md) y [Catalog Search](./catalog-search.md) para aumentar el potencial de coincidencia automática. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Para hacer coincidir manualmente los productos del catálogo con los listados de Amazon, seleccione un listado para que coincida, introduzca un ASIN para que coincida o asigne una condición que falte. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Vea información adicional sobre sus productos activos, incluido el Registro de actividades de lista, que muestra los cambios en un SKU o producto individual. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Cree un producto de catálogo [!DNL Commerce] utilizando la información importada con la lista de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Intentar coincidencia automática | Intente que haya una coincidencia automática entre el catálogo de [!DNL Commerce] y las listas de Amazon según la configuración de los criterios de búsqueda. Para intentar volver a coincidir, debe modificar las opciones [Listing](./listing-settings.md) y [Catalog Search](./catalog-search.md) para aumentar el potencial de coincidencia automática. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Seleccione manualmente un producto existente en su catálogo [!DNL Commerce] y asígnelo a la lista de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Cree un producto de catálogo [!DNL Commerce] utilizando la información importada con la lista de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Acción masiva) Se utiliza para volver a enumerar un listado que ha finalizado o para enumerar manualmente un producto que cumpla los requisitos de las reglas de listado, pero su _[!UICONTROL Product Listing Actions]_no está configurado en `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (Acción de lista única) Se utiliza para volver a enumerar una lista que ha finalizado. Esta acción también se utiliza para listar manualmente un producto que cumpla los requisitos de las reglas de listado cuando _[!UICONTROL Product Listing Actions]_no esté establecido en `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Acción masiva) Se utiliza para finalizar y eliminar manualmente los anuncios de sus productos que existen en Amazon. Los anuncios finalizados se pueden confiar siempre que cumplan los requisitos de las reglas de listado. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Acción masiva) Edite manualmente una &quot;anulación&quot; existente que establezca el precio, el tiempo de administración, la condición y el texto de notas del vendedor para un anuncio individual, ignorando otros valores predeterminados, configuraciones y reglas del anuncio. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Cree manualmente una &quot;anulación&quot; que establezca el precio, el tiempo de gestión, la condición y el texto de notas de vendedor para un anuncio individual, ignorando otros valores predeterminados, configuraciones y reglas de anuncios. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Se utiliza si ASIN coincide con el producto de su catálogo debe modificarse (por ejemplo: si el producto coincide con el listado incorrecto (ASIN). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Puede servir dos funciones:<br><br>Se puede utilizar para crear una relación de 1 a 2 entre el producto del catálogo y dos listas de Amazon. Ejemplo: Amazon tiene el producto enumerado con diferentes valores ASIN. Puede hacer coincidir su producto de catálogo con los dos anuncios ASIN del producto.<br><br>Se puede utilizar para controlar una lista en diferentes regiones de Amazon. Ejemplo: Tiene un producto de catálogo que tiene diferentes métodos de envío definidos en función de la región de Amazon (la región de EE. UU. es FBA y la región de Canadá es FBM). Para controlar las existencias y la cantidad, puede crear un SKU de vendedor de alias y volver a poner en venta el mismo producto en esa región con un SKU de vendedor diferente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Se utiliza para modificar el método de cumplimiento asociado con su producto (Satisfecho por Amazon: FBA o cumplido por comerciante: FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (Acción de lista única) Se utiliza para finalizar y eliminar manualmente los anuncios de sus productos que existen en Amazon. Los anuncios finalizados se pueden confiar siempre que cumplan los requisitos de las reglas de listado. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (Acción de un solo listado) Edite manualmente una &quot;anulación&quot; existente que establezca el precio, el tiempo de gestión, la condición y el texto de las notas del vendedor para un listado individual, ignorando otros valores predeterminados, configuraciones y reglas del listado. | [[!UICONTROL Overrides]](./overrides.md) |

## Acceso a listas de productos

1. En la barra lateral _Admin_, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

1. Haga clic en **Ver tienda** en la tarjeta de la tienda.

1. En el panel de la tienda, haga clic en **Administrar anuncios** en la sección _Store Listings_.
