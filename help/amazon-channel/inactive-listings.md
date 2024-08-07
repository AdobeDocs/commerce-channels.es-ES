---
title: Anuncios de Amazon inactivos
description: El canal de ventas de Amazon proporciona la ficha [!UICONTROL Inactive] para supervisar tus anuncios actualmente inactivos [!DNL Amazon Marketplace] 1.
feature: Sales Channels, Products
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Anuncios de Amazon inactivos

La ficha _[!UICONTROL Inactive]_muestra los productos que se han publicado en Amazon pero que no están activos en [!DNL Amazon Marketplace]. Tus anuncios podrían estar inactivos por distintos motivos. Por ejemplo, es posible que no pueda incluir en la lista esa marca en particular. Los anuncios inactivos están determinados por los estándares de anuncios de Amazon y los permisos de la cuenta [!DNL Amazon Seller Central].

En _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: elige eliminar todos los anuncios seleccionados de [!DNL Amazon Marketplace]. Ver [Finalizar un anuncio de Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: elige cambiar la configuración de anulación del anuncio. Ver [Anulaciones](./overrides.md) o [Editar o quitar una invalidación](./creating-editing-overrides.md#edit-override-single-listing).

En **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_:

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, como el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios para Buy Box de la competencia](./product-listing-details.md#buy-box-competitor-pricing) y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Ver [Ver detalles](./product-listing-details.md).

- **[!UICONTROL Create Override]**: elige crear una invalidación y aplicarla a este anuncio. Ver [Crear una invalidación](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: elija modificar el ASIN asignado al producto del catálogo. Esta acción se utiliza si un producto del catálogo coincide con el ASIN incorrecto. Consulte [Editar un ASIN asignado](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: elija crear un SKU de alias (unidad de stock) que se pueda usar para crear un listado de Amazon a partir del mismo producto de catálogo. Ver [Crear un SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: elija cambiar el método de cumplimiento asociado al pedido. Ver [Configuración completada por la configuración](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: elija quitar el listado de [!DNL Amazon Marketplace]. Ver [Finalizar un anuncio de Amazon](./end-listings-manually.md).

>[!NOTE]
>
>Si tiene listados en proceso, aparece un mensaje sobre las pestañas indicando el número de listados.

![Anuncios de Amazon inactivos](assets/amazon-inactive-listings.png){width="600" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

| Columna | Descripción |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa los números de identificación estándar de Amazon. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Status] | El estado del listado, definido por Amazon. |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazon no siempre proporciona un motivo para anuncios inactivos y puedes ponerte en contacto con Atención al cliente para resolver los problemas de los anuncios. En algunos casos, Amazon le notifica un motivo. Para ver estas respuestas, haga clic en **[!UICONTROL View Details]** en la columna _[!UICONTROL Action]_. Si se resuelven estos problemas y Amazon elimina el error, los productos pasan a la ficha_[!UICONTROL Active]_. |
| Acción | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y seleccione la opción:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
