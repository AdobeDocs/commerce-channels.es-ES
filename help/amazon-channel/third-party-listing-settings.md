---
title: Anuncios de terceros
description: Actualice la configuración de las listas de terceros para determinar si el catálogo de comercio importa productos de las listas de Amazon Seller Central existentes.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Anuncios de terceros

La configuración de la lista de terceros forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [tablero de almacenamiento](./amazon-store-dashboard.md).

Esta configuración determina si su [!DNL Commerce] el catálogo importa productos de [!DNL Amazon Seller Central] anuncios. Se recomienda importar listados de Amazon para asegurarse de que todos los listados tengan coincidencias [!DNL Commerce] productos. Cuando sus anuncios formen parte de su [!DNL Commerce] , puede administrar todos sus productos desde un único catálogo y utilizar las funciones de canal de ventas de Amazon. Estas funciones incluyen cumplimiento y administración de pedidos con Amazon, revalorización inteligente y administración de cantidades.

Cuando está configurado para importar sus anuncios de Amazon, el canal de ventas de Amazon importa sus anuncios de Amazon en su [!DNL Commerce] catálogo, intentando hacerlos coincidir con productos existentes. Si no se encuentra una coincidencia automáticamente, puede importar la lista de Amazon como una nueva [!DNL Commerce] producto o hacer coincidir manualmente el listado con un producto.

Si decide importar sus listados de Amazon, elija el [!DNL Commerce] atributos con valores para SKU de vendedor de Amazon y Amazon ASIN. Si no tiene [!DNL Commerce] [atributos del producto](./ob-creating-magento-attributes.md), considere la posibilidad de crearlos y asignarlos. Asignar estos atributos ayuda a hacer coincidir correctamente los anuncios de Amazon importados con el [!DNL Commerce] productos.

La importación inicial del listado se inicia cuando [integración de tiendas](./store-integration.md) ha finalizado. Después y en función de la configuración de cron, [!DNL Commerce] comprueba continuamente los listados de Amazon recién añadidos (no creados en la Sales Channel de Amazon) y actualiza su [!DNL Commerce] catálogo según la configuración de anuncios de terceros.

## Configuración de listas de terceros

1. Haga clic en **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda el _[!UICONTROL Third Party Listings]_para obtener más información.

1. Para **[!UICONTROL Import Third Party Listings]** (obligatorio), elija una opción:

   - `Import Listing` - (Predeterminado) Elija cuándo desea que la información del producto de sus anuncios de Amazon se importe en su [!DNL Commerce] catálogo de productos. Esta opción es la predeterminada y se recomienda.

   - `Do Not Import Listing` - Elija cuándo desea manualmente [crear y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} para su [!DNL Commerce] catálogo para sus anuncios de Amazon.
   >[!NOTE]
   >Los campos de opciones siguientes solo están activos cuando se establecen en `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, elija el [!DNL Commerce] que coincida con el valor SKU del vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, elija el [!DNL Commerce] que ha creado y que coincide con Amazon ASIN.

   >[!NOTE]
   >Si no ha creado estos [!DNL Commerce] atributos de sus anuncios de Amazon, consulte [Creación de atributos para la coincidencia de Amazon](./ob-creating-magento-attributes.md).

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Anuncios de terceros](assets/amazon-third-party-listings.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Import Third Party Listings] | Requerido. Opciones:<ul><li>**[!UICONTROL Import Listing]** - (Predeterminado) Elija cuándo desea que la información del producto de sus anuncios de Amazon se importe en su [!DNL Commerce] catálogo de productos. </li><li>**[!UICONTROL Do Not Import Listing]** - Elija cuándo desea manualmente [crear y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} para su [!DNL Commerce] catálogo para sus anuncios de Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Solo activa cuando está configurada en `Import Listing`.<br>Elija la [!DNL Commerce] como una coincidencia con el atributo Amazon para el SKU del vendedor de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia con Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise su [!DNL Commerce] [attributes](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Solo activa cuando está configurada en `Import Listing`.<br>Elija la [!DNL Commerce] que coincida con el atributo Amazon para Amazon ASIN. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia con Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise su [!DNL Commerce] [attributes](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
