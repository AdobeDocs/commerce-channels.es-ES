---
title: Condiciones de las reglas de precio
description: Utilice las condiciones de la regla de precio para determinar qué productos cumplen los requisitos para la regla de precio de anuncio.
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html: 
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 0%

---

# Condiciones de regla de precio

Las condiciones determinan qué productos cumplen los requisitos para la regla de precios. La definición de las condiciones para las reglas de precios de Amazon sigue la misma lógica y proceso que la definición de las condiciones para [reglas de precios del carro de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){:target=&quot;_blank&quot;} en [!DNL Commerce].

>[!IMPORTANT]
>
>Si la regla de precio se aplica a todos los productos del catálogo [!DNL Commerce], deje esta sección en blanco.

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

## Ejemplo: generar una condición de regla de precio

Este proceso puede ser sencillo o detallado, según la configuración del catálogo. Puede definir las condiciones para que cuando `ALL` o `ANY` de las condiciones sean `TRUE` o `FALSE` para un producto, el producto sea elegible para la regla de precios que se aplicará.

Las condiciones se basan en sus [atributos de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}. Para aplicar la regla a todos los productos, deje la sección condiciones en blanco.

>[!NOTE]
>
>Si desea definir una condición basada en un atributo de producto específico, **Use for Promo Rule Conditions** para el atributo debe configurarse como `Yes` en [Storefront Properties](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;} para el atributo.

![Condición de regla de precio - línea 1](assets/ob-price-rules-condition-1.png)

En este ejemplo se define una regla que aplica un 25% de descuento a todos los productos definidos en la categoría `Books`.

La instrucción rule tiene dos vínculos en negrita que, cuando se hace clic en ellos, muestran las opciones para esa parte de la condición. Si guarda la condición sin cambiar una opción en negrita, la regla se aplica a todos los productos.

- Haga clic en **[!UICONTROL ALL]** y elija `ALL` o `ANY`.
- Haga clic en **[!UICONTROL TRUE]** y elija `TRUE` o `FALSE`.
- Para aplicar la regla a todos los productos, deje la condición sin modificar.

Puede crear diferentes condiciones cambiando la combinación de estos valores. Para este ejemplo, se utiliza la siguiente condición:

`If ALL of these conditions are TRUE:`

1. Para mostrar los atributos disponibles para los que se aplica la condición, haga clic en el icono Add (![Add icon](assets/btn-add-grn.png)) al principio de la línea de condición y seleccione un atributo en el que basar la condición.

   **[!UICONTROL Conditions Combination]** - Elija crear otro conjunto de condiciones  `All/Any` y  `True/False` dentro de la condición existente.

   ![Combinación de condiciones de regla de precio](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]** - Los atributos de producto disponibles dependen de la  [configuración del atributo](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}. Para que un atributo se muestre en la lista, *[!UICONTROL Use for Promo Rule Conditions]* para el atributo debe establecerse en `Yes` en las [propiedades de tienda](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}.

   - Para **[!UICONTROL Product Attribute]**, elija el atributo que desea definir como base de la condición. Para este ejemplo, la condición seleccionada es `Category`.

      ![Condición de regla de precio - línea 2, parte 2](assets/ob-price-rule-condition-2.png)

      La condición seleccionada aparece en la instrucción, seguida de dos vínculos más en negrita. Las opciones difieren según el atributo de producto que seleccione.

      Una vez establecido el atributo, no se puede editar. Para cambiar el atributo, debe eliminar la línea y agregar el atributo nuevo. Para eliminar una línea de condición, haga clic en el icono Delete (![Delete icon](assets/btn-del-red.png)) situado al final de la línea.

   - Haga clic en **[!UICONTROL is]** y seleccione el operador de comparación que describe la condición para que se cumplan los productos.

      Para este ejemplo, el operador de comparación es `is`. Las opciones disponibles dependen del atributo seleccionado en el paso anterior y podrían incluir distintas opciones de comparación. Las opciones pueden incluir valores coincidentes, sin incluir o incluir al menos uno de un valor, y buenos que, iguales o inferiores a una cantidad numérica. En este ejemplo, las opciones son `is` y `is not`.

   - Haga clic en **[!UICONTROL ...]** y seleccione el valor del atributo en el que se basa la condición. Las opciones dependen de la configuración del atributo.

      Se le puede pedir que seleccione una opción o que introduzca un valor para la condición. Para este ejemplo, el campo aparece en blanco. Para seleccionar las categorías de la regla, haga clic en el icono de selección (![Icono de selector](assets/btn-chooser.png)) para mostrar las opciones de selección. Esta regla es para _Books_, seleccione la casilla de verificación **[!UICONTROL Books]**. El número de categoría se rellena. Para aceptar las selecciones de categoría, haga clic en el icono de marca de verificación verde (![Icono de marca de verificación](assets/btn-check-mark-green.png)).

      ![Condición de regla de precio - línea 2, parte 3](assets/ob-price-rule-condition-3.png)

      El elemento seleccionado aparece en la instrucción para completar la condición.

      ![Condición de regla de precio - línea 2, parte 4](assets/ob-price-rule-condition-4.png)

      Esta condición de ejemplo está completa. Como se ha indicado, esta condición significa que cualquier producto del catálogo [!DNL Commerce] que tenga una categoría definida de Libros (`4`) es apto para esta regla de precios. Puede agregar más líneas de condición para reducir aún más los productos aptos.

1. Para agregar otra línea de condición a la instrucción, vuelva al paso 1 y repita el proceso hasta que se hayan completado todas las condiciones deseadas.

   Puede eliminar una línea de la condición en cualquier momento haciendo clic en el icono Delete (![Delete icon](assets/btn-del-red.png)) al final de la línea.
