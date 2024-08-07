---
title: Buscar en el catálogo anuncios de Amazon
description: Para establecer la coincidencia de atributos que ayuda a asignar productos de catálogo Commerce aptos con listas de Amazon, actualice la configuración de Búsqueda en el catálogo.
feature: Sales Channels, Search, Catalog Management, Products, Configuration
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# Buscar en el catálogo anuncios de Amazon

La configuración de _Búsqueda en el catálogo_ forma parte de la configuración de tu anuncio de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración le permite establecer coincidencias de atributos que ayuden a asignar los productos aptos de [!DNL Commerce] con los listados de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

La definición de estos valores de asignación aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de hacer coincidir manualmente las listas de productos. Si agrega los atributos como parte de sus [tareas previas a la configuración](./amazon-pre-setup-tasks.md), el canal de ventas de Amazon tiene un mayor potencial para hacer coincidir automáticamente sus productos durante la incorporación y sincroniza los datos de productos entre Amazon y [!DNL Commerce].

Si solo crea el atributo ASIN de Amazon (sin agregar valores ASIN por producto), es posible que los productos [!DNL Commerce] no coincidan automáticamente con los listados de Amazon. Puedes [asignar manualmente](./creating-assigning-catalog-products.md) tus productos. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si coincide manualmente con un producto y desea actualizar un ASIN, UPC u otro elemento de datos para el producto, debe actualizar los datos en dos lugares. Actualízalo en tu catálogo [!DNL Commerce] y en tu anuncio de Amazon en tu cuenta de [!DNL Amazon Seller Central].

Se recomienda asignar estos atributos y valores si están disponibles. No es necesario completar esta asignación, pero resulta beneficioso para la coincidencia de productos y es necesario para la sincronización de catálogos adecuada entre Amazon y [!DNL Commerce].

Si desea agregar atributos, consulte [Crear atributos de producto para la coincidencia de Amazon](./ob-creating-magento-attributes.md).

## Configurar la configuración de [!UICONTROL Catalog Search]

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección _[!UICONTROL Catalog Search]_.

1. Para **[!UICONTROL ASIN]**, elija el atributo de producto que creó para el valor ASIN de Amazon.

   Un ASIN ([!DNL Amazon Standard Identification Number]) es un bloque único de diez letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo.

1. Para **[!UICONTROL EAN]**, elija el atributo de producto que creó para el valor EAN de Amazon.

   El número de artículo europeo (EAN) es una norma de código de barras, un código de identificación de producto de 12 o 13 dígitos. Cada EAN identifica de forma exclusiva el producto, el fabricante y sus atributos; normalmente, el EAN se imprime en una etiqueta de producto o en un embalaje como código de barras. Amazon requiere códigos EAN para mejorar la calidad de los resultados de búsqueda y la calidad del catálogo. Puede obtener EAN del fabricante.

1. Para **[!UICONTROL GCID]**, elija el atributo de producto que creó para el valor GCIN de Amazon.

   El Identificador de catálogo global (GCID) es un ID para productos que no tienen código UPC o ISBN. El Registro de marcas de Amazon le permite registrarse como propietario de una marca y crear un ID único para los productos.

1. Para **[!UICONTROL ISBN]**, elija el atributo de producto que creó para el valor ISBN de Amazon.

   El número de libro estándar internacional (ISBN) es un código de barras único de identificador comercial de libro. Cada código ISBN identifica un libro de forma exclusiva. Un ISBN tiene diez o 13 dígitos. Todos los ISBN asignados después del 1 de enero de 2007 tienen 13 dígitos.

1. Para **[!UICONTROL UPC]**, elija el atributo de producto que creó para el valor UPC de Amazon.

   El código de producto universal (UPC) es un código de barras de 12 dígitos que se utiliza ampliamente en los envases de venta al por menor en Estados Unidos.

1. Para **[!UICONTROL General Search]**, elija el atributo de producto que desee usar para una coincidencia de búsqueda general.

   Este atributo es uno que puede seleccionar para hacer coincidir [!DNL Commerce] productos con el listado de Amazon apropiado. La búsqueda general utiliza búsquedas de palabras clave del catálogo. Por lo tanto, se recomienda utilizar un atributo [!DNL Commerce] que contenga palabras clave relevantes, como el SKU o el nombre del producto. La búsqueda general puede devolver muchas coincidencias posibles y, en estos casos, puede seleccionar el listado de Amazon adecuado entre las posibles coincidencias. Una selección común para este campo es `Product Name`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Búsqueda en el catálogo](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| Campo | Descripción |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa [!DNL Amazon Standard Identification Number]. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL EAN (European Article Number)] | Un código de identificación de producto de 12 o 13 dígitos. El número de artículo europeo (EAN) es una norma de código de barras, un código de identificación de producto de 12 o 13 dígitos. Cada EAN identifica de forma exclusiva el producto, el fabricante y sus atributos; normalmente, el EAN se imprime en una etiqueta de producto o en un embalaje como código de barras. Amazon requiere códigos EAN para mejorar la calidad de los resultados de búsqueda y la calidad del catálogo. Puede obtener EAN del fabricante. |
| [!UICONTROL GCID (Global Catalog Identifier)] | El Identificador de catálogo global (GCID) es un ID para productos que no tienen código UPC o ISBN. El Registro de marcas de Amazon le permite registrarse como propietario de una marca y crear un ID único para productos que pueden no tener un UPC o ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | Un código de barras de identificador único de libro comercial de 10 o 13 dígitos. El número de libro estándar internacional (ISBN) es un código de barras único de identificador comercial de libro. Cada código ISBN identifica un libro de forma exclusiva. Un ISBN tiene diez o 13 dígitos. Todos los ISBN asignados después del 1 de enero de 2007 tienen 13 dígitos. |
| UPC (código de producto universal) | Un código de barras de 12 dígitos. El código de producto universal (UPC) es un código de barras de 12 dígitos que se utiliza ampliamente en los envases de venta al por menor en Estados Unidos. |
| [!UICONTROL General Search] | Seleccione un atributo. Este atributo es uno que puede seleccionar para hacer coincidir [!DNL Commerce] productos con el listado de Amazon apropiado. La búsqueda general utiliza búsquedas de palabras clave del catálogo. Por lo tanto, se recomienda utilizar un atributo [!DNL Commerce] que contenga palabras clave relevantes, como el SKU o el nombre del producto. La búsqueda general puede devolver muchas coincidencias posibles y, en estos casos, puede seleccionar el listado de Amazon adecuado entre las posibles coincidencias. Una selección común para este campo es `Product Name`. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
