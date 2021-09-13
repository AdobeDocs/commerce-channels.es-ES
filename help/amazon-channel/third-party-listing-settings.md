---
title: Anuncios de terceros
description: Actualice la configuración de las listas de terceros para determinar si el catálogo de comercio importa productos de las listas de Amazon Seller Central existentes.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Anuncios de terceros

La configuración de la lista de terceros forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Esta configuración determina si el catálogo de [!DNL Commerce] importa productos de los listados de [!DNL Amazon Seller Central] existentes. Se recomienda importar listados de Amazon para garantizar que todos los listados tengan productos [!DNL Commerce] coincidentes. Cuando sus anuncios forman parte de su catálogo [!DNL Commerce], puede administrar todos sus productos desde un único catálogo y utilizar las funciones de canal de ventas de Amazon. Estas funciones incluyen cumplimiento y administración de pedidos con Amazon, revalorización inteligente y administración de cantidades.

Cuando está configurado para importar sus listados de Amazon, el canal de ventas de Amazon importa sus listados de Amazon en su catálogo [!DNL Commerce], intentando hacerlos coincidir con los productos existentes. Si no se encuentra una coincidencia automáticamente, puede importar la lista de Amazon como un nuevo producto [!DNL Commerce] o hacer coincidir manualmente la lista con un producto.

Si decide importar sus anuncios de Amazon, elija los atributos [!DNL Commerce] con valores para el SKU del vendedor de Amazon y el ASIN de Amazon. Si no tiene [!DNL Commerce] [atributos de producto](./ob-creating-magento-attributes.md), considere la posibilidad de crearlos y asignarlos. Asignar estos atributos ayuda a hacer coincidir correctamente los listados de Amazon importados con sus productos [!DNL Commerce].

La importación inicial del listado se inicia cuando se completa la [integración del almacén](./store-integration.md). Después, y en función de la configuración de cron, [!DNL Commerce] comprueba continuamente los listados de Amazon recién agregados (no creados en la Sales Channel de Amazon) y actualiza su catálogo [!DNL Commerce] según la configuración de los listados de terceros.

## Configuración de listas de terceros

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección _[!UICONTROL Third Party Listings]_.

1. Para **[!UICONTROL Import Third Party Listings]** (obligatorio), elija una opción:

   - `Import Listing` - (Predeterminado) Elija cuándo desea que la información del producto de sus listados de Amazon se importe a su catálogo de  [!DNL Commerce] productos. Esta opción es la predeterminada y se recomienda.

   - `Do Not Import Listing` - Elija cuándo desea  [crear manualmente y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;} a su  [!DNL Commerce] catálogo para sus anuncios de Amazon.
   >[!NOTE]
   >Los campos de opciones siguientes solo están activos cuando se establecen en `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, elija el atributo [!DNL Commerce] que coincida con el valor SKU del vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, elija el atributo [!DNL Commerce] que ha creado y haga coincidir con el Amazon ASIN.

   >[!NOTE]
   >Si no ha creado estos atributos [!DNL Commerce] para sus listas de Amazon, consulte [Creación de atributos para la coincidencia con Amazon](./ob-creating-magento-attributes.md).

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Anuncios de terceros](assets/amazon-third-party-listings.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Import Third Party Listings] | Requerido. Opciones:<ul><li>**[!UICONTROL Import Listing]** - (Predeterminado) Elija cuándo desea que la información del producto de sus listados de Amazon se importe a su catálogo de  [!DNL Commerce] productos. </li><li>**[!UICONTROL Do Not Import Listing]** - Elija cuándo desea  [crear manualmente y asignar nuevos productos](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;} a su  [!DNL Commerce] catálogo para sus anuncios de Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Solo activa cuando se establece en `Import Listing`.<br>Elija el  [!DNL Commerce] atributo como una coincidencia con el atributo Amazon para el SKU del vendedor de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia con Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise sus [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Solo activa cuando se establece en `Import Listing`.<br>Elija el  [!DNL Commerce] atributo que coincida con el atributo Amazon para Amazon ASIN. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia con Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise sus [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
