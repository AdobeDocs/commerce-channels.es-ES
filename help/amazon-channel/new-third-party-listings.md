---
title: Nuevos anuncios de Amazon de terceros
description: Administre nuevos anuncios de Amazon asignándolos a un producto del catálogo de Commerce.
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Nuevos anuncios de Amazon de terceros

La ficha _[!UICONTROL New Third Party]_muestra los anuncios existentes de Amazon que no coinciden con ningún producto del catálogo [!DNL Commerce]. Para usar la administración de listados para cantidad, precios, tiempo de manipulación y mucho más, cada uno de los listados de Amazon debe coincidir (asignarse) con un producto del catálogo [!DNL Commerce]. Existen varias opciones para asignar un anuncio a un producto del catálogo [!DNL Commerce].

En _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**: elige usar la información de la lista de Amazon para crear automáticamente un producto en tu catálogo [!DNL Commerce]. Este proceso hace coincidir automáticamente el listado de Amazon con el nuevo producto del catálogo. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**: elige intentar la coincidencia automática de los anuncios seleccionados con el catálogo en función de las opciones actuales de [Búsqueda en el catálogo](./catalog-search.md) en la configuración del anuncio. Si modifica las opciones de _[!UICONTROL Catalog Search]_, esta acción le permite volver a intentar el proceso de coincidencia.

En _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**: elige hacer coincidir manualmente el anuncio con un producto del catálogo [!DNL Commerce]. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**: elige usar la información de la lista de Amazon para crear automáticamente un producto en tu catálogo [!DNL Commerce]. Este proceso hace coincidir automáticamente el listado de Amazon con el nuevo producto del catálogo. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, como el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios para Buy Box de la competencia](./product-listing-details.md#buy-box-competitor-pricing) y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Ver [Ver detalles](./product-listing-details.md).

>[!NOTE]
>
>Si tiene listados en proceso, aparece un mensaje sobre las pestañas indicando el número de listados.

![Nuevos anuncios de terceros](assets/amazon-listings-new-third-party.png){width="600" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Listing Price] | Identifica el precio de listado del artículo, tal como se define en el origen de precios y en cualquier regla de precios aplicable. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y elija una opción:<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
