---
title: Ver asignación de atributos de Amazon
description: Compruebe los valores de los atributos de comercio vinculados para que se sincronicen correctamente entre Commerce y Amazon.
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Ver asignación de atributos de Amazon

Al asignar atributos de Amazon a [!DNL Commerce] , el canal de ventas de Amazon realiza un seguimiento y proporciona una lista filtrable de todos los valores de Amazon. Utilice esta página para verificar los valores de los vínculos [!DNL Commerce] los atributos se sincronizan correctamente entre [!DNL Commerce] y Amazon. Puede revisar los valores sincronizados para el atributo Amazon vinculado o no vinculado a un [!DNL Commerce] atributo. Para crear o editar los atributos de Amazon, consulte [Creación y edición de atributos](./creating-attributes.md).

La variable _Valor de Amazon_ difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto mientras `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor de Amazon.

## Ver los valores de atributo

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create]** o **[!UICONTROL Edit]** en el _[!UICONTROL Action]_para abrir el Navegador.

1. Haga clic en el **[!UICONTROL Matching Attribute Values]** pestaña .

   Anuncios que tienen una [!DNL Commerce] el producto catálogo muestra un valor vinculado en la variable _SKU de producto de Magento_ para abrir el Navegador. Al hacer clic en un vínculo, se abre la página de detalles del producto del catálogo correspondiente. Los cambios en los atributos de Amazon en la página de detalles del producto no se sincronizan con el canal de ventas de Amazon.

>[!TIP]
>Para editar o asignar la asignación de una lista a un producto de catálogo, consulte [Actualizar información requerida](./amazon-manually-update-incomplete-listing.md).

![Ver valores de atributo](assets/amazon-managing-attribute-values.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Region] | La región para la actividad de ventas definida en **[!DNL Amazon Marketplace]País** durante la integración del almacén. |
| [!UICONTROL Magento Product SKU] | Indica la variable [!DNL Commerce] productos sincronizados con la tienda de Amazon. El valor es un ID de producto asignado por [!DNL Commerce] y están vinculados a un producto del catálogo. Para abrir el producto en [!DNL Commerce], haga clic en el vínculo . |
| [!UICONTROL ASIN] | Indica el identificador único alfanumérico de 10 caracteres del número de identificación estándar de Amazon (ASIN) asignado al producto por Amazon para la identificación del producto. |
| [!UICONTROL Amazon Value] | Indica el valor del atributo seleccionado. El valor de Amazon difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto mientras `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor de Amazon. |
| [!UICONTROL Status] | Indica si los valores de atributo se han importado en [!DNL Commerce] y vinculados a un [!DNL Commerce] atributo. Opciones: `Not Imported` / `Imported` |
