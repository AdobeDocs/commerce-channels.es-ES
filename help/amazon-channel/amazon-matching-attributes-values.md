---
title: Ver asignación de atributos de Amazon
description: Compruebe los valores de los atributos de Commerce vinculados para sincronizar correctamente entre Commerce y Amazon.
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Ver asignación de atributos de Amazon

Al asignar atributos de Amazon a [!DNL Commerce] atributos, Amazon sales channel realiza un seguimiento y proporciona una lista filtrable de todos los valores de Amazon. Utilice esta página para comprobar los valores de los vínculos [!DNL Commerce] los atributos se sincronizan correctamente entre [!DNL Commerce] y Amazon. Puede revisar los valores sincronizados del atributo de Amazon vinculados o no vinculados a un [!DNL Commerce] atributo. Para crear o editar los atributos de Amazon, consulte [Crear y editar atributos](./creating-attributes.md).

El _Valor de Amazon_ difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto mientras que `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor Amazon.

## Ver los valores de atributo

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create]** o **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. Haga clic en **[!UICONTROL Matching Attribute Values]** pestaña.

   Anuncios que tienen un correspondiente [!DNL Commerce] producto de catálogo mostrar un valor vinculado en la variable _[!UICONTROL Magento Product SKU]_columna. Al hacer clic en un vínculo, se abre la página de detalles del producto del catálogo correspondiente. Los cambios en los atributos de Amazon en la página de detalles del producto no se sincronizan con el canal de ventas de Amazon.

>[!TIP]
>Para editar o asignar la asignación de un listado a un producto del catálogo, consulte [Actualizar información requerida](./amazon-manually-update-incomplete-listing.md).

![Ver valores de atributo](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Region] | La región de la actividad de ventas definida en **[!DNL Amazon Marketplace]País** durante la integración con la tienda. |
| [!UICONTROL Magento Product SKU] | Indica el [!DNL Commerce] productos sincronizados con la tienda Amazon. El valor es un ID de producto asignado por [!DNL Commerce] y está vinculado a un producto del catálogo. Para abrir el producto en [!DNL Commerce], haga clic en el vínculo. |
| [!UICONTROL ASIN] | Indica el identificador único alfanumérico del número de identificación estándar de Amazon (ASIN) de 10 caracteres asignado al producto por Amazon para la identificación del producto. |
| [!UICONTROL Amazon Value] | Indica el valor del atributo seleccionado. El valor de Amazon difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto mientras que `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor Amazon. |
| [!UICONTROL Status] | Indica si los valores de atributo se han importado en [!DNL Commerce] y está vinculado a [!DNL Commerce] atributo. Opciones: `Not Imported` / `Imported` |
