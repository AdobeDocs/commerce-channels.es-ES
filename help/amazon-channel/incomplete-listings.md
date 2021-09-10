---
title: Listas incompletas
description: El canal de ventas de Amazon proporciona la pestaña [!UICONTROL Incomplete] para ayudarle a identificar y cumplir los requisitos de elegibilidad para sus anuncios de Amazon incompletos.
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Anuncios incompletos

La pestaña _[!UICONTROL Incomplete]_enumera los [!DNL Commerce] productos de catálogo que cumplen con los requisitos de elegibilidad de Amazon (definidos en las [reglas de listado](./listing-rules.md)), pero que carecen de la información requerida por Amazon (como Amazon ASIN o una condición de producto definida).

Hay cuatro causas posibles de que la lista esté incompleta, cada una de ellas identificada por su estado.

| Estado | Razón | Acción |
|--- |--- |--- |
| Condición que falta | Amazon acepta anuncios en varias condiciones (como _New_, _Refacshed_, _Utilizado: Como nuevo_) requiere una condición definida. | Actualice la información necesaria y asigne manualmente [una condición](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) a una lista. |
| No se puede asignar a la lista de Amazon | Error de coincidencia automática de este anuncio con su catálogo. Si no se encuentra ninguna coincidencia, la Sales Channel de Amazon no puede administrar la lista | Actualice la información necesaria y asigne manualmente [un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) al producto del catálogo para que coincida con el listado. |
| Se encontraron varias coincidencias | Error de coincidencia automática de este anuncio con su catálogo. Si se encuentran varias coincidencias posibles, debe seleccionar la coincidencia correcta para el producto. | Actualice la información necesaria y [elija manualmente una coincidencia de producto](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) para el producto y la lista. |
| Tiene variantes | Si el producto tiene variantes, como una camiseta disponible en diferentes tamaños o colores, debe elegir la variante del catálogo para que se asigne correctamente y coincida con la lista | Actualice la información necesaria y [elija manualmente la variante correcta](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) para asignar y hacer coincidir con esta lista. |

>[!NOTE]
>Cuando las listas incompletas coinciden correctamente con los productos del catálogo, la lista se mueve de la pestaña _[!UICONTROL Incomplete]_y se publica en Amazon según la configuración de [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md).

Las acciones disponibles en la pestaña _[!UICONTROL Incomplete]_incluyen:

En _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Elija iniciar el proceso automático para hacer coincidir los datos de Amazon listings con el  [!DNL Commerce] catálogo. Si los productos no coinciden automáticamente, vuelva a las opciones [_[!UICONTROL Catalog Search]_](./catalog-search.md) de las listas de permitidos. Si las listas no coinciden automáticamente después de actualizar las opciones de _[!UICONTROL Catalog Search]_, puede hacer coincidir los productos manualmente en la acción [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found).

En **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_:

- **[!UICONTROL Update Required Info]**: Elija cuándo los anuncios no coinciden automáticamente con su catálogo. Puede [hacer coincidir manualmente los productos del catálogo con los listados](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), [asignar un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) a una coincidencia del catálogo, o [asignar una condición que falta](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) para la inclusión en la lista.

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluidos el registro de actividades de  [anuncio](./product-listing-details.md#listing-activity-log), los precios [ de la competencia del ](./product-listing-details.md#buy-box-competitor-pricing)Buy Box y los precios de la competencia  [más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

>[!NOTE]
>
>Si tiene anuncios en curso, el número de anuncios aparece en un mensaje encima de las pestañas.

![Anuncios incompletos de Amazon](assets/amazon-incomplete-listings.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio de venta del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado de la lista, definido por Amazon. Consulte la tabla Estado anterior. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y seleccione una opción:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
