---
title: Listados inactivos
description: El canal de ventas de Amazon proporciona la variable [!UICONTROL Inactive] para controlar su estado inactivo [!DNL Amazon Marketplace] anuncios.
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Anuncios inactivos

La variable _[!UICONTROL Inactive]_muestra los productos que se han publicado en Amazon pero que no están activos en [!DNL Amazon Marketplace]. Sus anuncios podrían estar inactivos por varios motivos diferentes. Por ejemplo, es posible que no pueda enumerar esa marca en particular. Los listados inactivos están dictados por los estándares de listado de Amazon y sus [!DNL Amazon Seller Central] permisos de cuenta.

En _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Elija quitar todos los listados seleccionados del [!DNL Amazon Marketplace]. Consulte [Finalización de una lista de Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Elija cambiar la configuración de anulación de la lista. Consulte [Anulaciones](./overrides.md) o [Editar o quitar una anulación](./creating-editing-overrides.md#edit-override-single-listing).

En **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna:

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluido el [Registro de actividades de lista](./product-listing-details.md#listing-activity-log), [Precio de la competencia del Buy Box](./product-listing-details.md#buy-box-competitor-pricing)y [Precios de la competencia más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

- **[!UICONTROL Create Override]**: elija crear una anulación y aplicarla a esta lista. Consulte [Crear una anulación](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: elija modificar el ASIN asignado al producto del catálogo. Esta acción se usa si un producto del catálogo coincide con el ASIN incorrecto. Consulte [Editar ASIN asignado](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: elija crear un SKU de alias (unidad de mantenimiento de existencias) que se pueda usar para crear una lista de Amazon a partir del mismo producto de catálogo. Consulte [Crear un SKU de vendedor de alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: elija cambiar el método de cumplimiento asociado al pedido. Consulte [Configuración de los ajustes Completados por](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: Elija quitar el listado del [!DNL Amazon Marketplace]. Consulte [Finalización de una lista de Amazon](./end-listings-manually.md).

>[!NOTE]
>
>Si tiene anuncios en curso, aparece un mensaje encima de las pestañas que indica el número de anuncios.

![Listas inactivas de Amazon](assets/amazon-inactive-listings.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunas [controles del espacio de trabajo](./workspace-controls.md) que permiten personalizar los datos que se muestran.

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa los números de identificación estándar de Amazon. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La variable [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio de venta del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado de la lista, definido por Amazon. |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazon no siempre proporciona un motivo para los anuncios inactivos y puede ponerse en contacto con el servicio de asistencia al cliente para resolver los problemas relacionados con los anuncios. En algunos casos, Amazon le notifica un motivo. Para ver estas respuestas, haga clic en **[!UICONTROL View Details]** en el _[!UICONTROL Action]_para abrir el Navegador. Si estos problemas se resuelven y Amazon elimina el error, los productos pasan a la sección_[!UICONTROL Active]_ pestaña . |
| Acción | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y seleccione la opción :<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
