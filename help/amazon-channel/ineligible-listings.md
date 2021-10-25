---
title: Anuncios no elegibles
description: El canal de ventas de Amazon proporciona la variable [!UICONTROL Ineligible] para ayudarle a administrar los elementos no se pueden usar como listado basado en las reglas de listado actuales.
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Anuncios no aptos

La variable _[!UICONTROL Ineligible]_muestra una lista de todos los productos que están actualmente publicados en Amazon pero que no son aptos para entrar en la lista en función de las reglas de la lista actual. Si un producto anterior era elegible y se modifican las reglas de inclusión para que ahora sea inelegible, la cantidad asociada a un producto cae a 0 y el producto se marca como_ inelegible _. Sin embargo, sigue presente en su [!DNL Amazon Seller Account].

Para sacar un producto de _[!UICONTROL Ineligible]_, puede [modificar las reglas de listado](./listing-rules.md) para permitir que sus productos sean elegibles.

Las acciones disponibles en la variable _[!UICONTROL Ineligible]_La pestaña incluye:

En _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Elija quitar todos los listados seleccionados del [!DNL Amazon Marketplace]. Consulte [Finalización de una lista de Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Elija cambiar la configuración de anulación de la lista. Consulte [Anulaciones](./overrides.md) o [Editar o quitar una anulación](./creating-editing-overrides.md#edit-override-single-listing).

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluido el [Registro de actividades de lista](./product-listing-details.md#listing-activity-log), [Precio de la competencia del Buy Box](./product-listing-details.md#buy-box-competitor-pricing)y [Precios de la competencia más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

- **[!UICONTROL Create Override]**: elija crear una anulación y aplicarla a esta lista. Consulte [Crear una anulación](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: elija modificar el ASIN asignado al producto del catálogo. Esta acción se usa si un producto del catálogo coincide con el ASIN incorrecto. Consulte [Editar ASIN asignado](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: elija crear un SKU de alias que se pueda usar para crear una lista de Amazon a partir del mismo producto de catálogo. Consulte [Crear un SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: elija cambiar el método de cumplimiento asociado al pedido. Consulte [Configuración de los ajustes Completados por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: Elija quitar el listado del [!DNL Amazon Marketplace]. Consulte [Finalización de una lista de Amazon](./end-listings-manually.md).

>[!NOTE]
>Si tiene anuncios en curso, el número de anuncios se muestra en un mensaje encima de las pestañas.

![Anuncios de Amazon no aptos](assets/amazon-ineligible-listings.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunas [controles del espacio de trabajo](./workspace-controls.md) que permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa que [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La variable [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio de venta del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y seleccione una opción:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Crear anulación](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
