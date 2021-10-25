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

Crear o actualizar [!DNL Commerce] a medida que vende a través de Amazon y actualiza sus tiendas. Revise los atributos actuales de Amazon y los vínculos [!DNL Commerce] a través de la variable [_[!UICONTROL Attributes]_ver](./attributes-view.md) de la página de inicio del canal de ventas de Amazon. La variable_[!UICONTROL Action]_ muestra las acciones disponibles para el atributo. Puede crear y asignar un nuevo [!DNL Commerce] para un atributo de Amazon desvinculado, o bien puede editar un atributo existente [!DNL Commerce] y su asignación a un atributo de Amazon.

A medida que crea y actualiza atributos, es posible que desee verificar los valores de atributo de [!DNL Commerce] y productos de Amazon. Estos valores pueden diferir si no sincroniza e importa valores de Amazon. Para revisar los valores de Amazon para estos atributos, consulte [Revisión de la asignación de atributos de Amazon](./amazon-matching-attributes-values.md). Si desea cambiar esos valores, puede [editar o crear una asignación](./amazon-manually-update-incomplete-listing.md) entre Amazon y [!DNL Commerce].

## Crear un atributo {#create-an-attribute}

Estos pasos crean un [!DNL Commerce] y asígnelo a un atributo de Amazon. Según las configuraciones, los valores pueden comenzar a sincronizarse entre catálogos.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create Attribute]** en el _[!UICONTROL Action]_para abrir el Navegador.

1. Para habilitar la sincronización de los valores de Amazon con el vínculo [!DNL Commerce] atributo, conjunto **[!UICONTROL Is Active]** a `Yes`.

   Cuando se configura como `Yes`, los valores se sincronizan según la configuración.

1. Choose `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   El atributo se asigna al elegido para **[!UICONTROL Amazon Attribute Name]**.

1. Escriba un **[!UICONTROL Magento Product Attribute Name]**.

1. Escriba un **[!UICONTROL Magento Product Attribute Code]**.

   Este valor debe escribirse en minúscula y sin espacios.

1. Para **[!UICONTROL Attribute Set Ids]**, elija un conjunto de atributos para asignarlo.

   Normalmente, los atributos forman parte de un conjunto de atributos, como un conjunto de colores con atributos azul, verde, amarillo y rojo.

1. Para **[!UICONTROL Type]**, elija el tipo del valor del atributo, como texto y números.

   Esta opción afecta al valor permitido para el atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, configure como `Yes` para permitir que el atributo esté disponible para un parámetro dentro de las condiciones promocionales.

1. Para **[!UICONTROL Used in Search]**, configure como `Yes` si el atributo y el valor pueden utilizarse en búsquedas de productos.

1. Para **[!UICONTROL Comparable on Storefront]**, configure como `Yes` si el valor del atributo puede utilizarse en la funcionalidad &quot;Comparar por&quot; de Amazon.

1. Elija la [!DNL Commerce] [scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para el atributo y, a continuación, seleccione una o varias vistas de la tienda en las que importar los valores de Amazon.

   Si el ámbito está configurado en `Global`, el _[!UICONTROL Store View]_no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, sincroniza y guarda valores en todas las vistas de la tienda de Amazon. Solo es posible que desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

Después de guardar, puede que desee editar el atributo para revisar la configuración y hacer coincidir Amazon y [!DNL Commerce] para el atributo. También puede indicar si los valores de Amazon deben sobrescribirse [!DNL Commerce] valores.

![crear configuración de atributos](assets/amazon-attribute-settings-create.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Establecer como `Yes` para garantizar los valores de atributo de Amazon y [!DNL Commerce] permanecer sincronizado para el atributo seleccionado. |
| Seleccionar atributo de producto del Magento | Indica el atributo seleccionado que desea vincular al nombre de atributo de Amazon que aparece en la lista. Al crear un atributo, elija `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo de Amazon que ha elegido. El atributo seleccionado vincula a este atributo de Amazon. No se puede editar este valor a través de [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica el nombre del atributo o &quot;etiqueta&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica el código de atributo, todo en caracteres en minúsculas sin espacios. |
| [!UICONTROL Attribute Set Ids] | Indica el conjunto de atributos al que asignar el atributo. Los atributos suelen formar parte de un conjunto de atributos, como un conjunto de colores con atributos azul, verde, amarillo y rojo. |
| [!UICONTROL Type] | Indica el tipo de valor del valor del atributo, como texto y números. La selección afecta al valor permitido para el atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Alternar a `Yes` para permitir que el atributo esté disponible para un parámetro dentro de las condiciones promocionales. |
| [!UICONTROL Used in Search] | Indica si el atributo y el valor se pueden usar en las búsquedas de productos. |
| [!UICONTROL Comparable on Storefront] | Indica si el valor del atributo se puede usar en la funcionalidad &quot;Comparar por&quot; de Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica la variable [scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} para el atributo . Opciones: Vista Global/Tienda<br>Cuando se configura como `Global`, la vista de tienda no se puede editar una vez creado el atributo. |
| [!UICONTROL Store Views (to import values into to)] | Solo aparece cuando el ámbito está establecido en `Store View`. Elija la [vista de tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} en el que se sincronizan los valores de atributo de Amazon. Elección `All Store Views (Global)` actualiza el valor en todas las [!DNL Commerce] vistas de la tienda. |

## Editar un atributo {#edit-an-attribute}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_para abrir el Navegador.

1. Para activar o desactivar la sincronización de los valores de Amazon con el vínculo [!DNL Commerce] atributo, conjunto **Está activo** a `Yes` o `No`.

   Cuando se configura como `Yes`, los valores se sincronizan según la configuración.

1. Para **[!UICONTROL Select Magento Product Attribute]**, verifique o actualice el atributo para asignarlo al **[!UICONTROL Amazon Attribute Name]**.

1. Indique si desea que el valor del atributo entrante de Amazon sobrescriba el valor del atributo existente.

   Por ejemplo, es posible que no desee sobrescribir los precios de Amazon en [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserva el valor, manteniendo valores diferentes para su [!DNL Commerce] y las tiendas de Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Sobrescribe el valor en la variable [!DNL Commerce] catálogo de productos con el valor de Amazon entrante.

1. Si está disponible para su edición, elija una o varias **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si el atributo se creó con un `Global` ámbito, _Vista de la tienda_ no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, sincroniza y guarda valores en todas las vistas de tiendas. Solo es posible que desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

![editar configuración de atributos](assets/amazon-attribute-settings-edit.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Establecer como `Yes` para garantizar los valores de atributo de Amazon y [!DNL Commerce] permanecer sincronizado para el atributo seleccionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica el [!DNL Commerce] que desea vincular al nombre de atributo de Amazon que aparece en la lista. Si desea cambiar el vínculo [!DNL Commerce] , elija un atributo diferente en la lista desplegable. Los valores se sincronizan según las configuraciones. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo Amazon definido en [!DNL Amazon Seller Central]. El [!DNL Commerce] vínculos de atributos a este atributo de Amazon. No se puede editar este valor a través de [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica si los valores de atributo de Amazon sobrescriben los existentes [!DNL Commerce] , que afectan a todos los productos con esta [!DNL Commerce] atributo.<ul><li>**No sobrescribir valores de Magento existentes** - (Predeterminado) Conserva el [!DNL Commerce] valor, manteniendo distintos valores para [!DNL Commerce] y las tiendas de Amazon.</li><li>**Sobrescribir valores de Magento existentes** - Guarda el valor de Amazon sobre el [!DNL Commerce] en la variable [!DNL Commerce] catálogo de productos.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | No aparece al editar un atributo si el atributo se creó con la variable `Global` ámbito. Indica la variable [!DNL Commerce] [scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} se creó y se estableció en `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Elija su [!DNL Commerce] [vista de tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} al que se deben sincronizar los valores de atributos de Amazon. Elección `All Store Views (Global)` actualiza el valor en todas las vistas de tiendas. |
