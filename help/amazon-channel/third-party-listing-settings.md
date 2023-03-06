---
title: Anuncios de terceros
description: Actualice la configuración del anuncio de terceros para determinar si el catálogo de Commerce importa productos de los anuncios existentes de Amazon Seller Central.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Anuncios de terceros

La configuración de anuncios de terceros forma parte de la configuración de anuncios de tiendas. Se accede a la configuración de anuncio desde el [tablero de tienda](./amazon-store-dashboard.md).

Esta configuración determina si su [!DNL Commerce] catálogo importa productos de su existente [!DNL Amazon Seller Central] anuncios. Se recomienda importar los anuncios de Amazon para asegurarse de que todos los anuncios tengan coincidencias [!DNL Commerce] productos. Cuando tus anuncios formen parte de tu [!DNL Commerce] puede administrar todos sus productos desde un único catálogo y utilizar las funciones del canal de ventas de Amazon. Estas funciones incluyen gestión de pedidos y satisfacción de pedidos con Amazon, reasignación inteligente de precios y gestión de cantidades.

Cuando se configura para importar tus anuncios de Amazon, el canal de ventas de Amazon importa tus anuncios de Amazon en tu [!DNL Commerce] catálogo, intentando hacerlos coincidir con productos existentes. Si no encuentra una coincidencia automáticamente, puede importar el anuncio de Amazon como nuevo [!DNL Commerce] o hacer coincidir manualmente la lista con un producto.

Si decide importar los anuncios de Amazon, elija la opción [!DNL Commerce] atributos con valores para Amazon Seller SKU y Amazon ASIN. Si no tiene [!DNL Commerce] [atributos del producto](./ob-creating-magento-attributes.md), considere la posibilidad de crearlos y asignarlos. Asignar estos atributos ayuda a hacer coincidir correctamente los listados de Amazon importados con su [!DNL Commerce] productos.

La importación inicial del listado se inicia cuando [integración de tienda](./store-integration.md) se ha completado. Después y en función de su configuración de cron, [!DNL Commerce] comprueba continuamente los anuncios de Amazon que se acaban de agregar (no creados en la Sales Channel de Amazon) y actualiza su [!DNL Commerce] catálogo según la configuración de anuncios de terceros.

## Configuración de listados de terceros

1. Clic **[!UICONTROL Listing Settings]** en el tablero de la tienda.

1. Expanda el _[!UICONTROL Third Party Listings]_sección.

1. Para **[!UICONTROL Import Third Party Listings]** (obligatorio), elija una opción:

   - `Import Listing` - (Predeterminado) Elige cuándo quieres que la información de los productos de tus anuncios de Amazon se importe en tu [!DNL Commerce] catálogo de productos. Esta opción es la predeterminada y se recomienda.

   - `Do Not Import Listing` - Elige cuándo quieres hacerlo manualmente [crear y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} a su [!DNL Commerce] para tus anuncios de Amazon.
   >[!NOTE]
   >Los siguientes campos de opciones solo están activos cuando se establece en `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, elija la [!DNL Commerce] que coincida con el valor SKU del vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, elija la [!DNL Commerce] que ha creado y que coincide con el ASIN de Amazon.

   >[!NOTE]
   >Si no ha creado estos [!DNL Commerce] atributos de los anuncios de Amazon, consulte [Creación de atributos para la coincidencia de Amazon](./ob-creating-magento-attributes.md).

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Anuncios de terceros](assets/amazon-third-party-listings.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Import Third Party Listings] | Requerido. Opciones:<ul><li>**[!UICONTROL Import Listing]** - (Predeterminado) Elige cuándo quieres que la información de los productos de tus anuncios de Amazon se importe en tu [!DNL Commerce] catálogo de productos. </li><li>**[!UICONTROL Do Not Import Listing]** - Elige cuándo quieres hacerlo manualmente [crear y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} a su [!DNL Commerce] para tus anuncios de Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Solo está activo cuando se establece en `Import Listing`.<br>Elija la [!DNL Commerce] coincide con el atributo de Amazon para el SKU del vendedor de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia de Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise su [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Solo está activo cuando se establece en `Import Listing`.<br>Elija la [!DNL Commerce] que coincide con el atributo de Amazon para el ASIN de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia de Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise su [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
