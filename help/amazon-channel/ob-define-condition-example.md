---
title: '"Ejemplo: Definir una condición'''
description: Al crear las reglas de listado, defina las condiciones para identificar los productos del catálogo de comercio que se incluirán en Amazon Marketplace.
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Ejemplo: Definir una condición

## Condiciones

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

**No agregue condiciones si todos los productos dentro del sitio web seleccionado son elegibles.**

>[!NOTE]
>
>Existe un conjunto complejo de procesos back-end para comunicarse directamente con los sistemas de Amazon. En función del número de elementos que intente enumerar y de la cantidad de usuarios que estén en sistemas de Amazon (como Black Friday), puede que haya que esperar que los elementos aparezcan en Amazon.

Consulte la sección Condiciones de [Creación de una regla de precio del carro de compras](https://docs.magento.com/user-guide/marketing/price-rules-catalog-create.html){:target=&quot;_blank&quot;}.

## Definición de una condición

Este proceso puede ser sencillo o detallado, según la configuración del catálogo. Puede configurar las condiciones de modo que cuando `ALL` o `ANY` de las condiciones definidas sean `TRUE` o `FALSE` para un producto, el producto sea elegible para aparecer en la lista de Amazon.

Las condiciones se basan en valores de atributos de producto existentes. Para aplicar la regla a todos los productos, deje la sección condiciones en blanco.

>[!NOTE]
>
>Si desea definir una condición basada en un atributo de producto específico, establezca la configuración **[!UICONTROL Use for Promo Rule Conditions]** para el atributo en `Yes`. Puede acceder a esta configuración en la página [Propiedades de tienda](https://docs.magento.com/user-guide/catalog/product-attributes-add.html){:target=&quot;_blank&quot;} del atributo.

![Condición - línea 1](assets/ob-listing-rule-conditions-start.png)

La regla de este ejemplo define una regla que establece la idoneidad de Amazon para todos los productos de catálogo que tienen el atributo _Amazon FBA_ establecido en `Yes`.

La instrucción rule tiene dos vínculos en negrita que, cuando se hace clic en ellos, muestran las opciones de esa parte de la instrucción. Si guarda la condición sin cambiar la opción en negrita, la regla se aplica a todos los productos.

- Haga clic en **[!UICONTROL ALL]** y elija `ALL` o `ANY`.
- Haga clic en **[!UICONTROL TRUE]** y elija `TRUE` o `FALSE`.
- Para aplicar la regla a todos los productos, deje la condición sin modificar.

Puede crear diferentes condiciones cambiando la combinación de estos valores. Para este ejemplo, se utiliza la siguiente condición:

`If ALL of these conditions are TRUE:`

1. Haga clic en el icono Add (![Add icon](assets/btn-add-grn.png)) al principio de la línea de condición y seleccione un atributo en el que basar la condición, como una combinación de condiciones o un atributo de producto.

   - **[!UICONTROL Conditions Combination]** - Elija permitirle crear otro conjunto de  `All/Any` condiciones y  `True/False` dentro del conjunto existente.

      ![Combinación de condiciones](assets/ob-conditions-combinations.png)

   - **[!UICONTROL Product Attribute]** - Los atributos del producto dependen de la configuración del atributo. Para que un atributo aparezca en la lista, debe configurarse para su uso en condiciones de regla promocional. Consulte _Uso para condiciones de reglas promocionales_ en [Atributos de producto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

      En la lista de **[!UICONTROL Product Attribute]**, elija el atributo que desea utilizar como base de la condición. Para este ejemplo, la condición seleccionada es `Amazon FBA`.

      ![Línea de condición 2, parte 2](assets/ob-condition-attribute-dropdown.png)

      La condición seleccionada aparece en la instrucción, seguida de dos vínculos más en negrita. Las opciones difieren según el atributo de producto que seleccione.

      Una vez establecido el atributo, no se puede cambiar. Para cambiar el atributo, debe eliminar la línea y agregar el atributo nuevo. Puede eliminar una línea de condición haciendo clic en el icono Delete (![Delete icon](assets/btn-del-red.png)) al final de la línea.

      1. Haga clic en **[!UICONTROL is]** y seleccione el operador de comparación que describe la condición para que se cumplan los productos.

         Para este ejemplo, el operador de comparación es `is`. Las opciones disponibles dependen del atributo seleccionado en el paso anterior. Las opciones podrían incluir distintas opciones de comparación, como valores coincidentes, sin incluir o incluir al menos uno de un valor, y buenos que, iguales o inferiores a una cantidad numérica. En este ejemplo, las opciones son `is` y `is not`.

      1. Haga clic en **[!UICONTROL ...]** y seleccione el valor del atributo en el que se basa la condición.

         Las opciones dependen de la configuración del atributo. Se le puede pedir que seleccione una opción o que introduzca texto o valores numéricos para la condición. Para este ejemplo, la selección es `Yes`.

         El elemento seleccionado aparece en la instrucción para completar la condición.

         ![Línea de condición 2, parte 3](assets/ob-listing-rule-condition-is.png)
   Esta condición se ha completado. Como se ha indicado, esta condición significa que cualquier producto del catálogo [!DNL Commerce] que tenga el atributo FBA de Amazon establecido en un valor de `Yes` es apto para incluirse en Amazon en la región y la tienda. Puede agregar más líneas de condición para reducir aún más los productos aptos.

1, para agregar otra línea de condición a la instrucción, vuelva al paso 1 y repita el proceso hasta que se hayan completado todas las condiciones deseadas.

Puede eliminar una línea de la condición en cualquier momento haciendo clic en el icono Delete (![Delete icon](assets/btn-del-red.png)) al final de la línea.
