---
title: Crear un SKU de vendedor de Amazon de alias
description: Puede usar el SKU del vendedor de Alias Amazon para crear anuncios de Amazon multirregionales a partir de los productos del catálogo de Commerce.
feature: Sales Channels, Products
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# Crear un SKU de vendedor de Amazon de alias

Se usa un [!DNL Alias Amazon Seller SKU] para crear un anuncio de Amazon a partir del mismo producto en el catálogo [!DNL Commerce]. Si tienes experiencia como vendedor de Amazon, es posible que estés familiarizado con el [SKU global de Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} y el SKU específico del mercado para inventario y envío. Siguiendo principios similares para el canal de ventas de Amazon, la SKU del vendedor de Amazon controla la información de la lista de productos en un nivel multiregional y [!DNL Alias Amazon Seller SKU] se puede usar para controlar la información de la lista de productos en un nivel específico de la región.

Esta función se puede utilizar para realizar dos funciones:

- Cree un(a) [!DNL Alias Amazon Seller SKU] para uno de sus [!DNL Commerce] productos de catálogo a fin de controlar la información de listado específica de la región.

  **Ejemplo**: Usted es un vendedor en las regiones de Estados Unidos y Canadá. Recuerde que a cada una de las tiendas de canales de ventas de Amazon solo se le puede asignar una región de Amazon durante la configuración. Por lo tanto, tiene un almacén de canal de ventas de Amazon con una región de EE. UU. definida y otro con una región de Canadá definida. Ambas tiendas comparten tu catálogo [!DNL Commerce] para obtener información de listados en ambas regiones, incluidos los atributos de producto ASIN y SKU del vendedor de Amazon. Por lo tanto, los listados del producto del catálogo serían los mismos en ambas tiendas, compartiendo precios, stock/cantidad y otros atributos del producto. Sin embargo, sus existencias para su tienda de Canadá se envían desde una ubicación de Canadá, y su tienda de EE. UU. se envía desde una ubicación de EE. UU. Por lo tanto, debe controlar la cantidad del anuncio por separado para cada tienda. Para lograr este tipo de control específico de la región, puede crear un SKU de vendedor de alias de Amazon.

  Básicamente, puede crear un SKU de vendedor de Amazon de alias que esté vinculado al mismo producto del catálogo y que pueda utilizarse para volver a publicar el mismo anuncio en esa región.

- Cree un [!DNL Alias Amazon Seller SKU] y combine uno de los productos del catálogo [!DNL Commerce] con dos anuncios de Amazon.

  **Ejemplo**: Tiene un producto de catálogo que coincide con un listado de Amazon. Como Amazon tiene con frecuencia varios anuncios que representan el mismo producto, se descubre otro anuncio de Amazon para el mismo producto, pero Amazon le ha asignado un ASIN diferente. Para aumentar la visibilidad del producto e incluir, debe hacer coincidir el producto del catálogo con los distintos ASIN y crear listados para ambos valores ASIN. Para ello, puede crear un SKU de vendedor de alias de Amazon.

  Básicamente, puede crear un(a) [!DNL Alias Amazon Seller SKU] que se pueda usar para hacer coincidir un único producto de catálogo con un segundo listado de Amazon y crear un listado para el ASIN que acaba de coincidir. En esta situación, tendría dos anuncios de Amazon para el mismo producto de catálogo.

  Después de crear un SKU de vendedor de alias de Amazon, puedes usar la configuración del anuncio, las reglas y las invalidaciones para controlar la información del anuncio de la región. Los atributos de producto que se pueden definir por región para un listado incluyen la cantidad/stock, el método de cumplimiento, la condición, la idoneidad del producto y el tiempo de manipulación.

## Se utiliza para un propósito específico de la región {#region-specific}

Ver el listado en la página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _Activo_, _No apto_ o _Finalizado_).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, escriba un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, no realice ningún cambio.

   Este valor se rellena automáticamente con el ASIN del producto que coincide con el producto del catálogo. Si cambia este valor, coincidirá con el producto del catálogo en dos anuncios de Amazon basados en el ASIN.

1. Cambie la opción **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes`: elige eliminar el anuncio y crear uno con la nueva información proporcionada.

   - `No`: elige crear un anuncio y mantener el anuncio anterior sin cambios.

1. Haga clic en **[!UICONTROL Save Listing Update]**.

## Se utiliza para combinar un único producto de catálogo con dos anuncios de Amazon

1. Ver el listado en la página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_ o _[!UICONTROL Ended]_fichas).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, escriba un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, escriba un valor alfanumérico único.

   Este valor se rellena automáticamente con el ASIN del producto que coincide con el producto del catálogo. Si cambia este valor, coincidirá con el producto del catálogo en dos anuncios de Amazon basados en el ASIN.

1. Cambie la opción **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes`: elige eliminar el anuncio y crear uno con la nueva información proporcionada.

   - `No`: elige crear otro anuncio y mantener el anuncio anterior sin cambios.

1. Haga clic en **[!UICONTROL Save Listing Update]**.

![crear un SKU de vendedor de Amazon de alias](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| Campo | Descripción |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | Introduce un nuevo valor alfanumérico único para vincularlo al SKU original del vendedor de Amazon. Este número solo lo utiliza el canal de ventas de Amazon para coincidir con el producto del catálogo. Puede utilizar cualquier valor SKU, pero el valor solo se puede utilizar una vez en el catálogo. |
| [!UICONTROL Assign New ASIN] | Introduzca el valor ASIN para el listado con el que desea hacer coincidir el producto del catálogo. Modifique este campo únicamente cuando combine un único producto de catálogo con el ASIN para otro listado del mismo producto. Este valor debe coincidir con el ASIN asignado por Amazon; de lo contrario, el listado no será rechazado por Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Opciones:<ul><li>**[!UICONTROL Yes]**: elige eliminar el anuncio y crear uno con la nueva información proporcionada. El nuevo listado aparece en la ficha _[!UICONTROL Active]_y el listado anterior se mueve a la ficha_ Finalizado _.</li><li>**[!UICONTROL No]**: elige crear otro anuncio y mantener el anuncio anterior sin cambios. Ambos anuncios aparecen en la ficha Activo después de crear el nuevo anuncio.</li></ul> |
