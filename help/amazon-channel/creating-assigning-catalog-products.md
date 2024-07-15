---
title: Crear y asignar productos para el canal de ventas de Amazon
description: La Sales Channel de Amazon proporciona la ficha [!UICONTROL New Third Party] para ayudar a crear y asignar productos del catálogo de Commerce que coincidan con anuncios de Amazon.
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Creación y asignación de productos

Al ver la ficha _[!UICONTROL New Third Party]_, puede hacer coincidir los productos del catálogo [!DNL Commerce] con un listado de Amazon existente. Hay dos opciones para esta coincidencia. Puede asignar un listado a un producto de catálogo existente o puede utilizar la información del listado para crear productos de catálogo. Estas opciones son útiles cuando los anuncios de Amazon no coinciden automáticamente con el catálogo [!DNL Commerce].

Hacer coincidir (o asignar) sus productos con sus anuncios de Amazon es necesario para utilizar el conjunto completo de funciones del canal de ventas de Amazon.

Cuando crea un producto de catálogo a partir de una lista de Amazon:

- El **ASIN** se convierte en el SKU [!DNL Commerce]
- El **nombre de lista de productos** se convierte en el nombre de lista de catálogos
- **Precio** y **Cantidad** se han importado del anuncio de Amazon

El resto de la configuración necesaria está determinada por la configuración del producto [!DNL Commerce] que seleccione durante la creación.

Cuando se crean y coinciden, los listados se eliminan de la ficha _[!UICONTROL New Third Party]_y aparecen en la ficha_[!UICONTROL Active]_.

## Asignar un solo producto de catálogo a un listado de Amazon

1. Vea sus listados de productos en la ficha [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Busque el listado que desea asignar en la lista, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y haga clic en **[!UICONTROL Assign Catalog Product]**.

   Esta acción abre la página _[!UICONTROL Assign Magento Catalog Product]_.

1. Busque o filtre la lista con los [controles del espacio de trabajo](./workspace-controls.md) y busque el producto del catálogo apropiado que coincida con la lista.

1. Cuando aparezca el producto correcto en la lista, haga clic en **[!UICONTROL Assign Catalog Product]** en la columna _[!UICONTROL Action]_.

Su producto y listado ahora coinciden. El canal de ventas de Amazon ahora puede compartir datos de productos y listados con Amazon y administrar su listado y su información, incluidos el precio de listado, el precio de envío, el stock/cantidad, la información y el estado del pedido, etc.

## Crear un único producto de catálogo utilizando la información de listado de Amazon

1. Vea sus listados de productos en la ficha [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Busque el listado que desea crear en el catálogo [!DNL Commerce], haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y haga clic en **[!UICONTROL Create New Catalog Product]**.

   Esta acción abre la página _[!UICONTROL Create Magento Catalog Product]_.

1. Complete la configuración del catálogo para el producto.

   - Establezca el conmutador **[!UICONTROL Enable Product(s)]** en `Yes` o `No` (obligatorio).

     |Sí|Elige que el producto cumpla los requisitos para tus ventas de tienda de [!DNL Commerce].|
|No|Elige que el producto no cumpla los requisitos para tus ventas de tienda de [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

     Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **[!UICONTROL Done]** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) al que se asociará el producto.

     Las opciones de esta lista dependen de la configuración de [!DNL Commerce] [tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

     `Default` es la selección predeterminada. Las opciones de esta lista dependen de los [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que haya configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

     |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no se incluye en los listados de tienda, aunque podría estar disponible como una variación de otro producto.|
|**[!UICONTROL Catalog]**|El producto aparece en los listados del catálogo.|
|**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.|
|**[!UICONTROL Catalog and Search]**|El producto está incluido en los listados del catálogo y disponible para las operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

     Las opciones que se muestran en esta lista dependen de las [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que haya configurado.

   - Una vez finalizado, haga clic en **[!UICONTROL Create Catalog Products]**.

El producto del catálogo se crea en el catálogo [!DNL Commerce] y se asigna al listado de Amazon a partir del cual se creó. Ahora que el listado coincide con un listado de Amazon existente, el listado se elimina de la pestaña _[!UICONTROL New Third Party]_y aparece en la pestaña_[!UICONTROL Active]_.

## Crear varios productos de catálogo utilizando la información de su listado de Amazon

1. Vea sus listados de productos en la ficha [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Seleccione los listados para los que desea crear productos de catálogo.

   Puede seleccionar casillas de verificación individuales en la columna del lado izquierdo, o bien puede hacer clic en la flecha hacia abajo en la columna superior izquierda y elegir **[!UICONTROL Select All]** o **[!UICONTROL Select All on this Page]**.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceptar el mensaje de confirmación y abrir la página _[!UICONTROL Create Magento Catalog Product]_, haga clic en **[!UICONTROL OK]**.

1. Complete la configuración del catálogo de los productos.

   >[!NOTE]
   >Al crear productos de catálogo para varios anuncios seleccionados, la configuración de producto introducida se aplica a todos los anuncios.

   - Establezca el conmutador **[!UICONTROL Enable Product(s)]** en `Yes` o `No` (obligatorio).

     |Sí|Elige que el producto cumpla los requisitos para tus ventas de tienda de [!DNL Commerce].|
|No|Elige que el producto no cumpla los requisitos para tus ventas de tienda de [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

     Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **Listo** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) al que se asociará el producto.

     Las opciones de esta lista dependen de la configuración de [!DNL Commerce] [tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

     `Default` es la selección predeterminada. Las opciones de esta lista dependen de los [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que haya configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

     |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no se incluye en los listados de tienda, aunque podría estar disponible como una variación de otro producto.|
|**[!UICONTROL Catalog]**|El producto aparece en los listados del catálogo.|
|**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.|
|**[!UICONTROL Catalog and Search]**|El producto está incluido en los listados del catálogo y disponible para las operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

     Las opciones que se muestran en esta lista dependen de las [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que haya configurado.

   - Una vez finalizado, haga clic en **[!UICONTROL Create Catalog Products]**.

Los productos del catálogo se crean en el catálogo [!DNL Commerce] y se asignan al listado de Amazon a partir del cual se crearon. Ahora que los anuncios coinciden con sus respectivas listas de Amazon, se eliminan de la ficha [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) y aparecen en la ficha [_[!UICONTROL Active]_](./active-listings.md).

![Crear producto de catálogo de Commerce](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | (Obligatorio) Si está habilitado, el producto estará visible en la tienda [!DNL Commerce]. Si se deshabilita, el producto no se mostrará en la tienda [!DNL Commerce]. |
| [!UICONTROL Categories] | Puede introducir el nombre de la categoría del nuevo producto o seleccionar una categoría haciendo clic en la flecha hacia abajo para mostrar las opciones. Las opciones dependen de la configuración de [categories](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html). |
| [!UICONTROL Website Ids] | (Obligatorio) Elija el sitio web (tienda) al que se asociará el producto. Las opciones dependen de la configuración de [!DNL Commerce] [tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) |
| ID de conjunto de atributos | Seleccione un conjunto de atributos. Las opciones dependen de los [!DNL Commerce] [conjuntos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) configurados. |
| [!UICONTROL Visibility] | Opciones:<ul><li>**[!UICONTROL Not Visible Individually]**: el producto no está visible en la tienda [!DNL Commerce] (el más común para los productos de variante).</li><li>**[!UICONTROL Catalog]**: permite acceder al producto a través de la categoría a la que está asociado en el sitio web.</li><li>**Buscar** - Permite que el producto se encuentre solamente a través de la herramienta de búsqueda.</li><li>**[!UICONTROL Catalog and Search]**: permite acceder a los productos a través de la estructura de categorías y mediante la herramienta de búsqueda.</li></ul> |
| [!UICONTROL Assign Tax Class] | Asigne una clase de impuestos al nuevo producto. Las opciones dependen de las [clases de impuestos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) configuradas. |
