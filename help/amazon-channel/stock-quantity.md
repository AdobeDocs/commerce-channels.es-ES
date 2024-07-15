---
title: 'Sales Channel de Amazon: [!UICONTROL Stock/Quantity]'
description: Para controlar la sincronización de los detalles de cantidad de productos de tu tienda Commerce con tu cuenta de  [!DNL Amazon Seller Central] , actualiza la configuración de Stock/Quantity.
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

La configuración de *[!UICONTROL Stock/Quantity]* forma parte de la configuración del listado de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración se usa para sincronizar los detalles de cantidad de productos de la tienda [!DNL Commerce] con la cantidad de la cuenta [!DNL Amazon Seller Central]. Esta herramienta es potente y se puede utilizar para publicidad adicional mostrando urgencia al comprador mientras mantiene su inventario organizado. Por ejemplo, algunos comerciantes pueden tener 150 artículos de un SKU en particular en existencias en su almacén y desean asegurarse de que los compradores de Amazon puedan comprar todo su inventario. Es posible que otros comerciantes solo deseen enumerar un artículo a la vez para crear una sensación de escasez para el usuario final. En este caso, establezca *[!UICONTROL Maximum Listed Quantity]* en `1`.

La cantidad es un atributo regional y se basa en la configuración de **[!UICONTROL Amazon Marketplace Country]** definida durante la [integración del almacén](./store-integration.md). Cuando se realiza un cambio en la cantidad de un producto, el cambio afecta a todos los anuncios de Amazon que comparten ese(a) [!DNL Amazon Seller SKU] en sus tiendas Amazon que venden en el mismo país. Un cambio en un(a) [!DNL Amazon Seller SKU] compartido(a) en Estados Unidos no afecta la configuración de las tiendas Amazon para un país diferente. La primera tienda Amazon integrada (con la fecha de creación más antigua) controla la prioridad en la configuración de cantidades.

>[!NOTE]
>
>Para los usuarios de Adobe Commerce y Magento Open Source 2.3.x, el canal de ventas de Amazon admite el uso de la extensión de Inventory management sin ninguna configuración adicional. Ver [Administración del inventario](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## Configuración de stock/cantidad {#configure-stock--quantity-settings}

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección **[!UICONTROL Stock / Quantity]**.

1. Para **[!UICONTROL Out-of-Stock Threshold]** (obligatorio), introduzca un valor numérico para la cantidad más baja de un producto a fin de que el producto siga siendo apto para su listado de Amazon.

   El valor predeterminado es `0`. Si el stock de productos de [!DNL Commerce] es menor que este número, el anuncio de Amazon correspondiente no será apto para las ventas a través de Amazon.

1. Para **[!UICONTROL Maximum Listed Quantity]** (obligatorio), introduce un valor numérico para la cantidad que deseas mostrar en tu anuncio de Amazon.

   Esta configuración muestra todos los anuncios de Amazon aptos según el valor introducido. Cuando se vende un artículo, la cantidad del anuncio de Amazon no cambia. La cantidad disponible en el anuncio siempre utiliza este valor, incluso cuando la cantidad real del producto es superior o inferior. Esta configuración se suele utilizar cuando no se administra el inventario de productos. Por ejemplo, puede tener un producto con una cantidad de 80 en el catálogo [!DNL Commerce]. Con establecido en `10`, el anuncio de Amazon siempre muestra una cantidad disponible de `10` y no cambia cuando se realiza la venta del producto.

1. Para **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatorio), introduce un valor de cantidad para mostrar en tus anuncios de Amazon.

   Amazon requiere que publique una cantidad disponible. Para [!DNL Commerce] productos que están configurados para no administrar existencias pero que desea poner en venta en Amazon, el listado se publica con la cantidad disponible ingresada aquí.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Configuración de stock/cantidad](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| Campo | Descripción |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | Escriba un valor numérico para la cantidad más baja de un producto a fin de que el producto siga siendo apto para su listado de Amazon (el valor predeterminado es `0`).<br><br>Si el stock de productos de [!DNL Commerce] es menor que este número, el anuncio de Amazon correspondiente no será apto para las ventas a través de Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Introduce un valor numérico para la cantidad que deseas mostrar en tu anuncio de Amazon.<br><br>Cuando se vende un artículo, el anuncio de Amazon vuelve a publicar con la cantidad introducida aquí. Esta configuración se suele utilizar cuando no se administra el inventario de productos.<br><br>Por ejemplo, escribe el valor Cantidad máxima enumerada como `10`. La cantidad real de un producto es `80`. Dado que ha establecido este valor en `10`, el anuncio de Amazon siempre muestra una cantidad disponible de `10`. La cantidad disponible siempre se muestra con el valor definido, incluso cuando la cantidad de stock sea menor. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Introduce un valor para la cantidad que se muestra en los anuncios de Amazon.<br><br>Amazon requiere que publique una cantidad disponible. Para [!DNL Commerce] productos que están configurados para no administrar existencias pero que desea poner en venta en Amazon, el listado se publica con la cantidad disponible del valor ingresado aquí. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Ejemplo: Cantidad máxima enumerada

Cuando se vende un artículo, el anuncio de Amazon vuelve a ponerlo en venta en esta cantidad.

Por ejemplo, si establece *[!UICONTROL Maximum Listed Quantity]* como `12`, el listado de Amazon muestra una cantidad de 12 aunque el producto tenga una cantidad de [!DNL Commerce] de 80:

![Ejemplo de cantidad máxima enumerada 1](assets/amazon-max-listed-quantity.png){width="300"}

Si establece su *[!UICONTROL Maximum Listed Quantity]* como `1`, todos los productos aptos se enumerarán con una cantidad de `1`. Cuando se vende un artículo, el sistema consulta el producto [!DNL Commerce] y, si existen existencias adicionales, vuelve a poner en venta el artículo en Amazon con una cantidad de `1`.

Esta opción puede ser útil para productos que normalmente se solicitan en una cantidad de 1. También aumenta la urgencia para el comprador al ver su anuncio de Amazon.

![Ejemplo de cantidad máxima enumerada 2](assets/amazon-max-listed-quantity-1.png){width="300"}
