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

Amazon y [!DNL Commerce] ambos utilizan un sistema de propiedades de producto, conocidas como atributos, utilizado para definir un producto. Los atributos definen la descripción, el contenido, las imágenes, los precios y los distintos datos de sus productos.

La comunicación correcta entre Commerce y Amazon requiere que [!DNL Commerce] Los atributos de se asignarán correctamente (o coincidirán) al atributo de Amazon correspondiente. Al integrar con Amazon, se asignan estos atributos a los atributos de Amazon. Cuando termine, [!DNL Commerce] puede sincronizar y mantener sus listados de Amazon con su [!DNL Commerce] catálogo de productos.

Por ejemplo, imagine que tiene el mismo elemento en su [!DNL Commerce] catálogo y anuncios de Amazon. Un atributo para el producto puede ser el precio de venta del artículo. El nombre del precio del anuncio en [!DNL Commerce] puede tener el nombre `Price`, mientras que el precio del anuncio para Amazon puede tener el nombre `ListingPrice`. Debe indicar [!DNL Commerce] que cuando se comunica con Amazon, la variable [!DNL Commerce] atributo llamado `Price` es el mismo que el atributo de Amazon llamado `ListingPrice`. Este proceso se denomina _administración de atributos_, e incluye la creación de atributos nuevos y la edición de atributos existentes. Asegurarse de que los atributos estén correctamente coincidentes garantiza una comunicación correcta entre [!DNL Commerce] y Amazon.

Cuando se configura la asignación de atributos, [!DNL Commerce] puede comunicar información del producto de un lado a otro con Amazon. Si tiene listas de productos de Amazon, [!DNL Commerce] puede importar sus productos y detalles de Amazon en su [!DNL Commerce] , lo que le permite administrar sus listados de Amazon desde un único catálogo central de productos.

El canal de ventas de Amazon le permite acceder, revisar, crear y administrar atributos, según sea necesario, en la variable [_[!UICONTROL Attributes]_ver](./attributes-view.md) en la página de inicio del canal de ventas de Amazon. Si agrega un atributo a su [!DNL Commerce] catálogo, podría requerir una actualización de esos valores en todos los productos.

Para obtener más información, consulte [!DNL Commerce] y los valores y conjuntos de atributos de Amazon, consulte:

- [Conceptos básicos de administración de atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Crear un atributo](./creating-attributes.md#create-an-attribute)
- [Editar un atributo existente](./creating-attributes.md#edit-an-attribute)
- [Ver asignación de atributos](./amazon-matching-attributes-values.md)
- [Editar o crear asignación de atributos](./amazon-manually-update-incomplete-listing.md)
