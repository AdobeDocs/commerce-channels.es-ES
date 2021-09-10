---
title: Existencias/Cantidad
description: 'Para controlar la sincronización de los detalles de cantidad de producto de su tienda de comercio a su cuenta [!DNL Amazon Seller Central] , actualice la configuración Stock/Quantity.'
redirect_from: /sales-channels/asc/ob-stock-quantity.html: 
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 771
ht-degree: 0%

---

# Existencias/Cantidad

*[!UICONTROL Stock/Quantity]* la configuración forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Estos ajustes se utilizan para sincronizar los detalles de cantidad de producto de su tienda [!DNL Commerce] con la cantidad de su cuenta [!DNL Amazon Seller Central]. Esta herramienta es potente y puede utilizarse para publicidad adicional mostrando urgencia al comprador mientras mantiene organizado su inventario. Por ejemplo, algunos comerciantes pueden tener 150 artículos de un SKU en particular en existencias en su almacén y desean asegurarse de que los compradores de Amazon puedan comprar todo su inventario. Otros comerciantes tal vez deseen enumerar únicamente un elemento a la vez para crear una sensación de escasez para el usuario final. En este caso, establezca el *[!UICONTROL Maximum Listed Quantity]* en `1`.

La cantidad es un atributo regional y se basa en la configuración **[!UICONTROL Amazon Marketplace Country]** definida durante la [integración del almacén](./store-integration.md). Cuando se realiza un cambio en la cantidad de un producto, el cambio afecta a todos los listados de Amazon que comparten ese [!DNL Amazon Seller SKU] en sus tiendas de Amazon que venden en el mismo país. Un cambio en un [!DNL Amazon Seller SKU] compartido en Estados Unidos no afecta a la configuración de sus tiendas de Amazon para un país diferente. El primer almacén de Amazon integrado (con la fecha de creación más antigua) controla la prioridad en la configuración de cantidad.

>[!NOTE]
>
>Para los usuarios de Adobe Commerce y Magento Open Source 2.3.x, el canal de ventas de Amazon admite el uso de la extensión Administración de inventario sin ninguna configuración adicional. Consulte [Administración de inventario](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){:target=&quot;_blank&quot;}.

## Configuración de stock/cantidad {#configure-stock--quantity-settings}

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección **[!UICONTROL Stock / Quantity]** .

1. Para **[!UICONTROL Out-of-Stock Threshold]** (obligatorio), introduzca un valor numérico para la cantidad más baja de un producto para que el producto sea elegible para su lista de Amazon.

   El valor predeterminado es `0`. Si el producto [!DNL Commerce] va por debajo de este número, el anuncio de Amazon correspondiente no es apto para ventas a través de Amazon.

1. Para **[!UICONTROL Maximum Listed Quantity]** (obligatorio), introduzca un valor numérico para la cantidad que desee mostrar en su lista de Amazon.

   Esta configuración enumera todas las listas de Amazon aptas en el valor introducido. Cuando se vende un artículo, la cantidad de Amazon que cotiza no cambia. La cantidad de listado disponible siempre utiliza este valor, incluso cuando la cantidad de producto real es mayor o menor. Esta configuración generalmente se utiliza cuando no se administra el inventario de productos. Por ejemplo, puede tener un producto con una cantidad de 80 en su catálogo [!DNL Commerce]. Con configurado en `10`, el listado de Amazon siempre muestra una cantidad disponible de `10` y no cambia cuando se realiza la venta para el producto.

1. Para **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatorio), introduzca un valor de cantidad para mostrar para sus anuncios de Amazon.

   Amazon requiere que publique una cantidad disponible. Para los productos [!DNL Commerce] que están configurados para no administrar existencias pero desea enumerarlos en Amazon, la lista se publica con la cantidad disponible introducida aquí.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Ajustes de stock/cantidad](assets/amazon-stock-quantity.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Introduzca un valor numérico para la cantidad más baja de un producto con el fin de mantener el producto apto para su lista de Amazon (el valor predeterminado es `0`).<br><br>Si el stock del  [!DNL Commerce] producto es menor que este número, el anuncio de Amazon correspondiente no es apto para ventas a través de Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Introduzca un valor numérico para la cantidad que desea mostrar en la lista de Amazon.<br><br>Cuando se vende un artículo, el anuncio de Amazon se vuelve a publicar con la cantidad introducida aquí. Esta configuración generalmente se utiliza cuando no se administra el inventario de productos.<br><br>Por ejemplo, introduzca el valor Cantidad máxima enumerada como  `10`. La cantidad real de un producto es `80`. Dado que ha establecido este valor en `10`, el listado de Amazon siempre muestra una cantidad disponible de `10`. La cantidad disponible siempre se muestra con el valor definido, incluso cuando la cantidad de existencias es menor. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Introduzca un valor para la cantidad de visualización de sus anuncios de Amazon.<br><br>Amazon requiere que publique una cantidad disponible. Para los productos [!DNL Commerce] que están configurados para no administrar existencias pero desea enumerarlos en Amazon, la lista se publica con la cantidad disponible del valor introducido aquí. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Ejemplo: Cantidad máxima enumerada

Cuando se vende un artículo, el anuncio de Amazon lo vuelve a consultar en esta cantidad.

Por ejemplo, si establece *[!UICONTROL Maximum Listed Quantity]* como `12`, la lista de Amazon muestra una cantidad de 12 aunque el producto tenga una cantidad [!DNL Commerce] de 80:

![Ejemplo 1 de cantidad máxima enumerada](assets/amazon-max-listed-quantity.png)

Si establece su *[!UICONTROL Maximum Listed Quantity]* como `1`, todos los productos aptos se enumeran con una cantidad de `1`. Cuando se vende un artículo, el sistema busca su [!DNL Commerce] producto y, si existe un inventario adicional, confiere el artículo en Amazon con una cantidad de `1`.

Esta opción puede resultar útil para productos que normalmente se solicitan con una cantidad de 1. También aumenta la urgencia del comprador cuando ve su lista de Amazon.

![Ejemplo de cantidad máxima enumerada 2](assets/amazon-max-listed-quantity-1.png)
