---
title: Buscar en el catálogo
description: Para establecer la coincidencia de atributos que ayuda a asignar los productos aptos del catálogo de comercio con los listados de Amazon, actualice la configuración de Búsqueda en catálogo.
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# Buscar en el catálogo

_La_ configuración de búsqueda en el catálogo forma parte de la configuración de la lista de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Esta configuración le permite establecer coincidencias de atributos que le ayudarán a asignar productos [!DNL Commerce] aptos con las listas de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

La definición de estos valores de asignación aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de coincidir manualmente con las listas de productos. Si agrega los atributos como parte de sus [Tareas previas a la configuración](./amazon-pre-setup-tasks.md), el canal de ventas de Amazon tiene un mayor potencial para hacer coincidir automáticamente sus productos durante la incorporación y sincronización de datos de productos entre Amazon y [!DNL Commerce].

Si solo crea el atributo Amazon ASIN (sin añadir valores ASIN por producto), es posible que los productos [!DNL Commerce] no coincidan automáticamente con los listados de Amazon. Puede [asignar](./creating-assigning-catalog-products.md) manualmente sus productos. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si ha hecho coincidir manualmente un producto y desea actualizar un elemento de datos ASIN, UPC u otro para el producto, debe actualizar los datos en dos lugares. Actualícelo en su catálogo [!DNL Commerce] y en su listado de Amazon en su cuenta [!DNL Amazon Seller Central].

Se recomienda asignar estos atributos y valores si están disponibles. No es necesario completar esta asignación, pero es beneficioso para la coincidencia de productos y es necesario para una sincronización de catálogos adecuada entre Amazon y [!DNL Commerce].

Si desea agregar atributos, consulte [Crear atributos de producto para la coincidencia con Amazon](./ob-creating-magento-attributes.md).

## Configuración de [!UICONTROL Catalog Search]

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección _[!UICONTROL Catalog Search]_.

1. Para **[!UICONTROL ASIN]**, elija el atributo de producto que ha creado para el valor Amazon ASIN.

   Un ASIN ([!DNL Amazon Standard Identification Number]) es un bloque único de diez letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo.

1. Para **[!UICONTROL EAN]**, elija el atributo de producto que ha creado para el valor EAN de Amazon.

   El número de artículo europeo (EAN) es una norma de código de barras, un código de identificación de producto de 12 o 13 dígitos. Cada EAN identifica de forma exclusiva el producto, el fabricante y sus atributos; normalmente, el EAN se imprime en una etiqueta de producto o en un embalaje como código de barras. Amazon requiere códigos EAN para mejorar la calidad de los resultados de búsqueda y la calidad del catálogo. Puede obtener EAN del fabricante.

1. Para **[!UICONTROL GCID]**, elija el atributo de producto que ha creado para el valor GCIN de Amazon.

   El identificador de catálogo global (GCID) es un ID para productos que no tienen un código UPC o ISBN. El registro de marca de Amazon le permite registrarse como propietario de una marca y crear un ID único para los productos.

1. Para **[!UICONTROL ISBN]**, elija el atributo de producto que ha creado para el valor ISBN de Amazon.

   El Número Internacional Estándar de Libros (ISBN) es un código de barras único del identificador de libros comerciales. Cada código ISBN identifica exclusivamente un libro. Un ISBN tiene diez o 13 dígitos. Todos los ISBN asignados después del 1 de enero de 2007 tienen 13 dígitos.

1. Para **[!UICONTROL UPC]**, elija el atributo de producto que ha creado para el valor UPC de Amazon.

   El Código de producto universal (UPC) es un código de barras de 12 dígitos que se utiliza ampliamente para el empaquetado minorista en Estados Unidos.

1. Para **[!UICONTROL General Search]**, elija el atributo de producto que desea usar para una coincidencia de búsqueda general.

   Este atributo es uno que puede seleccionar para relacionar productos [!DNL Commerce] con la lista de Amazon correspondiente. La búsqueda general utiliza búsquedas de palabras clave del catálogo. Como tal, se recomienda utilizar un atributo [!DNL Commerce] que lleve palabras clave relevantes, como el SKU del producto o el nombre del producto. La búsqueda general puede devolver muchas coincidencias posibles y, en estos casos, puede seleccionar la lista de Amazon adecuada entre las posibles coincidencias. Una selección común para este campo es `Product Name`.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Buscar en el catálogo](assets/amazon-catalog-search.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa  [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL EAN (European Article Number)] | Código de identificación del producto de 12 o 13 dígitos. El número de artículo europeo (EAN) es una norma de código de barras, un código de identificación de producto de 12 o 13 dígitos. Cada EAN identifica de forma exclusiva el producto, el fabricante y sus atributos; normalmente, el EAN se imprime en una etiqueta de producto o en un embalaje como código de barras. Amazon requiere códigos EAN para mejorar la calidad de los resultados de búsqueda y la calidad del catálogo. Puede obtener EAN del fabricante. |
| [!UICONTROL GCID (Global Catalog Identifier)] | El identificador de catálogo global (GCID) es un ID para productos que no tienen un código UPC o ISBN. El Registro de marcas de Amazon le permite registrarse como propietario de una marca y crear un ID único para productos que pueden no tener un UPC o ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | Un código de barras de identificador de libro comercial único de 10 o 13 dígitos. El Número Internacional Estándar de Libros (ISBN) es un código de barras único del identificador de libros comerciales. Cada código ISBN identifica exclusivamente un libro. Un ISBN tiene diez o 13 dígitos. Todos los ISBN asignados después del 1 de enero de 2007 tienen 13 dígitos. |
| UPC (código de producto universal) | Código de barras de 12 dígitos. El Código de producto universal (UPC) es un código de barras de 12 dígitos que se utiliza ampliamente para el empaquetado minorista en Estados Unidos. |
| [!UICONTROL General Search] | Seleccione un atributo. Este atributo es uno que puede seleccionar para relacionar productos [!DNL Commerce] con la lista de Amazon correspondiente. La búsqueda general utiliza búsquedas de palabras clave del catálogo. Como tal, se recomienda utilizar un atributo [!DNL Commerce] que lleve palabras clave relevantes, como el SKU del producto o el nombre del producto. La búsqueda general puede devolver muchas coincidencias posibles y, en estos casos, puede seleccionar la lista de Amazon adecuada entre las posibles coincidencias. Una selección común para este campo es `Product Name`. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
