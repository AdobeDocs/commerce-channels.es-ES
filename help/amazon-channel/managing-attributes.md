---
title: Administrar atributos
description: Puede administrar la asignación de atributos de producto de Commerce a los atributos de Amazon para garantizar una información precisa del producto entre los sistemas.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Administrar atributos

Tanto Amazon como [!DNL Commerce] utilizan un sistema de propiedades de producto, conocidas como atributos, que se utiliza para definir un producto. Los atributos definen la descripción, el contenido, las imágenes, los precios y los distintos datos de sus productos.

La comunicación correcta entre Commerce y Amazon requiere que los atributos [!DNL Commerce] se asignen (o coincidan) correctamente al atributo correspondiente de Amazon. Al integrar con Amazon, se asignan estos atributos a los atributos de Amazon. Cuando esté completo, [!DNL Commerce] puede sincronizar y mantener sus listados de Amazon con su catálogo de productos [!DNL Commerce].

Por ejemplo, imaginemos que tiene el mismo artículo en el catálogo de [!DNL Commerce] y en las listas de Amazon. Un atributo para el producto puede ser el precio de venta del artículo. El nombre del precio del anuncio en [!DNL Commerce] puede tener el nombre `Price`, mientras que el precio del anuncio para Amazon puede tener el nombre `ListingPrice`. Debe indicar a [!DNL Commerce] que al comunicarse con Amazon, el atributo [!DNL Commerce] denominado `Price` es el mismo que el atributo de Amazon denominado `ListingPrice`. Este proceso se denomina _administración de atributos_ e incluye la creación de atributos nuevos y la edición de atributos existentes. Asegúrese de que los atributos coinciden correctamente y garantiza una comunicación correcta entre [!DNL Commerce] y Amazon.

Cuando se configura la asignación de atributos, [!DNL Commerce] puede comunicar información del producto de un lado a otro con Amazon. Si tiene listados de productos de Amazon, [!DNL Commerce] puede importar sus productos y detalles de Amazon en su catálogo [!DNL Commerce], lo que le permite administrar sus listados de Amazon desde un único catálogo central de productos.

El canal de ventas de Amazon le permite acceder, revisar, crear y administrar atributos, según sea necesario, en la [_[!UICONTROL Attributes]_vista](./attributes-view.md) de la página de inicio del canal de ventas de Amazon. Si agrega un atributo al catálogo [!DNL Commerce], podría requerir una actualización de esos valores en todos los productos.

Para obtener más información sobre los conjuntos y valores de atributos [!DNL Commerce] y Amazon, consulte:

- [Administrar conceptos básicos de atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Crear un atributo](./creating-attributes.md#create-an-attribute)
- [Editar un atributo existente](./creating-attributes.md#edit-an-attribute)
- [Ver asignación de atributos](./amazon-matching-attributes-values.md)
- [Editar o crear asignación de atributos](./amazon-manually-update-incomplete-listing.md)
