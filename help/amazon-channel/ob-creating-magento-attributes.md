---
title: Crear [!DNL Commerce] Atributos para Amazon
description: Antes de completar el proceso de incorporación del canal de ventas de Amazon, asegúrese de que tiene lo necesario [!UICONTROL Commerce] atributos del producto.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Crear [!DNL Commerce] atributos para Amazon

Antes de incorporar su [!DNL Amazon Seller Central] es recomendable agregar [!DNL Commerce] [atributos del producto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;} para asignar las listas de productos. Una vez completada la incorporación, puede administrar los atributos de producto mediante la variable [Atributos](./managing-attributes.md) de la pestaña [Inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página.

Estas instrucciones detallan cómo crear [!DNL Commerce] atributos para Amazon ASIN y Amazon Condition. Se recomienda crear atributos adicionales, incluidos Amazon EAN, Amazon ISBN y Amazon UPC. También es posible que desee crear un atributo de precio de Amazon si desea usar el precio de anuncio de Amazon como fuente de precios para las reglas de precios. Estos atributos se utilizan al configurar los precios y las listas durante la incorporación. Utilice también estos atributos al crear listas de Amazon y al actualizar y sincronizar [!DNL Commerce] catálogo con tus anuncios de Amazon.

La configuración de Búsqueda en el catálogo le permite establecer parámetros de búsqueda coincidentes que ayudan a asignar los elegibles [!DNL Commerce] productos con listas de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

La definición de estos valores aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de hacer coincidir manualmente las listas de productos más adelante. Añadir los atributos como parte de la incorporación [tareas previas a la configuración](./amazon-pre-setup-tasks.md), el canal de ventas de Amazon tiene un mayor potencial para emparejar automáticamente sus productos durante la incorporación y sincronización de datos de productos entre Amazon y [!DNL Commerce] después de la incorporación.

Si solo crea el atributo Amazon ASIN (sin añadir valores ASIN por producto), su [!DNL Commerce] es posible que los productos no coincidan automáticamente con sus anuncios de Amazon. Puede hacer coincidir manualmente los productos mediante _Revisión de la tienda_. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si actualiza un ASIN, UPC u otro elemento de datos para un producto que coincida manualmente, debe actualizar los datos en ambos lugares: your [!DNL Commerce] catálogo y el listado en su [!DNL Amazon Seller Central] cuenta.

## Creación del atributo de producto Amazon ASIN

1. Inicie sesión en su [!DNL Commerce] Administrador.

1. Haga clic en **[!UICONTROL Stores]** en el menú de la izquierda.

1. En el _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades de los atributos, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon ASIN` (el nombre del atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Text Field`.

1. Para **[!UICONTROL Values Required]**, elija `No`.

   Aunque se necesita un Amazon ASIN para enumerar un producto en Amazon, es posible que algunos de los productos del catálogo no estén enumerados en Amazon.

1. Expanda el _[!UICONTROL Advanced Attribute Properties]_y establezca las opciones:

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_asin`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo Amazon ASIN](assets/creating-asin-attribute.png)

## Creación del atributo de producto Amazon Condition

1. Inicie sesión en su [!DNL Commerce] Administrador.

1. Haga clic en **[!UICONTROL Stores]** en el menú de la izquierda.

1. En el _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades del atributo, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon Condition` (el nombre del atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Dropdown`.

   La variable _[!UICONTROL Manage Options (Values of your Attribute)]_aparece.

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

1. Seleccione el **[!UICONTROL Is Default]** para la condición que desea que sea la selección predeterminada.

1. En el _[!UICONTROL Admin]_, introduzca el texto de la etiqueta de la condición que está agregando (por ejemplo, `New`, `Used`y `Used-Like New`)

1. Haga clic en **[!UICONTROL Add Option]** para agregar más opciones, según sea necesario.

1. Expandir _[!UICONTROL Advanced Attribute Properties]_y establezca las opciones.

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_condition`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo Condición de Amazon](assets/creating-amazon-condition-attribute.png)

![Icono Siguiente](assets/btn-next.png) [**Continuar agregando o verificando clave de API**](./amazon-verify-api-key.md)
