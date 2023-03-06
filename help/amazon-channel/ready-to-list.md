---
title: Listo para la lista
description: El canal de ventas de Amazon proporciona la pestaña Listo para poner en venta para ayudarle a revisar los productos de Commerce que cumplen los requisitos, pero que no aparecen en la lista automáticamente.
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

El _[!UICONTROL Ready to List]_La pestaña muestra su [!DNL Commerce] catálogo productos que cumplan la configuración de su anuncio y que estén listos para publicar en Amazon as a **nuevo**listado. A diferencia de otras pestañas de listado, esta pestaña no siempre aparece en la [_[!UICONTROL Product Listings]_](./managing-product-listings.md) página.

El _[!UICONTROL Ready to List]_La pestaña solo aparece cuando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) en la configuración del anuncio se establece como `Do Not Automatically List Eligible Products`. Esta configuración indica al canal de ventas de Amazon que cualquier anuncio nuevo de Amazon debe publicarse manualmente.

Cuándo [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) se establece en `Automatically List Eligible Products`, el canal de ventas de Amazon publica automáticamente nuevos anuncios para los productos de catálogo aptos. Como los nuevos anuncios se publican automáticamente, la variable _[!UICONTROL Ready to List]_no se muestra.

En _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: elija volver a publicar el listado en [!DNL Amazon Marketplace]. Consulte [Publicar un anuncio de Amazon](./publish-listings-manually.md)

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL Publish On Amazon]**: elija volver a publicar el listado en [!DNL Amazon Marketplace]. Consulte [Publicar un anuncio de Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, incluido el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios de competidor Buy Box](./product-listing-details.md#buy-box-competitor-pricing), y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Consulte [Ver detalles](./product-listing-details.md).

Tiene algunas opciones para configurar manualmente [publicar un anuncio nuevo en Amazon](./publish-listings-manually.md).

>[!NOTE]
>Si tiene listados en proceso, el número de listados se muestra en un mensaje encima de las pestañas.

![Listo para la lista](assets/amazon-ready-to-list.png)

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa el [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | El [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y elija una opción:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causas comunes de los anuncios listos para publicar en la lista

- **[!UICONTROL Ready to List]** : el producto coincide con un ASIN de Amazon y está programado para su inclusión en la lista. If [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) en la configuración del anuncio se establece como `Do Not Automatically List Eligible Products`, este estado representa los productos que están listos para incluirse manualmente en la lista.

- **[!UICONTROL List in Progress]** : la lista de productos se ha enviado a Amazon y está a la espera de la confirmación de aceptación por parte de Amazon.
