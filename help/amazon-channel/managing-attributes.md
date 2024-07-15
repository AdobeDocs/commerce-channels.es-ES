---
title: Administrar atributos para listados de Amazon
description: Puede administrar la asignación de atributos de producto de Commerce a los atributos de Amazon para garantizar una información de producto precisa entre los sistemas.
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Administrar atributos para listados de Amazon

Amazon y [!DNL Commerce] utilizan un sistema de propiedades de producto, conocidas como atributos, que se usa para definir un producto. Los atributos definen la descripción, el contenido, las imágenes, los precios y los distintos datos de los productos.

La comunicación correcta entre Commerce y Amazon requiere que los atributos de [!DNL Commerce] se asignen (o coincidan) correctamente al atributo de Amazon correspondiente. Al integrar con Amazon, estos atributos se asignan a atributos de Amazon. Una vez finalizado, [!DNL Commerce] podrá sincronizar y mantener sus anuncios de Amazon con el catálogo de productos [!DNL Commerce].

Por ejemplo, imagine que tiene el mismo artículo en el catálogo [!DNL Commerce] y en los anuncios de Amazon. Un atributo para el producto puede ser el precio de listado del artículo. El nombre del precio de listado en [!DNL Commerce] podría ser `Price`, mientras que el precio de listado de Amazon podría ser `ListingPrice`. Debe indicar a [!DNL Commerce] que al comunicarse con Amazon, el atributo [!DNL Commerce] denominado `Price` es el mismo que el atributo Amazon denominado `ListingPrice`. Este proceso se denomina _administrar atributos_ e incluye la creación y edición de atributos existentes. Asegurarse de que los atributos coinciden correctamente garantiza la comunicación correcta entre [!DNL Commerce] y Amazon.

Cuando se configura la asignación de atributos, [!DNL Commerce] puede comunicar la información del producto con Amazon de un lado a otro. Si tienes listados de productos de Amazon, [!DNL Commerce] puede importar tus productos y detalles de Amazon en tu catálogo [!DNL Commerce], lo que te permite administrar tus listados de Amazon desde un único catálogo central de productos.

el canal de ventas de Amazon le permite acceder, revisar, crear y administrar atributos, según sea necesario, en la vista [_[!UICONTROL Attributes]_](./attributes-view.md) de la página de inicio del canal de ventas de Amazon. Si agrega un atributo al catálogo [!DNL Commerce], podría requerir una actualización de esos valores en todos los productos.

Para obtener más información sobre [!DNL Commerce] y los conjuntos de atributos y valores de Amazon, consulte:

- [Administrar conceptos básicos de atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Crear un atributo](./creating-attributes.md#create-an-attribute)
- [Editar un atributo existente](./creating-attributes.md#edit-an-attribute)
- [Ver asignación de atributos](./amazon-matching-attributes-values.md)
- [Editar o crear asignación de atributos](./amazon-manually-update-incomplete-listing.md)
