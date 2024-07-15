---
title: Ver asignación de atributos de Amazon
description: Compruebe los valores de los atributos de Commerce vinculados para sincronizar correctamente entre Commerce y Amazon.
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Ver asignación de atributos de Amazon

Al asignar atributos de Amazon a atributos de [!DNL Commerce], el canal de ventas de Amazon realiza un seguimiento y proporciona una lista filtrable de todos los valores de Amazon. Utilice esta página para comprobar que los valores de los atributos [!DNL Commerce] vinculados se sincronizan correctamente entre [!DNL Commerce] y Amazon. Puede revisar los valores sincronizados del atributo Amazon enlazado o no enlazado a un atributo [!DNL Commerce]. Para crear o editar los atributos de Amazon, consulte [Crear y editar atributos](./creating-attributes.md).

El _valor de Amazon_ difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto, mientras que `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor Amazon.

## Ver los valores de atributo

1. En la barra lateral _[!UICONTROL Admin]_, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y haga clic en **[!UICONTROL Create]** o **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Haga clic en la ficha **[!UICONTROL Matching Attribute Values]**.

   Los anuncios que tienen un producto de catálogo [!DNL Commerce] correspondiente muestran un valor vinculado en la columna _[!UICONTROL Magento Product SKU]_. Al hacer clic en un vínculo, se abre la página de detalles del producto del catálogo correspondiente. Los cambios en los atributos de Amazon en la página de detalles del producto no se sincronizan con el canal de ventas de Amazon.

>[!TIP]
>Para editar o asignar la asignación de un listado a un producto del catálogo, consulte [Actualizar la información necesaria](./amazon-manually-update-incomplete-listing.md).

![Ver valores de atributo](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Campo | Descripción |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | Región para la actividad de ventas definida en **[!DNL Amazon Marketplace]país** durante la integración de la tienda. |
| [!UICONTROL Magento Product SKU] | Indica los [!DNL Commerce] productos sincronizados con el almacén de Amazon. El valor es un id. de producto asignado por [!DNL Commerce] y vinculado a un producto del catálogo. Para abrir el producto en [!DNL Commerce], haga clic en el vínculo. |
| [!UICONTROL ASIN] | Indica el identificador único alfanumérico del número de identificación estándar de Amazon (ASIN) de 10 caracteres asignado al producto por Amazon para la identificación del producto. |
| [!UICONTROL Amazon Value] | Indica el valor del atributo seleccionado. El valor de Amazon difiere según el tipo de atributo y el atributo de Amazon que visualice. Por ejemplo, un valor de Amazon enumerado para `Label` sería un valor de texto, mientras que `AmazonListPrice` sería una cantidad numérica. El estado indica si se ha importado el valor Amazon. |
| [!UICONTROL Status] | Indica si los valores de atributo se importaron en [!DNL Commerce] y se vincularon a un atributo [!DNL Commerce]. Opciones: `Not Imported` / `Imported` |
