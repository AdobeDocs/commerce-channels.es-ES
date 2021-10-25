---
title: Listas incompletas
description: El canal de ventas de Amazon proporciona la variable [!UICONTROL Incomplete] para ayudarle a identificar y cumplir los requisitos de elegibilidad para sus anuncios de Amazon incompletos.
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Anuncios incompletos

La variable _[!UICONTROL Incomplete]_lista las [!DNL Commerce] catálogo de productos que cumplen los requisitos de elegibilidad de Amazon (definidos en [listar reglas](./listing-rules.md)), pero faltan la información requerida por Amazon (como Amazon ASIN o una condición de producto definida).

Hay cuatro causas posibles de que la lista esté incompleta, cada una de ellas identificada por su estado.

| Estado | Razón | Acción |
|--- |--- |--- |
| Condición que falta | Amazon acepta anuncios en varias condiciones (como _Nuevo_, _Reformado_, _Utilizado: Like New_) requiere una condición definida. | Actualizar la información necesaria y manualmente [asignar una condición](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) a un anuncio. |
| No se puede asignar a la lista de Amazon | Error de coincidencia automática de este anuncio con su catálogo. Si no se encuentra ninguna coincidencia, la Sales Channel de Amazon no puede administrar la lista | Actualizar la información necesaria y manualmente [asignar un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) al producto del catálogo para buscar coincidencias con la lista. |
| Se encontraron varias coincidencias | Error de coincidencia automática de este anuncio con su catálogo. Si se encuentran varias coincidencias posibles, debe seleccionar la coincidencia correcta para el producto. | Actualizar la información necesaria y manualmente [elija una coincidencia de producto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para el producto y la lista. |
| Tiene variantes | Si el producto tiene variantes, como una camiseta disponible en diferentes tamaños o colores, debe elegir la variante del catálogo para que se asigne correctamente y coincida con la lista | Actualizar la información necesaria y manualmente [elija la variante correcta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para asignar y hacer coincidir con este anuncio. |

>[!NOTE]
>Cuando los listados incompletos coinciden correctamente con los productos del catálogo, el listado se mueve del _[!UICONTROL Incomplete]_y se publican en Amazon en función de su [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) configuración.

Las acciones disponibles en la variable _[!UICONTROL Incomplete]_La pestaña incluye:

En _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Elija iniciar el proceso automático para hacer coincidir los datos de sus anuncios de Amazon con su [!DNL Commerce] catálogo. Si los productos no coinciden automáticamente, vuelva a consultar la [_[!UICONTROL Catalog Search]_](./catalog-search.md) opciones de la lista de permitidos. Si los anuncios no coinciden automáticamente después de actualizar su _[!UICONTROL Catalog Search]_, puede hacer coincidir los productos manualmente en la [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) acción.

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL Update Required Info]**: Elija cuándo los anuncios no coinciden automáticamente con su catálogo. Puede [hacer coincidir productos del catálogo con anuncios](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), manualmente [asignar un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) a una coincidencia de catálogo, o [asignar una condición que falta](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para incluirlo en la lista.

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluido el [Registro de actividades de lista](./product-listing-details.md#listing-activity-log), [Precio de la competencia del Buy Box](./product-listing-details.md#buy-box-competitor-pricing)y [Precios de la competencia más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

>[!NOTE]
>
>Si tiene anuncios en curso, el número de anuncios aparece en un mensaje encima de las pestañas.

![Anuncios incompletos de Amazon](assets/amazon-incomplete-listings.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunas [controles del espacio de trabajo](./workspace-controls.md) que permiten personalizar los datos que se muestran.

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa que [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La variable [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio de venta del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado de la lista, definido por Amazon. Consulte la tabla Estado anterior. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y seleccione una opción:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
