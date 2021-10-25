---
title: Crear y asignar productos
description: La Sales Channel de Amazon proporciona la variable [!UICONTROL New Third Party] para crear y asignar productos de catálogo de comercio coincidentes con los anuncios de Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Crear y asignar productos

Al ver _[!UICONTROL New Third Party]_, puede coincidir con su [!DNL Commerce] catálogo de productos en una lista de Amazon existente. Hay dos opciones para esta coincidencia. Puede asignar una lista a un producto de catálogo existente o puede usar la información de la lista para crear productos de catálogo. Estas opciones son útiles cuando sus anuncios de Amazon no coinciden automáticamente con sus [!DNL Commerce] catálogo.

Para usar el conjunto completo de funciones del canal de ventas de Amazon, es necesario que los productos coincidan (o asignen) a sus anuncios de Amazon.

Al crear un producto de catálogo a partir de una lista de Amazon:

- La variable **ASIN** se convierte en la variable [!DNL Commerce] SKU
- La variable **Nombre de lista de productos** se convierte en el nombre de lista del catálogo
- La variable **Precio** y **Cantidad** se importan desde la lista de Amazon

El resto de los ajustes necesarios se determinan mediante la variable [!DNL Commerce] configuración de producto que seleccione durante la creación.

Cuando se crean y coinciden, los anuncios se eliminan del _[!UICONTROL New Third Party]_y aparecen en la pestaña_[!UICONTROL Active]_ pestaña .

## Asignar un producto de catálogo único a una lista de Amazon

1. Vea sus listados de productos en el [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña .

1. Busque el listado que desea asignar en la lista, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y haga clic en **[!UICONTROL Assign Catalog Product]**.

   Esta acción abre las _[!UICONTROL Assign Magento Catalog Product]_página.

1. Busque o filtre la lista utilizando la variable [controles del espacio de trabajo](./workspace-controls.md) y busque el producto de catálogo correspondiente para que coincida con la lista.

1. Cuando aparezca el producto correcto en la lista, haga clic en **[!UICONTROL Assign Catalog Product]** en el _[!UICONTROL Action]_para abrir el Navegador.

El producto y el anuncio ya coinciden. El canal de ventas de Amazon ahora puede compartir datos de productos y listados con Amazon y administrar su anuncio y su información, incluido el precio de venta, el precio de envío, las acciones y cantidades, la información y el estado del pedido, entre otros.

## Cree un producto de catálogo único utilizando la información de listado de Amazon

1. Vea sus listados de productos en el [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña .

1. Encuentre el listado que desea crear en su [!DNL Commerce] catálogo, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_y haga clic en **[!UICONTROL Create New Catalog Product]**.

   Esta acción abre las _[!UICONTROL Create Magento Catalog Product]_página.

1. Complete la configuración del catálogo para el producto.

   - Establezca **[!UICONTROL Enable Product(s)]** alternar a `Yes` o `No` (obligatorio).

      |Sí|Elija hacer que el producto sea apto para su [!DNL Commerce] ventas de tienda.| |No|Elija hacer que el producto no sea apto para su [!DNL Commerce] ventas de tienda.|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **[!UICONTROL Done]** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) para el que se asociará el producto.

      Las opciones de esta lista dependen de su [!DNL Commerce] [configuración del almacén](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Configuración de {target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de su [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que ha configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no está incluido en sus listas de tiendas, aunque podría estar disponible como una variación de otro producto.| |**[!UICONTROL Catalog]**|El producto aparece en las listas del catálogo.| |**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.| |**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y está disponible para operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de la variable [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que ha configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

El producto del catálogo se crea en su [!DNL Commerce] catálogo y asignado al listado de Amazon desde el que se creó. Ahora que la lista coincide con una lista de Amazon existente, la lista se elimina del _[!UICONTROL New Third Party]_y aparecen en la pestaña_[!UICONTROL Active]_ pestaña .

## Crear varios productos de catálogo utilizando la información de listado de Amazon

1. Vea sus listados de productos en el [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) pestaña .

1. Seleccione los listados para los que desea crear productos de catálogo.

   Puede seleccionar casillas individuales en la columna de la izquierda o hacer clic en la flecha hacia abajo en la columna de la parte superior izquierda y elegir **[!UICONTROL Select All]** o **[!UICONTROL Select All on this Page]**.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceptar el mensaje de confirmación y abrir el _[!UICONTROL Create Magento Catalog Product]_página, haga clic en **[!UICONTROL OK]**.

1. Complete la configuración del catálogo para los productos.

   >[!NOTE]
   >Al crear productos de catálogo para varias listas seleccionadas, la configuración de producto introducida se aplica a todas las listas.

   - Establezca **[!UICONTROL Enable Product(s)]** alternar a `Yes` o `No` (obligatorio).

      |Sí|Elija hacer que el producto sea apto para su [!DNL Commerce] ventas de tienda.| |No|Elija hacer que el producto no sea apto para su [!DNL Commerce] ventas de tienda.|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **Listo** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) para el que se asociará el producto.

      Las opciones de esta lista dependen de su [!DNL Commerce] [configuración del almacén](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Configuración de {target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de su [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que ha configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no está incluido en sus listas de tiendas, aunque podría estar disponible como una variación de otro producto.| |**[!UICONTROL Catalog]**|El producto aparece en las listas del catálogo.| |**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.| |**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y está disponible para operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de la variable [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que ha configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

Los productos del catálogo se crean en su [!DNL Commerce] catálogo y asignado al listado de Amazon desde el que se creó. Ahora que los anuncios coinciden con sus respectivos listados de Amazon, los listados se eliminan del [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) y aparecen en la pestaña [_[!UICONTROL Active]_](./active-listings.md) pestaña .

![Crear producto de catálogo de comercio](assets/amazon-magento-catalog-product.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatorio) Si está habilitado, el producto es visible en su [!DNL Commerce] tienda. Si está desactivado, el producto no se muestra en su [!DNL Commerce] tienda. |
| [!UICONTROL Categories] | Puede introducir el nombre de la categoría del nuevo producto o seleccionar una categoría haciendo clic en la flecha hacia abajo para mostrar las opciones. Las opciones dependen del [categories](https://docs.magento.com/user-guide/catalog/category-create.html)Configuración de {target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obligatorio) Elija el sitio web (tienda) para el que se asociará el producto. Las opciones dependen del [!DNL Commerce] [configuración del almacén](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Configuración de {target=&quot;_blank&quot;} |
| Id De Conjunto De Atributos | Elija un conjunto de atributos. Las opciones dependen de la configuración [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Visibility] | Opciones:<ul><li>**[!UICONTROL Not Visible Individually]** - El producto no es visible en su [!DNL Commerce] tienda (más común para los productos de variante).</li><li>**[!UICONTROL Catalog]** - Permite acceder al producto a través de la categoría a la que está asociado dentro del sitio web.</li><li>**Buscar** : permite que el producto solo se encuentre a través de la herramienta de búsqueda.</li><li>**[!UICONTROL Catalog and Search]** - Permite acceder a los productos a través de la estructura de categorías y mediante la herramienta de búsqueda.</li></ul> |
| [!UICONTROL Assign Tax Class] | Asigne una clase fiscal al nuevo producto. Las opciones dependen de la configuración [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}. |
