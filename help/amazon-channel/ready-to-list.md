---
title: Listo para la lista
description: El canal de ventas de Amazon proporciona la pestaña Listo para lista para ayudarle a revisar los productos de comercio que cumplen los requisitos pero que no aparecen automáticamente en la lista.
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

La pestaña _[!UICONTROL Ready to List]_muestra los productos de catálogo de [!DNL Commerce] que cumplen la configuración de la lista y están listos para publicarse en Amazon como una lista **nueva**. A diferencia de otras pestañas de lista, esta pestaña no siempre aparece en la página [_[!UICONTROL Product Listings]_](./managing-product-listings.md).

La pestaña _[!UICONTROL Ready to List]_solo aparece cuando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) en la configuración de la lista está configurada como `Do Not Automatically List Eligible Products`. Esta configuración indica al canal de ventas de Amazon que cualquier anuncio nuevo de Amazon debe publicarse manualmente.

Cuando [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) está establecido en `Automatically List Eligible Products`, el canal de ventas de Amazon publica automáticamente nuevos listados para sus productos de catálogo aptos. Como las nuevas listas se publican automáticamente, no se muestra la pestaña _[!UICONTROL Ready to List]_.

En _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: Elija volver a publicar el listado en  [!DNL Amazon Marketplace]. Consulte [Publicación de una lista de Amazon](./publish-listings-manually.md)

En **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_:

- **[!UICONTROL Publish On Amazon]**: Elija volver a publicar el listado en  [!DNL Amazon Marketplace]. Consulte [Publicación de una lista de Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: elija ver los detalles de la lista, incluidos el registro de actividades de  [anuncio](./product-listing-details.md#listing-activity-log), los precios [ de la competencia del ](./product-listing-details.md#buy-box-competitor-pricing)Buy Box y los precios de la competencia  [más bajos](./product-listing-details.md#lowest-competitor-pricing). Esta acción es solo para ver. No se pueden realizar cambios en los detalles de la lista. Consulte [Ver detalles](./product-listing-details.md).

Tiene algunas opciones para publicar manualmente [un nuevo listado en Amazon](./publish-listings-manually.md).

>[!NOTE]
>Si tiene anuncios en curso, el número de anuncios se muestra en un mensaje encima de las pestañas.

![Listo para la lista](assets/amazon-ready-to-list.png)

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Condition] | La [condición](./product-listing-condition.md) del producto. |
| [!UICONTROL Landed Price] | El precio de venta del producto más su precio de envío. |
| [!UICONTROL Amazon Quantity] | La cantidad disponible cuando el producto aparece en la lista activa de Amazon. |
| [!UICONTROL Status] | El estado de la lista, definido por Amazon. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y elija una opción:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causas comunes de los listados de Listo para Lista

- **[!UICONTROL Ready to List]** : El producto coincide con un Amazon ASIN y está programado para su inclusión en la lista. Si [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) en la configuración de la lista está configurada en `Do Not Automatically List Eligible Products`, este estado representa los productos que están listos para aparecer en la lista manualmente.

- **[!UICONTROL List in Progress]** - La lista de productos se ha enviado a Amazon y está a la espera de que Amazon confirme su aceptación.
