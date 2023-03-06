---
title: Crear y editar atributos
description: La Sales Channel de Amazon proporciona la vista Atributos para ayudarle a revisar los atributos actuales de Amazon y los atributos de comercio vinculados.
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Crear y editar atributos

Crear o actualizar [!DNL Commerce] atributos a medida que vende a través de Amazon y actualiza sus tiendas. Revise los atributos actuales de Amazon y los vínculos [!DNL Commerce] mediante los atributos [_[!UICONTROL Attributes]_vista](./attributes-view.md) de la página de inicio del canal de ventas de Amazon. El_[!UICONTROL Action]_ muestra las acciones disponibles para el atributo. Puede crear y asignar un nuevo [!DNL Commerce] para un atributo de Amazon no vinculado o puede editar uno existente [!DNL Commerce] y su asignación a un atributo de Amazon.

A medida que crea y actualiza atributos, es posible que desee comprobar los valores de atributo de [!DNL Commerce] y productos de Amazon. Estos valores pueden diferir si no sincroniza e importa valores de Amazon. Para revisar los valores de Amazon de estos atributos, consulte [Revisión de la asignación de atributos de Amazon](./amazon-matching-attributes-values.md). Si desea cambiar esos valores, puede hacer lo siguiente [edición o creación de una asignación](./amazon-manually-update-incomplete-listing.md) entre Amazon y [!DNL Commerce].

## Crear un atributo {#create-an-attribute}

Estos pasos crean un [!DNL Commerce] y asignarlo a un atributo de Amazon. Según la configuración, los valores pueden comenzar a sincronizarse entre catálogos.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create Attribute]** en el _[!UICONTROL Action]_columna.

1. Para habilitar la sincronización de los valores de Amazon con el elemento vinculado [!DNL Commerce] atributo, establecer **[!UICONTROL Is Active]** hasta `Yes`.

   Cuando se establece en `Yes`, los valores se sincronizan según la configuración.

1. Elegir `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   El atributo se asigna al elegido para **[!UICONTROL Amazon Attribute Name]**.

1. Introduzca una **[!UICONTROL Magento Product Attribute Name]**.

1. Introduzca una **[!UICONTROL Magento Product Attribute Code]**.

   Este valor debe estar en minúscula y sin espacios.

1. Para **[!UICONTROL Attribute Set Ids]**, elija un Conjunto de atributos para asignar.

   Normalmente, los atributos forman parte de un conjunto de atributos, como un conjunto de colores que tienen atributos para azul, verde, amarillo y rojo.

1. Para **[!UICONTROL Type]**, elija el tipo de valor del atributo, como texto y números.

   Esta opción afecta al valor permitido para el atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, se establece en `Yes` para permitir que el atributo esté disponible para un parámetro dentro de las condiciones promocionales.

1. Para **[!UICONTROL Used in Search]**, se establece en `Yes` si el atributo y el valor se pueden utilizar en búsquedas de productos.

1. Para **[!UICONTROL Comparable on Storefront]**, se establece en `Yes` si el valor del atributo se puede utilizar en la funcionalidad &quot;Comparar por&quot; de Amazon.

1. Elija la [!DNL Commerce] [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target="_blank"} para el atributo y, a continuación, seleccione una o varias vistas de tienda en las que importar los valores de Amazon.

   Si el ámbito se establece en `Global`, el _[!UICONTROL Store View]_no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, sincroniza y guarda valores en todas las vistas de la tienda de Amazon. Es posible que solo desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

Después de guardar, es posible que desee editar el atributo para revisar la configuración y hacer coincidir Amazon y [!DNL Commerce] valores del atributo. También puede indicar si los valores de Amazon deben sobrescribirse [!DNL Commerce] valores.

![crear configuración de atributos](assets/amazon-attribute-settings-create.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Configure como. `Yes` para garantizar los valores de atributo de Amazon y [!DNL Commerce] permanecer sincronizado para el atributo seleccionado. |
| Seleccionar atributo de producto de Magento | Indica el atributo seleccionado que desea vincular al nombre de atributo de Amazon de la lista. Al crear un atributo, elija `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo de Amazon que ha elegido. El atributo seleccionado vincula a este atributo de Amazon. No puede editar este valor mediante [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica el nombre del atributo o &quot;etiqueta&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica el código de atributo, todo en caracteres en minúsculas sin espacios. |
| [!UICONTROL Attribute Set Ids] | Indica el conjunto de atributos al que asignar el atributo. Los atributos tienden a formar parte de un conjunto de atributos, como un conjunto de colores que tienen atributos para azul, verde, amarillo y rojo. |
| [!UICONTROL Type] | Indica el tipo de valor del atributo, como texto y números. La selección afecta al valor permitido para el atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Cambiar a `Yes` para permitir que el atributo esté disponible para un parámetro dentro de las condiciones promocionales. |
| [!UICONTROL Used in Search] | Indica si el atributo y el valor se pueden utilizar en búsquedas de productos. |
| [!UICONTROL Comparable on Storefront] | Indica si el valor del atributo se puede utilizar en la funcionalidad &quot;Comparar por&quot; de Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica el [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target="_blank"} para el atributo. Opciones: Global/Vista de tienda<br>Cuando se establece en `Global`Sin embargo, la vista de la tienda no se puede editar una vez creado el atributo. |
| [!UICONTROL Store Views (to import values into to)] | Solo aparece cuando el ámbito está establecido en `Store View`. Elija la [vista de tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target="_blank"} a los que se sincronizan los valores de atributo de Amazon. Elección `All Store Views (Global)` actualiza el valor en todas las [!DNL Commerce] vistas de la tienda. |

## Edición de un atributo {#edit-an-attribute}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. Para habilitar o deshabilitar la sincronización de los valores de Amazon con el vínculo [!DNL Commerce] atributo, establecer **Está activo** hasta `Yes` o `No`.

   Cuando se establece en `Yes`, los valores se sincronizan según la configuración.

1. Para **[!UICONTROL Select Magento Product Attribute]**, compruebe o actualice el atributo para asignarlo al elegido **[!UICONTROL Amazon Attribute Name]**.

1. Indique si desea que el valor del atributo Amazon entrante sobrescriba el valor del atributo existente.

   Por ejemplo, es posible que no desee sobrescribir los precios de Amazon en [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserva el valor, conservando valores diferentes para el [!DNL Commerce] y tiendas Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Sobrescribe el valor en el [!DNL Commerce] catálogo de productos con el valor Amazon entrante.

1. Si está disponible para edición, elija una o más **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si el atributo se creó con un `Global` ámbito, el _Vista de tienda_ no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, sincroniza y guarda valores en todas las vistas de tiendas. Es posible que solo desee sincronizar valores con vistas de tienda específicas.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute Settings]**.

![editar configuración de atributos](assets/amazon-attribute-settings-edit.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Configure como. `Yes` para garantizar los valores de atributo de Amazon y [!DNL Commerce] permanecer sincronizado para el atributo seleccionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica el seleccionado [!DNL Commerce] que desea vincular al Nombre de atributo de Amazon de la lista. Si desea cambiar el elemento vinculado [!DNL Commerce] , elija un atributo diferente de la lista desplegable. Los valores se sincronizan según las configuraciones. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo de Amazon definido en [!DNL Amazon Seller Central]. El seleccionado [!DNL Commerce] vínculos a este atributo de Amazon. No puede editar este valor mediante [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica si los valores de atributo de Amazon sobrescriben los existentes [!DNL Commerce] que afectan a todos los productos con esta variable [!DNL Commerce] atributo.<ul><li>**No sobrescribir valores de Magento existentes** - (Predeterminado) Conserva el [!DNL Commerce] valor, mantener valores diferentes para [!DNL Commerce] y tiendas Amazon.</li><li>**Sobrescribir valores de Magento existentes** - Guarda el valor de Amazon sobre el [!DNL Commerce] valor en [!DNL Commerce] catálogo de productos.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | No aparece al editar un atributo si el atributo se creó con `Global` ámbito. Indica el [!DNL Commerce] [ámbito](https://docs.magento.com/user-guide/configuration/scope.html){target="_blank"} se creó y se estableció en `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Elija su [!DNL Commerce] [vista de tienda](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target="_blank"} a la que se sincronizan los valores de atributo de Amazon. Elección `All Store Views (Global)` actualiza el valor en todas las vistas de tiendas. |
