---
title: Anuncios de Amazon incompletos
description: El canal de ventas de Amazon proporciona [!UICONTROL Incomplete] para ayudarte a identificar y cumplir los requisitos para tus anuncios de Amazon incompletos.
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Anuncios de Amazon incompletos

El _[!UICONTROL Incomplete]_enumera las [!DNL Commerce] catalogar productos que cumplan los requisitos de idoneidad para Amazon (definidos en su [enumerar reglas](./listing-rules.md)), pero faltan la información requerida por Amazon (como el ASIN de Amazon o una condición de producto definida).

Hay cuatro causas posibles para una lista incompleta, cada una identificada por su estado.

| Estado | Motivo | Acción |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Falta la condición | Amazon acepta anuncios en diversas condiciones (como _Nuevo_, _Restaurado_, _Usado: como nuevo_) el anuncio requiere una condición definida. | Actualice la información necesaria y manualmente [asignar una condición](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) a un anuncio. |
| No se puede asignar al listado de Amazon | Error al hacer coincidir automáticamente este anuncio con el catálogo. Si no se encuentra ninguna coincidencia, la Sales Channel de Amazon no puede administrar la lista | Actualice la información necesaria y manualmente [asignar un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) al producto del catálogo para que coincida con el listado. |
| Se encontraron varias coincidencias | Error al hacer coincidir automáticamente este anuncio con el catálogo. Si se encuentran varias coincidencias posibles, debe seleccionar la coincidencia correcta para el producto. | Actualice la información necesaria y manualmente [elija una coincidencia de producto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para el producto y listado. |
| Tiene variantes | Si el producto tiene variantes, como una camiseta disponible en diferentes tamaños o colores, debe elegir la variante del catálogo para que se asigne correctamente y coincida con el listado | Actualice la información necesaria y manualmente [elija la variante correcta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para asignar y hacer coincidir con este listado. |

>[!NOTE]
>Cuando los anuncios incompletos coinciden correctamente con los productos del catálogo, el anuncio se desplaza del _[!UICONTROL Incomplete]_y se publican en Amazon en función de sus [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración.

Las acciones disponibles en la _[!UICONTROL Incomplete]_pestaña incluir:

En _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: elige iniciar el proceso automático para hacer coincidir los datos de los anuncios de Amazon con los de tu [!DNL Commerce] catálogo. Si los productos no coinciden automáticamente, vuelva a su [_[!UICONTROL Catalog Search]_](./catalog-search.md) opciones de las opciones de los anuncios. Si los anuncios no coinciden automáticamente después de actualizar tu _[!UICONTROL Catalog Search]_opciones, puede hacer coincidir los productos manualmente en la [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) acción.

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL Update Required Info]**: elige si los anuncios no coinciden automáticamente con el catálogo. Puede hacerlo manualmente [hacer coincidir los productos del catálogo con los anuncios](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), manualmente [asignar un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) a una coincidencia de catálogo, o [asignar una condición que falta](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para su inclusión en lista.

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, incluido el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios de competidor Buy Box](./product-listing-details.md#buy-box-competitor-pricing), y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Consulte [Ver detalles](./product-listing-details.md).

>[!NOTE]
>
>Si tiene listados en proceso, el número de listados aparece en un mensaje encima de las pestañas.

![Anuncios de Amazon incompletos](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos elementos comunes [controles de workspace](./workspace-controls.md) que permiten personalizar los datos que se muestran.

| Columna | Descripción |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa el [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | El [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. Consulte la tabla Estado más arriba. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y seleccione una opción:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
