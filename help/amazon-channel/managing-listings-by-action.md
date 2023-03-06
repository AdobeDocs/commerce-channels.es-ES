---
title: Administrar listados de productos por acción
description: Al administrar los anuncios de Amazon, puedes aplicar una acción a anuncios individuales o múltiples.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Administrar listados de productos por acción

El _[!UICONTROL Product Listings]_Esta página contiene varias pestañas desde las que puedes ver los estados de todos tus anuncios y hacer coincidir tus productos con los de Amazon.

Las tareas de listado disponibles difieren ligeramente en cada pestaña, pero la variable [controles de workspace](./workspace-controls.md) son iguales y permiten personalizar los datos que se muestran en los anuncios.

Opciones en **[!UICONTROL Actions]** puede aplicar la acción a varios anuncios, mientras que las opciones de **[!UICONTROL Select]** en el _[!UICONTROL Action]_aplica la acción solo a la lista individual.

Consulte también [Administrar anuncios por estado/ficha](./managing-listings-by-tab.md).

| Acción | Descripción | Fichas |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Se utiliza para devolver los productos incompletos al proceso de coincidencia. Para intentar la recoincidencia, debe modificar su [Listado](./listing-settings.md) y [Búsqueda en catálogo](./catalog-search.md) configuración para aumentar el potencial de coincidencia automática. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Haga coincidir manualmente los productos del catálogo con los listados de Amazon seleccionando un listado que coincida, introduciendo un ASIN que coincida o asignando una condición que falte. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Consulta información adicional sobre tus productos activos, incluido el registro de actividad de anuncios, que muestra los cambios en un SKU o producto individual. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Crear un [!DNL Commerce] producto del catálogo que utiliza la información importada con el listado de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Intentar coincidencia automática | Intentar una coincidencia automática entre sus [!DNL Commerce] y sus anuncios de Amazon en función de la configuración de criterios de búsqueda. Para intentar la recoincidencia, debe modificar su [Listado](./listing-settings.md) y [Búsqueda en catálogo](./catalog-search.md) configuración para aumentar el potencial de coincidencia automática. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Seleccione manualmente un producto existente en su [!DNL Commerce] y asignarlo al listado de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Crear un [!DNL Commerce] producto del catálogo que utiliza la información importada con el listado de Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Acción masiva) Se utiliza para volver a poner en venta un anuncio que se ha finalizado o para poner en venta manualmente un producto que cumple los requisitos de las reglas del anuncio, pero _[!UICONTROL Product Listing Actions]_no se ha establecido en `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (Acción de anuncio único) Se utiliza para volver a poner en venta un anuncio que ha finalizado. Esta acción también se usa para poner en venta manualmente un producto que cumpla los requisitos de las reglas de la lista cuando _[!UICONTROL Product Listing Actions]_no se ha establecido en `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Acción masiva) Se utiliza para finalizar y eliminar manualmente los anuncios de sus productos que existen en Amazon. Los anuncios finalizados se pueden volver a poner en venta siempre que cumplan las normas de tu anuncio. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Acción masiva) Edita manualmente una &quot;anulación&quot; existente que establece el precio, el tiempo de manipulación, la condición y el texto de las notas del vendedor para un anuncio individual, ignorando otros valores predeterminados, configuraciones y reglas del anuncio. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Crea de forma manual una &quot;invalidación&quot; que establezca el precio, el tiempo de manipulación, la condición y el texto de las notas del vendedor para un anuncio individual, ignorando otros valores predeterminados, configuraciones y reglas del anuncio. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Se utiliza si se debe modificar el ASIN que coincide con el producto del catálogo (por ejemplo: si el producto coincide con el ASIN del listado incorrecto). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Puede cumplir dos funciones:<br><br>Se puede utilizar para crear una relación individual entre el producto del catálogo y dos listados de Amazon. Ejemplo: Amazon tiene el producto enumerado con diferentes valores ASIN. Puede hacer coincidir su producto de un catálogo con ambos listados ASIN para el producto.<br><br>Se puede utilizar para controlar un anuncio en diferentes regiones de Amazon. Ejemplo: Tiene un producto de catálogo que tiene diferentes métodos de envío definidos en función de la región de Amazon (la región de EE. UU. es FBA y la de Canadá es FBM). Para controlar las existencias y la cantidad, puede crear un SKU de vendedor alias y volver a poner en venta el mismo producto en esa región con un SKU de vendedor diferente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Se utiliza para modificar el método de cumplimiento asociado con su producto (Satisfecho por Amazon: FBA o Satisfecho por el Comerciante: FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (Acción de anuncio único) Se utiliza para finalizar y eliminar manualmente los anuncios de sus productos que existen en Amazon. Los anuncios finalizados se pueden volver a poner en venta siempre que cumplan las normas de tu anuncio. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (Acción de anuncio único) Edita manualmente una &quot;anulación&quot; existente que establece el precio, el tiempo de manipulación, la condición y el texto de las notas del vendedor de un anuncio individual, ignorando los valores predeterminados, la configuración y las reglas de otros anuncios. | [[!UICONTROL Overrides]](./overrides.md) |

## Acceder a listados de productos

1. En el _Administrador_ barra lateral, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

1. Clic **Ver tienda** en la tarjeta de la tienda.

1. En el tablero de la tienda, haga clic en **Administrar anuncios** en el _Anuncios de tienda_ sección.
