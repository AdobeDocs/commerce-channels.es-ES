---
title: Anuncios activos de Amazon
description: El canal de ventas de Amazon proporciona la pestaña Activo para supervisar las listas de Amazon activas que coinciden con un producto del catálogo de Adobe Commerce.
feature: Sales Channels, Products, Merchandising, Catalog Management
exl-id: c9105abc-74d6-442b-8d7a-e5aaea8872e4
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Anuncios activos de Amazon

La ficha _[!UICONTROL Active]_muestra los anuncios activos de [!DNL Amazon Marketplace] que coinciden con un producto del catálogo [!DNL Commerce].

Las acciones disponibles en la ficha _[!UICONTROL Active]_incluyen:

En _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: elige eliminar todos los anuncios seleccionados de [!DNL Amazon Marketplace]. Ver [Finalizar un anuncio de Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: elige cambiar la configuración de anulación del anuncio. Ver [Anulaciones](./overrides.md) o [Editar o quitar una invalidación](./creating-editing-overrides.md#edit-override-single-listing).

En **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_:

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, como el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios para Buy Box de la competencia](./product-listing-details.md#buy-box-competitor-pricing) y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Ver [Ver detalles](./product-listing-details.md).

- **[!UICONTROL Create Override]**: elige crear una invalidación y aplicarla a este anuncio. Ver [Crear una invalidación](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: elija modificar el ASIN asignado al producto del catálogo. Utilice esta acción si un producto del catálogo coincide con el ASIN incorrecto. Consulte [Editar un ASIN asignado](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: elige crear un SKU de alias que se pueda usar para crear un anuncio de Amazon a partir del mismo producto de catálogo. Ver [Crear un SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: elija cambiar el método de cumplimiento asociado al pedido. Ver [Configuración completada por la configuración](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: elija quitar el listado de [!DNL Amazon Marketplace]. Ver [Finalizar un anuncio de Amazon](./end-listings-manually.md).

>[!NOTE]
>
>Si tiene listados en proceso, el número de listados se muestra en un mensaje encima de las pestañas.

![Anuncios activos](assets/amazon-active-listings.png){width="700" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

| Columna | Descripción |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos. <br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible después de que el producto aparezca en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. |
| [!UICONTROL Buy Box Won] | Si la lista de productos ganó la posición de [Buy Box](./buy-box-competitor-pricing.md). |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_para mostrar las opciones:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
