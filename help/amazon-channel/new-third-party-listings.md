---
title: Nuevos anuncios de terceros
description: Administre nuevos listados de Amazon emparejándolos con un producto de su catálogo de comercio.
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Nuevos anuncios de terceros

La variable _[!UICONTROL New Third Party]_muestra los anuncios de Amazon existentes que no coinciden con ningún producto de su [!DNL Commerce] catálogo. Para usar la administración de listados en cantidad, precio, tiempo de manejo, etc., cada uno de sus listados de Amazon debe coincidir (asignarse) con un producto de su [!DNL Commerce] catálogo. Tiene algunas opciones para asignar una lista a un producto de su [!DNL Commerce] catálogo.

En _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**: Elija utilizar la información de la lista de Amazon para crear automáticamente un producto en su [!DNL Commerce] catálogo. Este proceso hace coincidir automáticamente el listado de Amazon con el nuevo producto de catálogo. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**: Elija intentar la coincidencia automática para los anuncios seleccionados en su catálogo en función de su [Buscar en el catálogo](./catalog-search.md) en la configuración de la lista. Si modifica su _[!UICONTROL Catalog Search]_, esta acción le permite volver a intentar el proceso coincidente.

En _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**: Elija que el listado coincida con un producto de su [!DNL Commerce] catálogo de forma manual. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**: Elija utilizar la información de la lista de Amazon para crear automáticamente un producto en su [!DNL Commerce] catálogo. Este proceso hace coincidir automáticamente el listado de Amazon con el nuevo producto de catálogo. Consulte [Crear y asignar productos de catálogo](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluido el [Registro de actividades de lista](./product-listing-details.md#listing-activity-log), [Precio de la competencia del Buy Box](./product-listing-details.md#buy-box-competitor-pricing)y [Precios de la competencia más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

>[!NOTE]
>
>Si tiene anuncios en curso, aparece un mensaje encima de las pestañas que indica el número de anuncios.

![Nuevos anuncios de terceros](assets/amazon-listings-new-third-party.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunas [controles del espacio de trabajo](./workspace-controls.md) que permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa que [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La variable [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Listing Price] | Identifica el precio del anuncio para el artículo, tal como se define en la fuente de precios y en cualquier regla de precios aplicable. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado de la lista, definido por Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y elija una opción:<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
