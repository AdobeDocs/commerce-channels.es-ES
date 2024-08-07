---
title: "Ejemplo: Definición de una condición para reglas de listado de Amazon"
description: Al crear las reglas de listado, defina las condiciones para identificar los productos del catálogo de Commerce que se enumerarán en Amazon Marketplace.
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Ejemplo: Definición de una condición

## Condiciones

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

**No agregue condiciones si todos los productos del sitio web seleccionado cumplen los requisitos.**

>[!NOTE]
>
>Existe un complejo conjunto de procesos back-end para comunicarse directamente con los sistemas de Amazon. En función del número de artículos que intentas poner en venta y de la ocupación que puedan tener los sistemas de Amazon (por ejemplo, Black Friday), puede que tus artículos tarden un tiempo en aparecer en Amazon.

Consulte la sección Condiciones de [Creación de una regla de precio de carro de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## Definición de una condición

Este proceso puede ser sencillo o detallado, en función de la configuración del catálogo. Puede configurar las condiciones de modo que cuando `ALL` o `ANY` de las condiciones definidas sean `TRUE` o `FALSE` para un producto, este pueda aparecer en la lista de Amazon.

Las condiciones se basan en valores de atributo de producto existentes. Para aplicar la regla a todos los productos, deje en blanco la sección de condiciones.

>[!NOTE]
>
>Si desea definir una condición basada en un atributo de producto específico, establezca la configuración de **[!UICONTROL Use for Promo Rule Conditions]** para el atributo en `Yes`. Puede obtener acceso a esta configuración en la página [Propiedades de tienda](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) para el atributo.

![Condición: línea 1](assets/ob-listing-rule-conditions-start.png){width="500"}

La regla de este ejemplo define una regla que establece la idoneidad de Amazon para todos los productos de catálogo que tienen el atributo _Amazon FBA_ establecido en `Yes`.

La instrucción de regla tiene dos vínculos en negrita que, al hacer clic en ellos, muestran las opciones de esa parte de la instrucción. Si guarda la condición sin realizar ningún cambio en una opción en negrita, la regla se aplica a todos los productos.

- Haga clic en **[!UICONTROL ALL]** y elija `ALL` o `ANY`.
- Haga clic en **[!UICONTROL TRUE]** y elija `TRUE` o `FALSE`.
- Para aplicar la regla a todos los productos, deje la condición sin cambios.

Puede crear diferentes condiciones cambiando la combinación de estos valores. Para este ejemplo, se utiliza la siguiente condición:

`If ALL of these conditions are TRUE:`

1. Haga clic en el icono Agregar (![Agregar icono](assets/btn-add-grn.png)) al principio de la línea de condición y seleccione un atributo en el que basar la condición, como una combinación de condiciones o un atributo de producto.

   - **[!UICONTROL Conditions Combination]**: elija esta opción para permitirle crear otro conjunto de `All/Any` y `True/False` condiciones dentro del conjunto existente.

     ![Combinación de condiciones](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]**: los atributos del producto dependen de la configuración del atributo. Para que un atributo aparezca en la lista, debe configurarse para su uso en condiciones de regla promocional. Consulte _Uso de las condiciones de regla de promoción_ en [Atributos del producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     En la lista debajo de **[!UICONTROL Product Attribute]**, elija el atributo que desea usar como base de la condición. Para este ejemplo, la condición seleccionada es `Amazon FBA`.

     ![Línea de condición 2, parte 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     La condición seleccionada aparece en la instrucción, seguida de dos vínculos en negrita más. Las opciones difieren según el atributo de producto que seleccione.

     Una vez establecido el atributo, no se puede cambiar. Para cambiar el atributo, debe eliminar la línea y agregar el nuevo atributo. Para eliminar una línea de condición, haga clic en el icono Eliminar (![icono Eliminar](assets/btn-del-red.png)) que aparece al final de la línea.

      1. Haga clic en **[!UICONTROL is]** y elija el operador de comparación que describe la condición que deben cumplir los productos.

         Para este ejemplo, el operador de comparación es `is`. Las opciones disponibles dependen del atributo seleccionado en el paso anterior. Las opciones pueden incluir diferentes opciones de comparación, como valores coincidentes, sin incluir o al menos uno de un valor, y mayor que, igual a y menor que una cantidad numérica. En este ejemplo, las opciones son `is` y `is not`.

      1. Haga clic en **[!UICONTROL ...]** y elija el valor de atributo en el que se basa la condición.

         Las opciones dependen de la configuración del atributo. Se le puede pedir que seleccione una opción o que introduzca texto o valores numéricos para la condición. Para este ejemplo, la selección es `Yes`.

         El elemento seleccionado aparece en la instrucción para completar la condición.

         ![Línea de condición 2, parte 3](assets/ob-listing-rule-condition-is.png){width="500"}

   Esta condición se ha completado. Como se ha indicado, esta condición significa que cualquier producto del catálogo [!DNL Commerce] que tenga el atributo FBA de Amazon establecido en un valor de `Yes` es apto para su inclusión en Amazon en la región y tienda. Puede añadir más líneas de condición para reducir aún más los productos aptos.

1, Para agregar otra línea de condición a la instrucción, vuelva al paso 1 y repita el proceso hasta que se hayan completado todas las condiciones deseadas.

Puede eliminar una línea de la condición en cualquier momento haciendo clic en el icono Eliminar (![Icono Eliminar](assets/btn-del-red.png)) al final de la línea.
