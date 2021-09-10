---
title: Crear un SKU de vendedor de Amazon de alias
description: Puede usar el SKU de vendedor de Amazon de alias para crear anuncios de Amazon multiregionales a partir de los productos del catálogo de comercio.
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Crear un SKU de vendedor de Amazon de alias

Se utiliza un [!DNL Alias Amazon Seller SKU] para crear un listado de Amazon a partir del mismo producto en su catálogo [!DNL Commerce]. Si es un vendedor experimentado de Amazon, es posible que esté familiarizado con el [SKU global de Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target=&quot;_blank&quot;} y el SKU específico de Marketplace para inventario y envío. Siguiendo principios similares para el canal de ventas de Amazon, el SKU del vendedor de Amazon controla la información de la lista de productos a nivel multiregional, y el [!DNL Alias Amazon Seller SKU] puede utilizarse para controlar la información de la lista de productos a nivel específico de la región.

Esta función se puede utilizar para realizar dos funciones:

- Cree un [!DNL Alias Amazon Seller SKU] para uno de sus [!DNL Commerce] productos de catálogo para controlar la información de listado específica de la región.

   **Ejemplo**: Eres vendedor en las regiones de Estados Unidos y Canadá. Recuerde que a cada una de las tiendas de canales de ventas de Amazon solo se le puede asignar una región de Amazon durante la configuración. Por lo tanto, tiene un almacén de canales de ventas de Amazon con una región de EE. UU. definida y otra tienda con una región de Canadá definida. Ambas tiendas comparten su [!DNL Commerce] catálogo para obtener información sobre las listas en ambas regiones, incluidos el SKU del vendedor de Amazon y los atributos de producto ASIN. Por lo tanto, los anuncios del producto del catálogo serían los mismos en ambas tiendas, compartiendo precios, stock/cantidad y otros atributos del producto. Pero, sus existencias para Canadá almacenan barcos desde una ubicación de Canadá, y los de EE. UU. desde una ubicación de EE. UU. Por lo tanto, debe controlar la cantidad de listado por separado para cada almacén. Para realizar este tipo de control específico de la región, puede crear un SKU de vendedor de Amazon de alias.

   Esencialmente, puede crear una SKU de vendedor de Amazon de alias vinculada al mismo producto de catálogo y que se puede usar para volver a publicar la misma oferta en esa región.

- Cree un [!DNL Alias Amazon Seller SKU] y haga coincidir uno de sus productos de catálogo [!DNL Commerce] con dos anuncios de Amazon.

   **Ejemplo**: Tiene un producto de catálogo que coincide con un listado de Amazon. Como Amazon tiene con frecuencia varias listas que representan el mismo producto, descubre otra lista de Amazon para el mismo producto, pero Amazon ha asignado un ASIN diferente a la lista. Para aumentar la visibilidad del producto para incluir, debe buscar coincidencias entre el producto del catálogo y los distintos ASIN y crear listas para ambos valores ASIN. Para ello, puede crear un SKU de vendedor de Amazon de alias.

   Esencialmente, puede crear un [!DNL Alias Amazon Seller SKU] que se pueda usar para hacer coincidir un producto de catálogo único con un segundo anuncio de Amazon y crear un listado para el ASIN que acaba de coincidir. En esta situación, tendría dos listas de Amazon para el mismo producto de catálogo.

   Después de crear un SKU de vendedor de Amazon de alias, puede usar la configuración de la lista, las reglas y las anulaciones para controlar la información de la lista de la región. Los atributos de producto que se pueden definir por región para una lista incluyen cantidad/stock, método de cumplimiento, condición, idoneidad del producto y tiempo de manipulación.

## Se utiliza para un propósito específico de la región. {#region-specific}

Vea el listado en la página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _Activo_, _Inelegible_ o _Terminado_).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, introduzca un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, no realice ningún cambio.

   Este valor se rellena automáticamente con el ASIN de producto que coincide con el producto del catálogo. Si se cambia este valor, el producto del catálogo se ajustará a dos listas de Amazon basadas en el ASIN.

1. Cambie la opción **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes` - Elige eliminar el listado y crear un listado usando la nueva información proporcionada.

   - `No` - Elige crear una lista y mantener la lista antigua sin cambios.

1. Haga clic en **[!UICONTROL Save Listing Update]**.

## Se utiliza para hacer coincidir un producto de catálogo único con dos listas de Amazon.

1. Vea el listado en la página _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_ o _[!UICONTROL Ended]_pestañas).

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Create Alias Seller SKU]**.

1. Para **[!UICONTROL Assign New Seller SKU]**, introduzca un valor alfanumérico único.

   Este valor debe ser único (no se utiliza para ningún otro producto o alias del catálogo).

1. Para **[!UICONTROL Assign New ASIN]**, introduzca un valor alfanumérico único.

   Este valor se rellena automáticamente con el ASIN de producto que coincide con el producto del catálogo. Si se cambia este valor, el producto del catálogo se ajustará a dos listas de Amazon basadas en el ASIN.

1. Cambie la opción **[!UICONTROL Remove Existing Seller SKU]** según sea necesario.

   - `Yes` - Elige eliminar el listado y crear un listado usando la nueva información proporcionada.

   - `No` - Elige crear otro listado y mantener el listado antiguo sin cambios.

1. Haga clic en **[!UICONTROL Save Listing Update]**.

![crear un SKU de vendedor de Amazon de alias](assets/amazon-alias-sku-create.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | Introduzca un nuevo valor alfanumérico único que se vinculará al SKU original del vendedor de Amazon. Este número solo lo usa el canal de ventas de Amazon para coincidir con el producto del catálogo. Puede usar cualquier valor de SKU, pero el valor solo se puede usar una vez en el catálogo. |
| [!UICONTROL Assign New ASIN] | Introduzca el valor ASIN del listado con el que desea coincidir el producto del catálogo. Modifique este campo únicamente al hacer coincidir un producto de catálogo único con el ASIN para otra lista del mismo producto. Este valor debe coincidir con el ASIN asignado por Amazon o Amazon no rechazará el listado. |
| [!UICONTROL Remove Existing Seller SKU] | Opciones:<ul><li>**[!UICONTROL Yes]** - Elige eliminar el listado y crear un listado usando la nueva información proporcionada. El nuevo listado aparece en la pestaña _[!UICONTROL Active]_y el listado antiguo se mueve a la pestaña_ Ended _.</li><li>**[!UICONTROL No]** - Elige crear otro listado y mantener el listado antiguo sin cambios. Ambas listas aparecen en la pestaña Activo después de crear la nueva lista.</li></ul> |
