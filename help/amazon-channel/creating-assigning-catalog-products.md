---
title: Crear y asignar productos
description: La Sales Channel de Amazon proporciona la pestaña [!UICONTROL New Third Party] para ayudar a crear y asignar productos de catálogo de comercio coincidentes con listas de Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Crear y asignar productos

Al ver la pestaña _[!UICONTROL New Third Party]_, puede hacer coincidir los productos del catálogo de [!DNL Commerce] con un listado de Amazon existente. Hay dos opciones para esta coincidencia. Puede asignar una lista a un producto de catálogo existente o puede usar la información de la lista para crear productos de catálogo. Estas opciones son útiles cuando los anuncios de Amazon no coinciden automáticamente con el catálogo de [!DNL Commerce].

Para usar el conjunto completo de funciones del canal de ventas de Amazon, es necesario que los productos coincidan (o asignen) a sus anuncios de Amazon.

Al crear un producto de catálogo a partir de una lista de Amazon:

- El **ASIN** se convierte en el SKU [!DNL Commerce]
- El **Nombre de lista de productos** se convierte en el Nombre de lista de catálogo
- Los **Price** y **Quantity** se importan desde la Lista de Amazon

El resto de las opciones necesarias están determinadas por la configuración del producto [!DNL Commerce] que seleccione durante la creación.

Cuando se crean y coinciden, las listas se eliminan de la pestaña _[!UICONTROL New Third Party]_y aparecen en la pestaña_[!UICONTROL Active]_.

## Asignar un producto de catálogo único a una lista de Amazon

1. Consulte las listas de productos en la pestaña [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Busque el listado que desea asignar en la lista, haga clic **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y haga clic en **[!UICONTROL Assign Catalog Product]**.

   Esta acción abre la página _[!UICONTROL Assign Magento Catalog Product]_.

1. Busque o filtre la lista utilizando los [workspace controls](./workspace-controls.md) y busque el producto de catálogo correspondiente para que coincida con la lista.

1. Cuando aparezca el producto correcto en la lista, haga clic en **[!UICONTROL Assign Catalog Product]** en la columna _[!UICONTROL Action]_.

El producto y el anuncio ya coinciden. El canal de ventas de Amazon ahora puede compartir datos de productos y listados con Amazon y administrar su anuncio y su información, incluido el precio de venta, el precio de envío, las acciones y cantidades, la información y el estado del pedido, entre otros.

## Cree un producto de catálogo único utilizando la información de listado de Amazon

1. Consulte las listas de productos en la pestaña [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Busque el listado que desea crear en su catálogo [!DNL Commerce], haga clic **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_y haga clic en **[!UICONTROL Create New Catalog Product]**.

   Esta acción abre la página _[!UICONTROL Create Magento Catalog Product]_.

1. Complete la configuración del catálogo para el producto.

   - Establezca el **[!UICONTROL Enable Product(s)]** conmutador en `Yes` o `No` (obligatorio).

      |Sí|Elija hacer que el producto sea apto para sus ventas de tienda [!DNL Commerce].|
|No|Elija hacer que el producto no sea apto para sus ventas de tienda [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **[!UICONTROL Done]** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) para el que se asociará el producto.

      Las opciones de esta lista dependen de la configuración de [!DNL Commerce] [tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de los [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que haya configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no está incluido en sus listas de tiendas, aunque podría estar disponible como una variación de otro producto.|
|**[!UICONTROL Catalog]**|El producto aparece en sus listas de catálogos.|
|**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.|
|**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y disponible para operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de las [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que haya configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

El producto del catálogo se crea en su catálogo [!DNL Commerce] y se asigna a la lista de Amazon desde la que se creó. Ahora que la lista coincide con una lista de Amazon existente, la lista se elimina de la pestaña _[!UICONTROL New Third Party]_y aparece en la pestaña_[!UICONTROL Active]_.

## Crear varios productos de catálogo utilizando la información de listado de Amazon

1. Consulte las listas de productos en la pestaña [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Seleccione los listados para los que desea crear productos de catálogo.

   Puede seleccionar casillas de verificación individuales en la columna del lado izquierdo o puede hacer clic en la flecha hacia abajo en la columna superior izquierda y elegir **[!UICONTROL Select All]** o **[!UICONTROL Select All on this Page]**.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create New Catalog Product(s)]**.

1. Para aceptar el mensaje de confirmación y abrir la página _[!UICONTROL Create Magento Catalog Product]_, haga clic en **[!UICONTROL OK]**.

1. Complete la configuración del catálogo para los productos.

   >[!NOTE]
   >Al crear productos de catálogo para varias listas seleccionadas, la configuración de producto introducida se aplica a todas las listas.

   - Establezca el **[!UICONTROL Enable Product(s)]** conmutador en `Yes` o `No` (obligatorio).

      |Sí|Elija hacer que el producto sea apto para sus ventas de tienda [!DNL Commerce].|
|No|Elija hacer que el producto no sea apto para sus ventas de tienda [!DNL Commerce].|

   - Para **[!UICONTROL Categories]**, asigne una categoría para el producto (opcional).

      Para seleccionar la categoría del producto, haga clic en la flecha hacia abajo y seleccione una casilla de verificación de categoría. Haga clic en **Listo** cuando termine.

   - Para **[!UICONTROL Website Ids]**, elija el sitio web (tienda) para el que se asociará el producto.

      Las opciones de esta lista dependen de la configuración de [!DNL Commerce] [tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Attribute Set Id]** (obligatorio), elija una opción.

      `Default` es la selección predeterminada. Las opciones de esta lista dependen de los [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que haya configurado.

   - Para **[!UICONTROL Visibility]**, elija una opción para el nuevo producto.

      |**[!UICONTROL Not Visible Individually]** (predeterminado)|El producto no está incluido en sus listas de tiendas, aunque podría estar disponible como una variación de otro producto.|
|**[!UICONTROL Catalog]**|El producto aparece en sus listas de catálogos.|
|**[!UICONTROL Search]**|El producto está disponible para operaciones de búsqueda.|
|**[!UICONTROL Catalog and Search]**|El producto está incluido en las listas de catálogos y disponible para operaciones de búsqueda.|

   - Para **[!UICONTROL Assign Tax Class]**, elija una opción para el producto.

      Las opciones que se muestran en esta lista dependen de las [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que haya configurado.

   - Cuando termine, haga clic en **[!UICONTROL Create Catalog Products]**.

Los productos del catálogo se crean en su catálogo [!DNL Commerce] y se asignan a la lista de Amazon desde la que se creó. Ahora que los listados coinciden con sus respectivos listados de Amazon, los listados se eliminan de la pestaña [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) y aparecen en la pestaña [_[!UICONTROL Active]_](./active-listings.md).

![Crear producto de catálogo de comercio](assets/amazon-magento-catalog-product.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatorio) Si está habilitado, el producto es visible en su tienda [!DNL Commerce]. Si está desactivado, el producto no se muestra en su tienda [!DNL Commerce]. |
| [!UICONTROL Categories] | Puede introducir el nombre de la categoría del nuevo producto o seleccionar una categoría haciendo clic en la flecha hacia abajo para mostrar las opciones. Las opciones dependen de la configuración [categories](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obligatorio) Elija el sitio web (tienda) para el que se asociará el producto. Las opciones dependen de la configuración de [!DNL Commerce] [tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} |
| Id De Conjunto De Atributos | Elija un conjunto de atributos. Las opciones dependen de los [!DNL Commerce] [conjuntos de atributos](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} configurados. |
| [!UICONTROL Visibility] | Opciones:<ul><li>**[!UICONTROL Not Visible Individually]** - El producto no es visible en su  [!DNL Commerce] tienda (más común para los productos de variante).</li><li>**[!UICONTROL Catalog]** - Permite acceder al producto a través de la categoría a la que está asociado dentro del sitio web.</li><li>**Búsqueda** : permite que el producto solo se encuentre a través de la herramienta de búsqueda.</li><li>**[!UICONTROL Catalog and Search]** - Permite acceder a los productos a través de la estructura de categorías y mediante la herramienta de búsqueda.</li></ul> |
| [!UICONTROL Assign Tax Class] | Asigne una clase fiscal al nuevo producto. Las opciones dependen de las [clases de impuestos](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} configuradas. |
