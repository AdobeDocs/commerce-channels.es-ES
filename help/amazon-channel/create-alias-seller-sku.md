---
title: Crear un SKU de vendedor de Amazon de alias
description: Puede usar el SKU del vendedor de Alias Amazon para crear anuncios de Amazon multirregionales a partir de los productos del catálogo de Commerce.
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Crear un SKU de vendedor de Amazon de alias

Un [!DNL Alias Amazon Seller SKU] se utiliza para crear un anuncio de Amazon a partir del mismo producto en su [!DNL Commerce] catálogo. Si tienes experiencia como vendedor de Amazon, es posible que estés familiarizado con el [SKU global de Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} y SKU específicas del mercado para inventario y envío. Siguiendo principios similares para el canal de ventas de Amazon, el SKU del vendedor de Amazon controla la información de la lista de productos en el nivel multiregional, y la variable [!DNL Alias Amazon Seller SKU] se puede utilizar para controlar la información de la lista de productos en un nivel específico de la región.

Esta función se puede utilizar para realizar dos funciones:

- Crear un [!DNL Alias Amazon Seller SKU] para uno de sus [!DNL Commerce] catálogo de productos para controlar la información de listado específica de la región.

   **Ejemplo**: Usted es un vendedor en las regiones de Estados Unidos y Canadá. Recuerde que a cada una de las tiendas de canales de ventas de Amazon solo se le puede asignar una región de Amazon durante la configuración. Por lo tanto, tiene un almacén de canal de ventas de Amazon con una región de EE. UU. definida y otro con una región de Canadá definida. Ambas tiendas comparten su [!DNL Commerce] catálogo para obtener información de listado en ambas regiones, incluidos los atributos de producto ASIN y SKU del vendedor de Amazon. Por lo tanto, los listados del producto del catálogo serían los mismos en ambas tiendas, compartiendo precios, stock/cantidad y otros atributos del producto. Sin embargo, sus existencias para su tienda de Canadá se envían desde una ubicación de Canadá, y su tienda de EE. UU. se envía desde una ubicación de EE. UU. Por lo tanto, debe controlar la cantidad del anuncio por separado para cada tienda. Para lograr este tipo de control específico de la región, puede crear un SKU de vendedor de alias de Amazon.

   Básicamente, puede crear un SKU de vendedor de Amazon de alias que esté vinculado al mismo producto del catálogo y que pueda utilizarse para volver a publicar el mismo anuncio en esa región.

- Crear un [!DNL Alias Amazon Seller SKU] y coincida con uno de sus [!DNL Commerce] catalogar productos en dos anuncios de Amazon.

   **Ejemplo**: Tiene un producto de catálogo que coincide con un listado de Amazon. Como Amazon tiene con frecuencia varios anuncios que representan el mismo producto, se descubre otro anuncio de Amazon para el mismo producto, pero Amazon le ha asignado un ASIN diferente. Para aumentar la visibilidad del producto e incluir, debe hacer coincidir el producto del catálogo con los distintos ASIN y crear listados para ambos valores ASIN. Para ello, puede crear un SKU de vendedor de alias de Amazon.

   Básicamente, puede crear un [!DNL Alias Amazon Seller SKU] que se puede utilizar para hacer coincidir un único producto de catálogo con un segundo listado de Amazon y crear un listado para el ASIN recién coincidente. En esta situación, tendría dos anuncios de Amazon para el mismo producto de catálogo.

   Después de crear un SKU de vendedor de alias de Amazon, puedes usar la configuración del anuncio, las reglas y las invalidaciones para controlar la información del anuncio de la región. Los atributos de producto que se pueden definir por región para un listado incluyen la cantidad/stock, el método de cumplimiento, la condición, la idoneidad del producto y el tiempo de manipulación.

## Se utiliza para un propósito específico de la región {#region-specific}

Ver el anuncio en la _[!UICONTROL Product Listings]_página (_[!UICONTROL Inactive]_, _Activo_, _No apto_, o _Finalizado_ pestaña).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, introduzca un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, no realice ningún cambio.

   Este valor se rellena automáticamente con el ASIN del producto que coincide con el producto del catálogo. Si cambia este valor, coincidirá con el producto del catálogo en dos anuncios de Amazon basados en el ASIN.

1. Alternar el **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes` - Elige eliminar el anuncio y crear un anuncio con la nueva información proporcionada.

   - `No` : elige crear un anuncio y mantener el anuncio anterior sin cambios.

1. Clic **[!UICONTROL Save Listing Update]**.

## Se utiliza para combinar un único producto de catálogo con dos anuncios de Amazon

1. Ver el anuncio en la _[!UICONTROL Product Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_, o _[!UICONTROL Ended]_pestañas).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, introduzca un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, introduzca un valor alfanumérico único.

   Este valor se rellena automáticamente con el ASIN del producto que coincide con el producto del catálogo. Si cambia este valor, coincidirá con el producto del catálogo en dos anuncios de Amazon basados en el ASIN.

1. Alternar el **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes` - Elige eliminar el anuncio y crear un anuncio con la nueva información proporcionada.

   - `No` - Elige crear otro anuncio y mantener el anterior sin cambios.

1. Clic **[!UICONTROL Save Listing Update]**.

![crear un SKU de vendedor de Amazon de alias](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | Introduce un nuevo valor alfanumérico único para vincularlo al SKU original del vendedor de Amazon. Este número solo lo utiliza el canal de ventas de Amazon para coincidir con el producto del catálogo. Puede utilizar cualquier valor SKU, pero el valor solo se puede utilizar una vez en el catálogo. |
| [!UICONTROL Assign New ASIN] | Introduzca el valor ASIN para el listado con el que desea hacer coincidir el producto del catálogo. Modifique este campo únicamente cuando combine un único producto de catálogo con el ASIN para otro listado del mismo producto. Este valor debe coincidir con el ASIN asignado por Amazon; de lo contrario, el listado no será rechazado por Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Opciones:<ul><li>**[!UICONTROL Yes]** - Elige eliminar el anuncio y crear un anuncio con la nueva información proporcionada. El nuevo listado aparece en la _[!UICONTROL Active]_y el anuncio antiguo pasa a la pestaña_ Finalizado _pestaña.</li><li>**[!UICONTROL No]** - Elige crear otro anuncio y mantener el anterior sin cambios. Ambos anuncios aparecen en la ficha Activo después de crear el nuevo anuncio.</li></ul> |
