---
title: Anuncios de Amazon no aptos
description: El canal de ventas de Amazon proporciona [!UICONTROL Ineligible] para ayudarte a administrar artículos no se pueden utilizar como anuncio según las reglas actuales.
feature: Sales Channels, Products
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Anuncios de Amazon no aptos

El _[!UICONTROL Ineligible]_Esta pestaña muestra una lista de todos los productos que están publicados actualmente en Amazon, pero que no cumplen los requisitos para aparecer en un anuncio según las reglas actuales. Si un producto anterior era apto y se modifican las reglas de listado para que ahora no sea apto, la cantidad asociada a un producto cae a 0 y el producto se marca como_ inelegible _. Sin embargo, sigue presente en su [!DNL Amazon Seller Account].

Para mover un producto fuera de _[!UICONTROL Ineligible]_pestaña, puede [modificar las reglas del anuncio](./listing-rules.md) para permitir que sus productos sean aptos.

Las acciones disponibles en la _[!UICONTROL Ineligible]_pestaña incluir:

En _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: elige eliminar todos los anuncios seleccionados del [!DNL Amazon Marketplace]. Consulte [Finalizar un anuncio de Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: decide cambiar la configuración de anulación del listado. Consulte [Invalidaciones](./overrides.md) o [Editar o quitar una anulación](./creating-editing-overrides.md#edit-override-single-listing).

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL View Details]**: elige ver los detalles del anuncio, incluido el [Registro de actividades de anuncio](./product-listing-details.md#listing-activity-log), [Precios de competidor Buy Box](./product-listing-details.md#buy-box-competitor-pricing), y [Precios más bajos para competidores](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles del listado. Consulte [Ver detalles](./product-listing-details.md).

- **[!UICONTROL Create Override]**: elige crear una anulación y aplicarla a este anuncio. Consulte [Creación de una anulación](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: modifique el ASIN asignado al producto del catálogo. Esta acción se utiliza si un producto del catálogo coincide con el ASIN incorrecto. Consulte [Editar un ASIN asignado](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: elija crear un SKU de alias que se pueda usar para crear un anuncio de Amazon a partir del mismo producto de catálogo. Consulte [Crear un SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: elija cambiar el método de cumplimiento asociado al pedido. Consulte [Configuración de Satisfecho por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: elige eliminar el listado de [!DNL Amazon Marketplace]. Consulte [Finalizar un anuncio de Amazon](./end-listings-manually.md).

>[!NOTE]
>Si tiene listados en proceso, el número de listados se muestra en un mensaje encima de las pestañas.

![Anuncios de Amazon no aptos](assets/amazon-ineligible-listings.png){width="600" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos elementos comunes [controles de workspace](./workspace-controls.md) que permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa el [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Condition] | El [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio del anuncio del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | Cantidad disponible cuando el producto aparece activamente en la lista de Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y seleccione una opción:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Crear anulación](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
