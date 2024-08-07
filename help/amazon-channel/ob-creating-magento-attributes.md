---
title: Crear atributos de Commerce para Amazon
description: Antes de completar el proceso de incorporación al canal de ventas de Amazon, asegúrese de que dispone de los atributos de producto de [!UICONTROL Commerce] necesarios.
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Crear atributos de Commerce para Amazon

Antes de incorporar tus cuentas de [!DNL Amazon Seller Central], se recomienda agregar [!DNL Commerce] [atributos de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) para asignar tus listas de productos. Una vez que hayas completado la incorporación, puedes administrar los atributos de tus productos a través de la pestaña [Atributos](./managing-attributes.md) de la página de inicio de [canal de ventas de Amazon](./amazon-sales-channel-home.md).

Estas instrucciones detallan cómo crear atributos de [!DNL Commerce] para Amazon ASIN y la condición de Amazon. Se recomienda crear atributos adicionales, incluidos Amazon EAN, Amazon ISBN y Amazon UPC. También puede crear un atributo Precio de Amazon si desea utilizar el precio de listado de Amazon como fuente de precios para las reglas de asignación de precios. Estos atributos se utilizan para configurar los anuncios y los precios durante la incorporación. Utilice también estos atributos al crear anuncios de Amazon y al actualizar y sincronizar el catálogo [!DNL Commerce] con los anuncios de Amazon.

La configuración de Búsqueda en el catálogo permite establecer parámetros de búsqueda coincidentes que ayuden a asignar los productos aptos de [!DNL Commerce] con los listados de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

Definir estos valores aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de hacer coincidir manualmente las listas de productos más adelante. Si agrega los atributos como parte de sus [tareas previas a la configuración](./amazon-pre-setup-tasks.md) de incorporación, el canal de ventas de Amazon tiene un mayor potencial para hacer coincidir automáticamente sus productos durante la incorporación y sincroniza los datos de productos entre Amazon y [!DNL Commerce] después de la incorporación.

Si solo crea el atributo ASIN de Amazon (sin agregar valores ASIN por producto), es posible que los productos [!DNL Commerce] no coincidan automáticamente con los listados de Amazon. Puedes hacer coincidir manualmente tus productos con _Revisión de tienda_. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si actualiza un ASIN, UPC u otro elemento de datos para un producto que coincida manualmente, debe actualizar los datos en ambos lugares: el catálogo [!DNL Commerce] y el listado en la cuenta [!DNL Amazon Seller Central].

## Cree el atributo de producto ASIN de Amazon

1. Inicie sesión en su administrador de [!DNL Commerce].

1. Haga clic en **[!UICONTROL Stores]** en el menú del lado izquierdo.

1. En la sección _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades de los atributos, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, escriba `Amazon ASIN` (el nombre de su atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Text Field`.

1. Para **[!UICONTROL Values Required]**, elija `No`.

   Aunque se requiere un ASIN de Amazon para enumerar un producto en Amazon, es posible que algunos de los productos del catálogo no estén enumerados en Amazon.

1. Expanda la sección _[!UICONTROL Advanced Attribute Properties]_y defina las opciones:

   - Para **[!UICONTROL Attribute Code]**, escriba `amazon_asin`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo ASIN de Amazon](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## Cree el atributo de producto Condición de Amazon

1. Inicie sesión en su administrador de [!DNL Commerce].

1. Haga clic en **[!UICONTROL Stores]** en el menú del lado izquierdo.

1. En la sección _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades del atributo, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, escriba `Amazon Condition` (el nombre de su atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Dropdown`.

   Aparecerá la sección _[!UICONTROL Manage Options (Values of your Attribute)]_.

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

1. En la columna _[!UICONTROL Admin]_, escriba el texto de la etiqueta de la condición que está agregando (como `New`, `Used` y `Used-Like New`)

1. Haga clic en **[!UICONTROL Add Option]** para agregar más opciones, según sea necesario.

1. Expanda la sección _[!UICONTROL Advanced Attribute Properties]_y defina las opciones.

   - Para **[!UICONTROL Attribute Code]**, escriba `amazon_condition`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Haga clic en **[!UICONTROL Save Attribute]**.

![Atributo de condición de Amazon](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![Siguiente icono](assets/btn-next.png) [**Continúe agregando o verificando la clave de API**](./amazon-verify-api-key.md)
