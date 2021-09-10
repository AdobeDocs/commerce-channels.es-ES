---
title: Crear y editar atributos
description: La Sales Channel de Amazon proporciona la vista Atributos para ayudarle a revisar los atributos actuales de Amazon y los atributos de comercio vinculados.
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Crear y editar atributos

Cree o actualice atributos [!DNL Commerce] a medida que vende a través de Amazon y actualice sus tiendas. Revise los atributos actuales de Amazon y los atributos [!DNL Commerce] vinculados a través de la [_[!UICONTROL Attributes]_vista](./attributes-view.md) de la página principal del canal de ventas de Amazon. La columna_[!UICONTROL Action]_ muestra las acciones disponibles para el atributo. Puede crear y asignar un nuevo atributo [!DNL Commerce] para un atributo Amazon desvinculado o editar un atributo [!DNL Commerce] existente y su asignación a un atributo Amazon.

A medida que crea y actualiza atributos, es posible que desee verificar los valores de atributo de los productos [!DNL Commerce] y Amazon. Estos valores pueden diferir si no sincroniza e importa valores de Amazon. Para revisar los valores de Amazon para estos atributos, consulte [Revisión de la asignación de atributos de Amazon](./amazon-matching-attributes-values.md). Si desea cambiar estos valores, puede [editar o crear una asignación](./amazon-manually-update-incomplete-listing.md) entre Amazon y [!DNL Commerce].

## Crear un atributo {#create-an-attribute}

Estos pasos crean un atributo [!DNL Commerce] y lo asignan a un atributo de Amazon. Según las configuraciones, los valores pueden comenzar a sincronizarse entre catálogos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic **[!UICONTROL Create Attribute]** en la columna _[!UICONTROL Action]_.

1. Para habilitar la sincronización de los valores de Amazon con el atributo [!DNL Commerce] vinculado, establezca **[!UICONTROL Is Active]** en `Yes`.

   Cuando se establece en `Yes`, los valores se sincronizan según la configuración.

1. Elija `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   El atributo se asigna al elegido para **[!UICONTROL Amazon Attribute Name]**.

1. Introduzca un **[!UICONTROL Magento Product Attribute Name]**.

1. Introduzca un **[!UICONTROL Magento Product Attribute Code]**.

   Este valor debe escribirse en minúscula y sin espacios.

1. Para **[!UICONTROL Attribute Set Ids]**, elija un conjunto de atributos para asignar.

   Normalmente, los atributos forman parte de un conjunto de atributos, como un conjunto de colores con atributos azul, verde, amarillo y rojo.

1. Para **[!UICONTROL Type]**, elija el tipo del valor del atributo, como texto y números.

   Esta opción afecta al valor permitido para el atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, establezca en `Yes` para permitir que el atributo esté disponible para un parámetro dentro de sus condiciones promocionales.

1. Para **[!UICONTROL Used in Search]**, establezca en `Yes` si el atributo y el valor se pueden usar en las búsquedas de productos.

1. Para **[!UICONTROL Comparable on Storefront]**, establézcalo en `Yes` si el valor del atributo se puede usar en la funcionalidad &quot;Comparar por&quot; de Amazon.

1. Elija el [!DNL Commerce] [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para el atributo y, a continuación, seleccione una o varias vistas de la tienda en las que importar los valores de Amazon.

   Si el ámbito se establece en `Global`, el _[!UICONTROL Store View]_no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, se sincronizan y se guardan los valores en todas las vistas de la tienda de Amazon. Solo es posible que desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

Después de guardar, puede que desee editar el atributo para revisar la configuración y los valores coincidentes de Amazon y [!DNL Commerce] del atributo. También puede indicar si los valores de Amazon deben sobrescribir los valores [!DNL Commerce].

![crear configuración de atributos](assets/amazon-attribute-settings-create.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Configúrelo en `Yes` para asegurarse de que los valores de atributo de Amazon y [!DNL Commerce] se mantengan sincronizados para el atributo seleccionado. |
| Seleccionar atributo de producto del Magento | Indica el atributo seleccionado que desea vincular al nombre de atributo de Amazon que aparece en la lista. Al crear un atributo, elija `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo de Amazon que ha elegido. El atributo seleccionado vincula a este atributo de Amazon. No puede editar este valor a través de [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica el nombre del atributo o &quot;etiqueta&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica el código de atributo, todo en caracteres en minúsculas sin espacios. |
| [!UICONTROL Attribute Set Ids] | Indica el conjunto de atributos al que asignar el atributo. Los atributos suelen formar parte de un conjunto de atributos, como un conjunto de colores con atributos azul, verde, amarillo y rojo. |
| [!UICONTROL Type] | Indica el tipo de valor del valor del atributo, como texto y números. La selección afecta al valor permitido para el atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Cambie a `Yes` para permitir que el atributo esté disponible para un parámetro dentro de las condiciones promocionales. |
| [!UICONTROL Used in Search] | Indica si el atributo y el valor se pueden usar en las búsquedas de productos. |
| [!UICONTROL Comparable on Storefront] | Indica si el valor del atributo se puede usar en la funcionalidad &quot;Comparar por&quot; de Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica el [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} del atributo. Opciones: Global / Vista de almacén<br>Cuando se establece en `Global`, la vista de almacén no se puede editar una vez creado el atributo. |
| [!UICONTROL Store Views (to import values into to)] | Solo aparece cuando el ámbito está establecido en `Store View`. Elija la [vista de almacén](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} a la que se sincronizan los valores de atributos de Amazon. Al seleccionar `All Store Views (Global)` se actualiza el valor en todas las [!DNL Commerce] vistas de tienda. |

## Editar un atributo {#edit-an-attribute}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Para habilitar o deshabilitar la sincronización de los valores de Amazon con el atributo [!DNL Commerce] vinculado, establezca **Is Active** en `Yes` o `No`.

   Cuando se establece en `Yes`, los valores se sincronizan según la configuración.

1. Para **[!UICONTROL Select Magento Product Attribute]**, verifique o actualice el atributo para asignarlo al **[!UICONTROL Amazon Attribute Name]** seleccionado.

1. Indique si desea que el valor del atributo entrante de Amazon sobrescriba el valor del atributo existente.

   Por ejemplo, es posible que no desee sobrescribir los precios de Amazon en [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserva el valor, manteniendo valores diferentes para las tiendas de Amazon  [!DNL Commerce] y .

   - **[!UICONTROL Overwrite Existing Magento Values]** - Sobrescribe el valor del catálogo de  [!DNL Commerce] productos con el valor de Amazon entrante.

1. Si está disponible para edición, elija uno o más **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si el atributo se creó con un ámbito `Global`, la _vista de almacén_ no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, sincroniza y guarda los valores en todas las vistas de la tienda. Solo es posible que desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

![editar configuración de atributos](assets/amazon-attribute-settings-edit.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Configúrelo en `Yes` para asegurarse de que los valores de atributo de Amazon y [!DNL Commerce] se mantengan sincronizados para el atributo seleccionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica el atributo [!DNL Commerce] seleccionado que desea vincular al nombre de atributo de Amazon indicado. Si desea cambiar el atributo vinculado [!DNL Commerce], elija un atributo diferente en la lista desplegable. Los valores se sincronizan según las configuraciones. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo Amazon definido en [!DNL Amazon Seller Central]. El atributo [!DNL Commerce] seleccionado vincula a este atributo de Amazon. No puede editar este valor a través de [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica si los valores de atributo de Amazon sobrescriben los valores [!DNL Commerce] existentes, lo que afecta a todos los productos con este atributo [!DNL Commerce].<ul><li>**No sobrescribir valores de Magento existentes** : (predeterminado) conserva el  [!DNL Commerce] valor, manteniendo valores diferentes para  [!DNL Commerce] y las tiendas de Amazon.</li><li>**Sobrescribir valores de Magento existentes** : guarda el valor de Amazon sobre el  [!DNL Commerce] valor del catálogo de  [!DNL Commerce] productos.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | No aparece al editar un atributo si el atributo se creó con el ámbito `Global`. Indica que el [!DNL Commerce] [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} se creó y se estableció en `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Elija la [!DNL Commerce] [vista de almacenamiento](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} a la que desea sincronizar los valores de atributos de Amazon. Al seleccionar `All Store Views (Global)` se actualiza el valor en todas las vistas de tienda. |
