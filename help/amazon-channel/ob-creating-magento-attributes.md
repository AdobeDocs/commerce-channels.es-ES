---
title: Creación de atributos  [!DNL Commerce] para Amazon
description: Antes de completar el proceso de incorporación del canal de ventas de Amazon, asegúrese de tener los atributos de producto [!UICONTROL Commerce] necesarios.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Crear atributos [!DNL Commerce] para Amazon

Antes de incorporar sus cuentas de [!DNL Amazon Seller Central], se recomienda agregar [!DNL Commerce] [atributos de producto](https://docs.magento.com/user-guide/stores/attributes-product.html){:target=&quot;_blank&quot;} para asignar sus listas de productos. Después de completar la incorporación, puede administrar los atributos de producto a través de la pestaña [Attributes](./managing-attributes.md) de la página [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md).

Estas instrucciones detallan cómo crear atributos [!DNL Commerce] para Amazon ASIN y Amazon Condition. Se recomienda crear atributos adicionales, incluidos Amazon EAN, Amazon ISBN y Amazon UPC. También es posible que desee crear un atributo de precio de Amazon si desea usar el precio de anuncio de Amazon como fuente de precios para las reglas de precios. Estos atributos se utilizan al configurar los precios y las listas durante la incorporación. Utilice también estos atributos al crear listas de Amazon y al actualizar y sincronizar su catálogo [!DNL Commerce] con sus listas de Amazon.

La configuración de Búsqueda en el catálogo le permite establecer parámetros de búsqueda coincidentes que le ayudarán a asignar productos aptos de [!DNL Commerce] a los listados de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

La definición de estos valores aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de hacer coincidir manualmente las listas de productos más adelante. Si agrega los atributos como parte de las [tareas previas a la configuración](./amazon-pre-setup-tasks.md) de incorporación, el canal de ventas de Amazon tiene un mayor potencial para hacer coincidir automáticamente sus productos durante la incorporación y sincronización de datos de productos entre Amazon y [!DNL Commerce] después de la incorporación.

Si solo crea el atributo Amazon ASIN (sin añadir valores ASIN por producto), es posible que los productos [!DNL Commerce] no coincidan automáticamente con los anuncios de Amazon. Puede hacer coincidir manualmente sus productos mediante _Store Review_. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si actualiza un ASIN, UPC u otro elemento de datos para un producto que coincida manualmente, debe actualizar los datos en ambos lugares: su catálogo [!DNL Commerce] y el listado en su cuenta [!DNL Amazon Seller Central].

## Creación del atributo de producto Amazon ASIN

1. Inicie sesión en su administrador de [!DNL Commerce].

1. Haga clic **[!UICONTROL Stores]** en el menú de la izquierda.

1. En la sección _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades de los atributos, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon ASIN` (el nombre del atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Text Field`.

1. Para **[!UICONTROL Values Required]**, elija `No`.

   Aunque se necesita un Amazon ASIN para enumerar un producto en Amazon, es posible que algunos de los productos del catálogo no estén enumerados en Amazon.

1. Expanda la sección _[!UICONTROL Advanced Attribute Properties]_y defina las opciones:

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_asin`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo Amazon ASIN](assets/creating-asin-attribute.png)

## Creación del atributo de producto Amazon Condition

1. Inicie sesión en su administrador de [!DNL Commerce].

1. Haga clic **[!UICONTROL Stores]** en el menú de la izquierda.

1. En la sección _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades del atributo, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon Condition` (el nombre del atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Dropdown`.

   Aparece la sección _[!UICONTROL Manage Options (Values of your Attribute)]_.

1. Para **[!UICONTROL Values Required]**, elija `No`.

1. Para **[!UICONTROL Manage Options (Values for your Attribute)]**, agregue cada una de las opciones de condición.

   Las condiciones estándar de Amazon incluyen:

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Haga clic en **[!UICONTROL Add Option]**.

1. Seleccione la opción **[!UICONTROL Is Default]** para la condición que desea que sea la selección predeterminada.

1. En la columna _[!UICONTROL Admin]_, introduzca el texto de la etiqueta de la condición que está agregando (como `New`, `Used` y `Used-Like New`)

1. Haga clic en **[!UICONTROL Add Option]** para agregar más opciones, según sea necesario.

1. Expanda la sección _[!UICONTROL Advanced Attribute Properties]_y defina las opciones.

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_condition`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo Condición de Amazon](assets/creating-amazon-condition-attribute.png)

![Siguiente ](assets/btn-next.png) [**iconoContinuar con la adición o verificación de la clave de API**](./amazon-verify-api-key.md)
