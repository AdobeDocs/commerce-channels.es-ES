---
title: Crear [!DNL Commerce] Atributos para Amazon
description: Antes de completar el proceso de incorporación al canal de ventas de Amazon, asegúrese de que dispone de los [!UICONTROL Commerce] atributos del producto.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Crear [!DNL Commerce] Atributos para Amazon

Antes de incorporar su [!DNL Amazon Seller Central] cuentas, se recomienda añadir lo siguiente [!DNL Commerce] [atributos del producto](https://docs.magento.com/user-guide/stores/attributes-product.html){target="_blank"} para asignar los listados de productos. Una vez que haya completado la incorporación, puede administrar los atributos del producto mediante las [Atributos](./managing-attributes.md) de la pestaña [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página.

Estas instrucciones detallan cómo crear [!DNL Commerce] atributos para Amazon ASIN y Amazon Condition. Se recomienda crear atributos adicionales, incluidos Amazon EAN, Amazon ISBN y Amazon UPC. También puede crear un atributo Precio de Amazon si desea utilizar el precio de listado de Amazon como fuente de precios para las reglas de asignación de precios. Estos atributos se utilizan para configurar los anuncios y los precios durante la incorporación. Utilice también estos atributos al crear anuncios de Amazon y al actualizar y sincronizar su [!DNL Commerce] con sus anuncios de Amazon.

La configuración de Búsqueda en el catálogo permite establecer parámetros de búsqueda coincidentes que ayuden a asignar elementos aptos [!DNL Commerce] productos con listados de Amazon. Cuando se asigna, Amazon activa acciones relacionadas con los precios, la cantidad, las anulaciones y la sincronización de pedidos y productos.

Definir estos valores aumenta el potencial de coincidencias exactas, lo que minimiza la necesidad de hacer coincidir manualmente las listas de productos más adelante. Adición de los atributos como parte de la incorporación [tareas previas a la configuración](./amazon-pre-setup-tasks.md), el canal de ventas de Amazon tiene un mayor potencial para hacer coincidir automáticamente sus productos durante la incorporación y sincroniza los datos de productos entre Amazon y [!DNL Commerce] después de la incorporación.

Si solo crea el atributo ASIN de Amazon (sin agregar valores ASIN por producto), su [!DNL Commerce] es posible que los productos no coincidan automáticamente con tus anuncios de Amazon. Puede hacer coincidir manualmente sus productos mediante _Crítica de tienda_. Sin embargo, la coincidencia manual no crea los elementos de datos necesarios para compartir y sincronizar los datos del producto.

>[!IMPORTANT]
>
>Si actualiza un ASIN, UPC u otro elemento de datos para un producto que coincida manualmente, debe actualizar los datos en ambos lugares: su [!DNL Commerce] catálogo y el listado en su [!DNL Amazon Seller Central] cuenta.

## Cree el atributo de producto ASIN de Amazon

1. Inicie sesión en su [!DNL Commerce] Administrador.

1. Clic **[!UICONTROL Stores]** en el menú del lado izquierdo.

1. En el _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades de los atributos, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon ASIN` (el nombre de su atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Text Field`.

1. Para **[!UICONTROL Values Required]**, elija `No`.

   Aunque se requiere un ASIN de Amazon para enumerar un producto en Amazon, es posible que algunos de los productos del catálogo no estén enumerados en Amazon.

1. Expanda el _[!UICONTROL Advanced Attribute Properties]_y defina las opciones:

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_asin`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Clic **[!UICONTROL Save Attribute]**.

![Atributo ASIN de Amazon](assets/creating-asin-attribute.png)

## Cree el atributo de producto Condición de Amazon

1. Inicie sesión en su [!DNL Commerce] Administrador.

1. Clic **[!UICONTROL Stores]** en el menú del lado izquierdo.

1. En el _[!UICONTROL Attributes]_, haga clic en **[!UICONTROL Product]**.

1. Para abrir las propiedades del atributo, haga clic en **[!UICONTROL Add New Attribute]**.

1. Para **[!UICONTROL Default Label]**, introduzca `Amazon Condition` (el nombre de su atributo).

1. Para **[!UICONTROL Catalog Input Type for Store Owner]**, elija `Dropdown`.

   El _[!UICONTROL Manage Options (Values of your Attribute)]_aparece la sección.

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

1. Clic **[!UICONTROL Add Option]**.

1. Seleccione el **[!UICONTROL Is Default]** para la condición que desea que sea la selección predeterminada.

1. En el _[!UICONTROL Admin]_, introduzca el texto de la etiqueta de la condición que está añadiendo (por ejemplo, `New`, `Used`, y `Used-Like New`)

1. Clic **[!UICONTROL Add Option]** para agregar más opciones, según sea necesario.

1. Expandir _[!UICONTROL Advanced Attribute Properties]_y configure las opciones.

   - Para **[!UICONTROL Attribute Code]**, introduzca `amazon_condition`.

   - Para **[!UICONTROL Scope]**, elija `Global`.

   - Para **[!UICONTROL Unique Value]**, elija `No`.

   - Para **[!UICONTROL Input Validation for Store Owner]**, elija `None`.

   - Para **[!UICONTROL Add to Column Options]**, elija `Yes`.

   - Para **[!UICONTROL Use in Filter Options]**, elija `Yes`.

1. Clic **[!UICONTROL Save Attribute]**.

![Atributo de condición de Amazon](assets/creating-amazon-condition-attribute.png)

![Icono Siguiente](assets/btn-next.png) [**Continuar para añadir o verificar la clave API**](./amazon-verify-api-key.md)
