---
title: 'Canal de ventas de Amazon: [!UICONTROL Ready to List]'
description: El canal de ventas de Amazon proporciona la pestaña Listo para poner en venta para ayudarle a revisar los productos de Commerce que cumplen los requisitos, pero que no aparecen en la lista automáticamente.
feature: Sales Channels, Products, Merchandising
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

La pestaña _[!UICONTROL Ready to List]_muestra los productos del catálogo [!DNL Commerce] que cumplen la configuración del anuncio y están listos para publicarse en Amazon como un anuncio **nuevo**. A diferencia de otras fichas de listado, esta ficha no siempre aparece en la página [_[!UICONTROL Product Listings]_](./managing-product-listings.md).

La ficha _[!UICONTROL Ready to List]_solo aparece cuando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) está establecido en `Do Not Automatically List Eligible Products` en la configuración del anuncio. Esta configuración indica al canal de ventas de Amazon que cualquier anuncio nuevo de Amazon debe publicarse manualmente.

Cuando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) se establece en `Automatically List Eligible Products`, el canal de ventas de Amazon publica automáticamente nuevos anuncios para los productos de catálogo aptos. Como los nuevos anuncios se publican automáticamente, no se muestra la ficha _[!UICONTROL Ready to List]_.

En _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: elija volver a publicar el listado en [!DNL Amazon Marketplace]. Ver [Listado de Publish y Amazon](./publish-listings-manually.md)

En **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_:

- **[!UICONTROL Publish On Amazon]**: elija volver a publicar el listado en [!DNL Amazon Marketplace]. Ver [Listado de Publish y Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, como el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios para Buy Box de la competencia](./product-listing-details.md#buy-box-competitor-pricing) y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Ver [Ver detalles](./product-listing-details.md).

Tienes algunas opciones para [publicar manualmente un anuncio nuevo en Amazon](./publish-listings-manually.md).

>[!NOTE]
>Si tiene listados en proceso, el número de listados se muestra en un mensaje encima de las pestañas.

![Listo para poner en venta](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## Columnas predeterminadas

| Columna | Descripción |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y elija una opción:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causas comunes de los anuncios listos para publicar en la lista

- **[!UICONTROL Ready to List]**: el producto coincide con un ASIN de Amazon y está programado para su inclusión en la lista. Si [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) está establecido en `Do Not Automatically List Eligible Products` en la configuración de su anuncio, este estado representa los productos que están listos para ser listados manualmente.

- **[!UICONTROL List in Progress]**: la lista de productos se ha enviado a Amazon y está a la espera de la confirmación de aceptación de Amazon.
