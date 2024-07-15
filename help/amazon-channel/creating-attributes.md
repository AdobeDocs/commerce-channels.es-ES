---
title: Cree y edite atributos para el canal de ventas de Amazon
description: La Sales Channel de Amazon proporciona la vista Atributos para ayudarle a revisar los atributos actuales de Amazon y los atributos de Commerce vinculados.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Crear y editar atributos

Cree o actualice los atributos [!DNL Commerce] a medida que vende a través de Amazon y actualice sus tiendas. Revise los atributos actuales de Amazon y los atributos vinculados de [!DNL Commerce] a través de la vista [_[!UICONTROL Attributes]_](./attributes-view.md) de la página de inicio del canal de ventas de Amazon. La columna_[!UICONTROL Action]_ muestra las acciones disponibles para el atributo. Puede crear y asignar un nuevo atributo [!DNL Commerce] para un atributo de Amazon sin vincular, o bien puede editar un atributo [!DNL Commerce] existente y su asignación a un atributo de Amazon.

A medida que crea y actualiza atributos, es posible que desee comprobar los valores de atributo de [!DNL Commerce] y los productos de Amazon. Estos valores pueden diferir si no sincroniza e importa valores de Amazon. Para revisar los valores Amazon de estos atributos, consulte [Revisión de la asignación de atributos Amazon](./amazon-matching-attributes-values.md). Si desea cambiar esos valores, puede [editar o crear una asignación](./amazon-manually-update-incomplete-listing.md) entre Amazon y [!DNL Commerce].

## Crear un atributo {#create-an-attribute}

Estos pasos crean un atributo [!DNL Commerce] y lo asignan a un atributo Amazon. Según la configuración, los valores pueden comenzar a sincronizarse entre catálogos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create Attribute]** en la columna _[!UICONTROL Action]_.

1. Para habilitar la sincronización de los valores de Amazon con el atributo [!DNL Commerce] vinculado, establezca **[!UICONTROL Is Active]** en `Yes`.

   Cuando se establece en `Yes`, los valores se sincronizan de acuerdo con la configuración.

1. Elija `Create New Magento Attribute` para **[!UICONTROL Select Magento Product Attribute]**.

   El atributo se asigna al elegido para **[!UICONTROL Amazon Attribute Name]**.

1. Escriba un **[!UICONTROL Magento Product Attribute Name]**.

1. Escriba un **[!UICONTROL Magento Product Attribute Code]**.

   Este valor debe estar en minúscula y sin espacios.

1. Para **[!UICONTROL Attribute Set Ids]**, elija un conjunto de atributos para asignar.

   Normalmente, los atributos forman parte de un conjunto de atributos, como un conjunto de colores que tienen atributos para azul, verde, amarillo y rojo.

1. Para **[!UICONTROL Type]**, elija el tipo de valor del atributo, como texto y números.

   Esta opción afecta al valor permitido para el atributo.

1. Para **[!UICONTROL Use for Promo Rule Conditions]**, establézcalo en `Yes` para permitir que el atributo esté disponible para un parámetro dentro de sus condiciones promocionales.

1. Para **[!UICONTROL Used in Search]**, establézcalo en `Yes` si el atributo y el valor se pueden usar en las búsquedas de productos.

1. Para **[!UICONTROL Comparable on Storefront]**, establézcalo en `Yes` si el valor del atributo se puede usar en la funcionalidad &quot;Comparar por&quot; de Amazon.

1. Elija [!DNL Commerce] [ámbito](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) para el atributo y, a continuación, seleccione una o varias vistas de tienda en las que importar los valores de Amazon.

   Si el ámbito está establecido en `Global`, el _[!UICONTROL Store View]_no se puede cambiar después de crear el atributo.

   Si elige `All Store Views (Global)`, se sincronizan y guardan los valores en todas las vistas de la tienda Amazon. Es posible que solo desee sincronizar valores con vistas de tienda específicas.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute Settings]**.

Después de guardar, es posible que desee editar el atributo para revisar la configuración y los valores coincidentes de Amazon y [!DNL Commerce] para el atributo. También puede indicar si los valores Amazon deben sobrescribir los valores [!DNL Commerce].

![crear configuración de atributos](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Campo | Descripción |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Se establece en `Yes` para garantizar que los valores de atributo de Amazon y [!DNL Commerce] se mantengan sincronizados con el atributo seleccionado. |
| Seleccionar atributo de producto de Magento | Indica el atributo seleccionado que desea vincular al nombre de atributo de Amazon de la lista. Al crear un atributo, elija `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo de Amazon que ha elegido. El atributo seleccionado vincula a este atributo de Amazon. No puede editar este valor mediante [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indica el nombre del atributo o &quot;etiqueta&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indica el código de atributo, todo en caracteres en minúsculas sin espacios. |
| [!UICONTROL Attribute Set Ids] | Indica el conjunto de atributos al que asignar el atributo. Los atributos tienden a formar parte de un conjunto de atributos, como un conjunto de colores que tienen atributos para azul, verde, amarillo y rojo. |
| [!UICONTROL Type] | Indica el tipo de valor del atributo, como texto y números. La selección afecta al valor permitido para el atributo. |
| [!UICONTROL Use for Promo Rule Conditions] | Cambie a `Yes` para permitir que el atributo esté disponible para un parámetro dentro de sus condiciones promocionales. |
| [!UICONTROL Used in Search] | Indica si el atributo y el valor se pueden utilizar en búsquedas de productos. |
| [!UICONTROL Comparable on Storefront] | Indica si el valor del atributo se puede utilizar en la funcionalidad &quot;Comparar por&quot; de Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indica el [ámbito](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) del atributo. Opciones: Global / Vista de tienda<br>Cuando se establece en `Global`, la vista de tienda no se puede editar una vez creado el atributo. |
| [!UICONTROL Store Views (to import values into to)] | Solo aparece cuando el ámbito está establecido en `Store View`. Elija la [vista de tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) a la que se sincronizan los valores de atributo de Amazon. Al elegir `All Store Views (Global)`, se actualiza el valor en todas las [!DNL Commerce] vistas de tiendas. |

## Edición de un atributo {#edit-an-attribute}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Para habilitar o deshabilitar la sincronización de los valores de Amazon con el atributo [!DNL Commerce] vinculado, establezca **Está activo** en `Yes` o `No`.

   Cuando se establece en `Yes`, los valores se sincronizan de acuerdo con la configuración.

1. Para **[!UICONTROL Select Magento Product Attribute]**, compruebe o actualice el atributo para asignarlo al **[!UICONTROL Amazon Attribute Name]** elegido.

1. Indique si desea que el valor del atributo Amazon entrante sobrescriba el valor del atributo existente.

   Por ejemplo, es posible que no desee sobrescribir los precios de Amazon en [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**: conserva el valor y conserva valores diferentes para las tiendas [!DNL Commerce] y Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]**: sobrescribe el valor del catálogo de productos [!DNL Commerce] con el valor de Amazon entrante.

1. Si está disponible para edición, elija uno o más **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si el atributo se creó con un ámbito `Global`, la _vista de la tienda_ no se puede cambiar una vez creado el atributo.

   Si elige `All Store Views (Global)`, se sincronizan y guardan los valores en todas las vistas de tiendas. Es posible que solo desee sincronizar valores con vistas de tienda específicas.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute Settings]**.

![editar configuración de atributos](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Campo | Descripción |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indica si este atributo está activo y se sincroniza activamente entre Amazon y [!DNL Commerce]. Se establece en `Yes` para garantizar que los valores de atributo de Amazon y [!DNL Commerce] se mantengan sincronizados con el atributo seleccionado. |
| [!UICONTROL Select Magento Product Attribute] | Indica el atributo [!DNL Commerce] seleccionado que desea vincular con el nombre de atributo de Amazon de la lista. Si desea cambiar el atributo [!DNL Commerce] vinculado, elija un atributo diferente en la lista desplegable. Los valores se sincronizan según las configuraciones. |
| [!UICONTROL Amazon Attribute Name] | Muestra el nombre del atributo Amazon definido en [!DNL Amazon Seller Central]. El atributo [!DNL Commerce] seleccionado vincula a este atributo de Amazon. No puede editar este valor mediante [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indica si los valores del atributo Amazon sobrescriben los valores [!DNL Commerce] existentes, lo que afecta a todos los productos con este atributo [!DNL Commerce].<ul><li>**No sobrescribir valores de Magento existentes** - (predeterminado) Conserva el valor [!DNL Commerce], conservando valores diferentes para [!DNL Commerce] y tiendas Amazon.</li><li>**Sobrescribir valores de Magento existentes**: guarda el valor de Amazon sobre el valor [!DNL Commerce] en el catálogo de productos [!DNL Commerce].</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | No aparece al editar un atributo si el atributo se creó con el ámbito `Global`. Indica que el [!DNL Commerce] [ámbito](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) se creó y se estableció en `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Elija su [!DNL Commerce] [vista de tienda](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) con la que sincronizar los valores de atributo de Amazon. Al elegir `All Store Views (Global)`, se actualiza el valor en todas las vistas de tiendas. |
