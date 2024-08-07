---
title: 'Canal de ventas de Amazon: condiciones de regla de precio'
description: Utilice las condiciones de la regla de precios para determinar qué productos cumplen los requisitos para la regla de precios de listado.
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Condiciones de regla de precio

Las condiciones determinan qué productos cumplen los requisitos para la regla de precio. La definición de las condiciones para las reglas de precios de Amazon sigue la misma lógica y proceso que la definición de las condiciones para [Reglas de precios del carro de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) en [!DNL Commerce].

>[!IMPORTANT]
>
>Si la regla de precio se aplica a todos los productos del catálogo [!DNL Commerce], deje esta sección en blanco.

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

## Ejemplo: Creación de una condición de regla de precio

Este proceso puede ser sencillo o detallado, en función de la configuración del catálogo. Puede definir las condiciones de modo que cuando `ALL` o `ANY` de las condiciones sean `TRUE` o `FALSE` para un producto, el producto sea apto para la regla de precios que se va a aplicar.

Las condiciones se basan en [atributos del producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Para aplicar la regla a todos los productos, deje en blanco la sección de condiciones.

>[!NOTE]
>
>Si desea definir una condición basada en un atributo de producto específico, **Use for Promo Rule Conditions** para el atributo debe establecerse en `Yes` en sus [Propiedades de tienda](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) para el atributo.

![Condición de regla de precio: línea 1](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

Este ejemplo define una regla que aplica un descuento del 25% a todos los productos definidos en la categoría `Books`.

La instrucción de regla tiene dos vínculos en negrita que, al hacer clic en ellos, muestran las opciones de esa parte de la instrucción de condición. Si guarda la condición sin cambiar una opción en negrita, la regla se aplica a todos los productos.

- Haga clic en **[!UICONTROL ALL]** y elija `ALL` o `ANY`.
- Haga clic en **[!UICONTROL TRUE]** y elija `TRUE` o `FALSE`.
- Para aplicar la regla a todos los productos, deje la condición sin cambios.

Puede crear diferentes condiciones cambiando la combinación de estos valores. Para este ejemplo, se utiliza la siguiente condición:

`If ALL of these conditions are TRUE:`

1. Para mostrar los atributos disponibles para los que se aplica la condición, haga clic en el icono Agregar (![Icono Agregar](assets/btn-add-grn.png)) al principio de la línea de condición y seleccione un atributo en el que basar la condición.

   **[!UICONTROL Conditions Combination]** - Elija crear otro conjunto de `All/Any` y `True/False` condiciones dentro de la condición existente.

   ![Combinación de condiciones de regla de precio](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]**: los atributos de producto disponibles dependen de la [configuración del atributo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html). Para que un atributo se muestre en la lista, *[!UICONTROL Use for Promo Rule Conditions]* para el atributo debe establecerse en `Yes` en las propiedades de la tienda.

   - Para **[!UICONTROL Product Attribute]**, elija el atributo que desea definir como base de la condición. Para este ejemplo, la condición seleccionada es `Category`.

     ![Condición de regla de precio: línea 2, parte 2](assets/ob-price-rule-condition-2.png){width="500"}

     La condición seleccionada aparece en la instrucción, seguida de dos vínculos en negrita más. Las opciones difieren según el atributo de producto que seleccione.

     Una vez establecido el atributo, no se puede editar. Para cambiar el atributo, debe eliminar la línea y agregar el nuevo atributo. Para eliminar una línea de condición, haga clic en el icono Eliminar (![Icono Eliminar](assets/btn-del-red.png)) que aparece al final de la línea.

   - Haga clic en **[!UICONTROL is]** y elija el operador de comparación que describe la condición que deben cumplir los productos.

     Para este ejemplo, el operador de comparación es `is`. Las opciones disponibles dependen del atributo seleccionado en el paso anterior y podrían incluir diferentes opciones de comparación. Las opciones pueden incluir valores coincidentes, sin incluir al menos uno de un valor, y mayores, iguales y menores que una cantidad numérica. En este ejemplo, las opciones son `is` y `is not`.

   - Haga clic en **[!UICONTROL ...]** y elija el valor de atributo en el que se basa la condición. Las opciones dependen de la configuración del atributo.

     Puede que se le pida que seleccione una opción o que introduzca un valor para la condición. Para este ejemplo, el campo aparece en blanco. Para seleccionar las categorías de la regla, haga clic en el icono del selector (![Icono del selector](assets/btn-chooser.png)) para mostrar las opciones de selección. Esta regla es para _Libros_, seleccione la casilla de verificación **[!UICONTROL Books]**. El número de categoría se rellena. Para aceptar las selecciones de categoría, haga clic en el icono de marca de verificación verde (![Icono de marca de verificación](assets/btn-check-mark-green.png)).

     ![Condición de regla de precio: línea 2, parte 3](assets/ob-price-rule-condition-3.png){width="500"}

     El elemento seleccionado aparece en la instrucción para completar la condición.

     ![Condición de regla de precio: línea 2, parte 4](assets/ob-price-rule-condition-4.png){width="500"}

     Esta condición de ejemplo está completa. Como se ha indicado, esta condición significa que cualquier producto del catálogo [!DNL Commerce] que tenga una categoría definida de Libros (`4`) es apto para esta regla de precios. Puede añadir más líneas de condición para reducir aún más los productos aptos.

1. Para agregar otra línea de condición a la instrucción, vuelva al paso 1 y repita el proceso hasta que se hayan completado todas las condiciones deseadas.

   Puede eliminar una línea de la condición en cualquier momento haciendo clic en el icono Eliminar (![Icono Eliminar](assets/btn-del-red.png)) al final de la línea.
