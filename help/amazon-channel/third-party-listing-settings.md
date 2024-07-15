---
title: 'Sales Channel de Amazon: [!UICONTROL Third-party Listings]'
description: Actualice la configuración de anuncios de terceros para determinar si el catálogo de Commerce importa productos de los anuncios existentes de Amazon Seller Central.
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

La configuración de anuncios de terceros forma parte de la configuración de anuncios de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración determina si el catálogo [!DNL Commerce] importa productos de los listados de [!DNL Amazon Seller Central] existentes. Se recomienda importar los listados de Amazon para asegurarse de que todos los listados tengan [!DNL Commerce] productos que coincidan. Si los anuncios forman parte del catálogo [!DNL Commerce], puede administrar todos los productos desde un único catálogo y utilizar las características del canal de ventas de Amazon. Estas funciones incluyen gestión de pedidos y satisfacción de pedidos con Amazon, reasignación inteligente de precios y gestión de cantidades.

Cuando se configura para importar los anuncios de Amazon, el canal de ventas de Amazon importa los anuncios de Amazon en el catálogo [!DNL Commerce] e intenta hacerlos coincidir con los productos existentes. Si no se encuentra una coincidencia automáticamente, puede importar el listado de Amazon como un nuevo producto de [!DNL Commerce] o hacer coincidir manualmente el listado con un producto.

Si decides importar tus anuncios de Amazon, elige los atributos de [!DNL Commerce] con valores para el SKU del vendedor de Amazon y el ASIN de Amazon. Si no tiene [!DNL Commerce] [atributos de producto](./ob-creating-magento-attributes.md), considere la posibilidad de crearlos y asignarlos. Asignar estos atributos ayuda a hacer coincidir correctamente los listados de Amazon importados con los productos de [!DNL Commerce].

La importación inicial del listado se inicia cuando [se completa la integración de la tienda](./store-integration.md). Después, y en función de la configuración de cron, [!DNL Commerce] comprueba de forma continua los anuncios de Amazon que se acaban de agregar (no se han creado en la Sales Channel de Amazon) y actualiza el catálogo [!DNL Commerce] según la configuración de anuncios de terceros.

## Configuración de listados de terceros

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección _[!UICONTROL Third Party Listings]_.

1. Para **[!UICONTROL Import Third Party Listings]** (obligatorio), elija una opción:

   - `Import Listing` - (Predeterminado) Elija cuándo desea que la información de productos de sus listados de Amazon se importe en su catálogo de productos [!DNL Commerce]. Esta opción es la predeterminada y se recomienda.

   - `Do Not Import Listing`: elige cuándo quieres [crear y asignar manualmente nuevos productos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) a tu catálogo [!DNL Commerce] para tus anuncios de Amazon.

   >[!NOTE]
   >Los siguientes campos de opciones solo están activos cuando se establecen en `Import Listing`.

1. Para **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, elige el atributo [!DNL Commerce] que coincida con el valor de SKU del vendedor de Amazon.

1. Para **[!UICONTROL Attribute That Contains Amazon ASIN]**, elija el atributo [!DNL Commerce] que ha creado y haga coincidir con el ASIN de Amazon.

   >[!NOTE]
   >Si no creó estos atributos de [!DNL Commerce] para sus anuncios de Amazon, consulte [Creación de atributos para la coincidencia de Amazon](./ob-creating-magento-attributes.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Anuncios de terceros](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | Requerido. Opciones:<ul><li>**[!UICONTROL Import Listing]** - (Predeterminado) Elija cuándo desea que la información de productos de sus listados de Amazon se importe en su catálogo de productos [!DNL Commerce]. </li><li>**[!UICONTROL Do Not Import Listing]**: elige cuándo quieres [crear y asignar manualmente nuevos productos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) a tu catálogo [!DNL Commerce] para tus anuncios de Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Solo está activo cuando se establece en `Import Listing`.<br>Elige el atributo [!DNL Commerce] como una coincidencia con el atributo Amazon para el SKU del vendedor de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia de Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise sus [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Solo está activo cuando se establece en `Import Listing`.<br>Elija el atributo [!DNL Commerce] que coincida con el atributo Amazon para el ASIN de Amazon. Si este atributo no existe, consulte [Creación de atributos de producto de Amazon para la coincidencia de Amazon](./ob-creating-magento-attributes.md). Si es necesario, revise sus [!DNL Commerce] [atributos](./managing-attributes.md) y cree o edite un atributo para que coincida con estos datos de Amazon. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
