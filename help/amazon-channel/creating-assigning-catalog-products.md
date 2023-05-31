---
title: Crear y asignar productos para el canal de ventas de Amazon
description: La Sales Channel de Amazon proporciona el [!UICONTROL New Third Party] para crear y asignar productos del catálogo de Commerce que coincidan con anuncios de Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Creación y asignación de productos

Al ver _[!UICONTROL New Third Party]_pestaña, puede hacer coincidir su [!DNL Commerce] catalogar productos a un listado de Amazon existente. Hay dos opciones para esta coincidencia. Puede asignar un listado a un producto de catálogo existente o puede utilizar la información del listado para crear productos de catálogo. Estas opciones son útiles cuando los anuncios de Amazon no coinciden automáticamente con las [!DNL Commerce] catálogo.

Hacer coincidir (o asignar) sus productos con sus anuncios de Amazon es necesario para utilizar el conjunto completo de funciones del canal de ventas de Amazon.

Cuando crea un producto de catálogo a partir de una lista de Amazon:

- El **ASINA** se convierte en [!DNL Commerce] SKU
- El **Nombre del listado de productos** se convierte en el nombre del listado de catálogo
- El **Precio** y **Cantidad** se importan desde el listado de Amazon

El resto de la configuración necesaria viene determinado por la variable [!DNL Commerce] configuración del producto que selecciona durante la creación.

Cuando se crean y se comparan, los anuncios se eliminan del _[!UICONTROL New Third Party]_y aparecerán en la_[!UICONTROL Active]_ pestaña.

## Asignar un solo producto de catálogo a un listado de Amazon

1. Ver los listados de productos en [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña.

1. Busque el listado que desea asignar en la lista y haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y haga clic en **[!UICONTROL Assign Catalog Product]**.

   Esta acción abre el _[!UICONTROL Assign Magento Catalog Product]_página.

1. Busque o filtre la lista utilizando el [controles de workspace](./workspace-controls.md) y busque el producto de catálogo adecuado que coincida con el listado.

1. Cuando aparezca el producto correcto en la lista, haga clic en **[!UICONTROL Assign Catalog Product]** en el _[!UICONTROL Action]_columna.

Su producto y listado ahora coinciden. El canal de ventas de Amazon ahora puede compartir datos de productos y listados con Amazon y administrar su listado y su información, incluidos el precio de listado, el precio de envío, el stock/cantidad, la información y el estado del pedido, etc.

## Crear un único producto de catálogo utilizando la información de listado de Amazon

1. Ver los listados de productos en [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña.

1. Busque el anuncio que desea crear en su [!DNL Commerce] catálogo, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y haga clic en **[!UICONTROL Create New Catalog Product]**.

   Esta acción abre el _[!UICONTROL Create Magento Catalog Product]_página.

1. Complete la configuración del catálogo para el producto.

   - Establecer **[!UICONTROL Enable Product(s)]** cambiar a `Yes` o `No` (obligatorio).

      |Sí|Elija que el producto cumpla los requisitos para su [!DNL Commerce] ventas de tienda.| |No|Elija que el producto no cumpla los requisitos para su [!DNL Commerce] ventas de tienda.|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Clic **[!UICONTROL Done]** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) al que desea asociar el producto.

      Las opciones de esta lista dependen de su [!DNL Commerce] [configuración de tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configuración.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de su [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que ha configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no se incluye en los anuncios de las tiendas, aunque podría estar disponible como una variación de otro producto.| |**[!UICONTROL Catalog]**|El producto aparece en los listados del catálogo.| |**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.| |**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y disponible para las operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de la variable [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que ha configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

El producto del catálogo se crea en su [!DNL Commerce] y asignado al listado de Amazon a partir del cual se creó. Ahora que el listado coincide con un listado de Amazon existente, el listado se elimina del _[!UICONTROL New Third Party]_y aparecen en la pestaña_[!UICONTROL Active]_ pestaña.

## Crear varios productos de catálogo utilizando la información de su listado de Amazon

1. Ver los listados de productos en [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña.

1. Seleccione los listados para los que desea crear productos de catálogo.

   Puede seleccionar casillas de verificación individuales en la columna del lado izquierdo o puede hacer clic en la flecha hacia abajo de la columna superior izquierda y elegir **[!UICONTROL Select All]** o **[!UICONTROL Select All on this Page]**.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceptar el mensaje de confirmación y abrir _[!UICONTROL Create Magento Catalog Product]_página, haga clic en **[!UICONTROL OK]**.

1. Complete la configuración del catálogo de los productos.

   >[!NOTE]
   >Al crear productos de catálogo para varios anuncios seleccionados, la configuración de producto introducida se aplica a todos los anuncios.

   - Establecer **[!UICONTROL Enable Product(s)]** cambiar a `Yes` o `No` (obligatorio).

      |Sí|Elija que el producto cumpla los requisitos para su [!DNL Commerce] ventas de tienda.| |No|Elija que el producto no cumpla los requisitos para su [!DNL Commerce] ventas de tienda.|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Clic **Listo** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) al que desea asociar el producto.

      Las opciones de esta lista dependen de su [!DNL Commerce] [configuración de tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configuración.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de su [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que ha configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no se incluye en los anuncios de las tiendas, aunque podría estar disponible como una variación de otro producto.| |**[!UICONTROL Catalog]**|El producto aparece en los listados del catálogo.| |**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.| |**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y disponible para las operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de la variable [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que ha configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

Los productos del catálogo se crean en su [!DNL Commerce] y asignado al listado de Amazon a partir del cual se creó. Ahora que los anuncios coinciden con sus respectivas listas de Amazon, se eliminan del [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) y aparecen en la pestaña [_[!UICONTROL Active]_](./active-listings.md) pestaña.

![Crear producto del catálogo de Commerce](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatorio) Si está activado, el producto es visible en su [!DNL Commerce] tienda. Si está desactivado, el producto no se muestra en su [!DNL Commerce] tienda. |
| [!UICONTROL Categories] | Puede introducir el nombre de la categoría del nuevo producto o seleccionar una categoría haciendo clic en la flecha hacia abajo para mostrar las opciones. Las opciones dependen de su [categorías](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) configuración. |
| [!UICONTROL Website Ids] | (Obligatorio) Elija el sitio web (tienda) al que se asociará el producto. Las opciones dependen de su [!DNL Commerce] [configuración de tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) configuración |
| ID de conjunto de atributos | Seleccione un conjunto de atributos. Las opciones dependen de la configuración [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | Opciones:<ul><li>**[!UICONTROL Not Visible Individually]** - El producto no es visible en su [!DNL Commerce] tienda (más común para productos de variante).</li><li>**[!UICONTROL Catalog]** - Permite acceder al producto a través de la categoría a la que está asociado dentro del sitio web.</li><li>**Buscar** - Permite que el producto solo se encuentre a través de la herramienta de búsqueda.</li><li>**[!UICONTROL Catalog and Search]** - Permite acceder a los productos a través de la estructura de categorías y utilizando la herramienta de búsqueda.</li></ul> |
| [!UICONTROL Assign Tax Class] | Asigne una clase de impuestos al nuevo producto. Las opciones dependen de la configuración [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
