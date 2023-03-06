---
title: Administrar atributos
description: Puede administrar la asignación de atributos de producto de Commerce a atributos de Amazon para garantizar una información de producto precisa entre los sistemas.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Administrar atributos

AMAZON y [!DNL Commerce] ambos utilizan un sistema de propiedades de producto, conocido como atributos, que se utiliza para definir un producto. Los atributos definen la descripción, el contenido, las imágenes, los precios y los distintos datos de los productos.

Una comunicación correcta entre Commerce y Amazon requiere lo siguiente [!DNL Commerce] Los atributos de se pueden asignar (o hacer coincidir) correctamente al atributo de Amazon correspondiente. Al integrar con Amazon, estos atributos se asignan a atributos de Amazon. Una vez finalizado, [!DNL Commerce] puede sincronizar y mantener tus anuncios de Amazon con tu [!DNL Commerce] catálogo de productos.

Por ejemplo, imagine que tiene el mismo elemento en su [!DNL Commerce] catálogos y listados de Amazon. Un atributo para el producto puede ser el precio de listado del artículo. El nombre del precio de listado en [!DNL Commerce] podría tener nombre `Price`, mientras que el precio de venta de Amazon puede tener el nombre `ListingPrice`. Debe instruir [!DNL Commerce] que, al comunicarse con Amazon, la variable [!DNL Commerce] atributo denominado `Price` es el mismo que el atributo de Amazon denominado `ListingPrice`. Este proceso se llama _administración de atributos_ e incluye la creación de nuevos atributos y la edición de los existentes. Asegurarse de que los atributos coinciden correctamente garantiza una comunicación correcta entre [!DNL Commerce] y Amazon.

Cuando se configura la asignación de atributos, [!DNL Commerce] puede comunicar información del producto con Amazon de un lado a otro. Si tiene listados de productos de Amazon, [!DNL Commerce] puede importar los productos y detalles de Amazon en su [!DNL Commerce] catálogo, que permite administrar los anuncios de Amazon desde un único catálogo central de productos.

El canal de ventas de Amazon le permite acceder, revisar, crear y administrar atributos, según sea necesario, en la [_[!UICONTROL Attributes]_vista](./attributes-view.md) en la página de inicio del canal de ventas de Amazon. Si agrega un atributo a su [!DNL Commerce] catálogo, podría requerir una actualización de esos valores en todos los productos.

Para obtener más información acerca de [!DNL Commerce] y los conjuntos de atributos y valores de Amazon; consulte:

- [Administrar conceptos básicos de atributos](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}
- [Crear un atributo](./creating-attributes.md#create-an-attribute)
- [Editar un atributo existente](./creating-attributes.md#edit-an-attribute)
- [Ver asignación de atributos](./amazon-matching-attributes-values.md)
- [Editar o crear asignación de atributos](./amazon-manually-update-incomplete-listing.md)
