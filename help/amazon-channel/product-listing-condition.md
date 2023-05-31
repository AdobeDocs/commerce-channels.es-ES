---
title: 'Canal de ventas de Amazon: condición de lista de productos'
description: Utilice la configuración de Condición de la lista de productos para asignar sus productos de Commerce a una condición de producto de Amazon, como "Nuevo" o "Reacondicionado".
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Condición de lista de productos

La configuración de condición de lista de productos forma parte de la configuración de lista de tiendas. Puede acceder a la configuración de la lista en la [tablero de tienda](./amazon-store-dashboard.md).

Amazon requiere que una lista de productos tenga una condición definida. Si todos los productos están en la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos como el valor de condición global. Las condiciones estándar de Amazon incluyen:

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>Si vende productos renovados (reacondicionados), debe inscribirse en el [!DNL Amazon Renewed Program]. Consulte [Productos renovados](./renewed-products.md).

Sin embargo, si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Reacondicionado), debe elegir **[!UICONTROL Assign Condition Using Product Attribute]**. Esta configuración le permite asignar su [!DNL Commerce] atributo de condición y valores a las condiciones de su anuncio de Amazon.

Durante [Tareas previas a la configuración](./amazon-pre-setup-tasks.md), se le recomienda crear un [!DNL Commerce] atributo de producto para la condición de un producto. Si ofrece productos en varias condiciones y no ha creado un atributo de condición, consulte [Creación de un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md). Una vez creado el atributo de condición, puede asignar un valor de condición a cada uno de los productos de su [!DNL Commerce] catálogo.

## Configurar opciones

1. Clic **[!UICONTROL Listing Settings]** en el tablero de la tienda.

1. Expanda el **[!UICONTROL Product Listing Condition]** sección.

1. Para **[!UICONTROL Listing Product Condition]**, elija una opción.

   Elige una de las condiciones estándar de Amazon para el valor de condición global de todos tus anuncios. La configuración predeterminada es `New`.

   Si tiene productos o listados que tienen condiciones diferentes, elija `Assign Condition Using Product Attribute` para definir la configuración de la condición del producto en los campos adicionales que aparecen.

1. Para **Atributo de condición**, elija la [!DNL Commerce] para asignar valores a cada uno de los atributos de condición estándar de Amazon.

   Si tiene productos en la `Used` o `Collectible` condición, pero no distingue más, puede asignar a una sola `Used` o `Collectible` Amazon y deje los demás en blanco. Este método asigna todos los `Used` o `Collectible` a la condición Amazon Used o Collectible única.

   Por ejemplo, tiene un solo `Used` condición para sus productos. Al realizar la asignación, debe elegir si desea asignar a la condición de Amazon `Used; Like New`, `Used; Very Good`, `Used; Good`, o `Used; Acceptable`. Complete solo el campo de la condición de Amazon que desee y deje el otro `Used` opciones establecidas en `--Select Option--`. En la imagen de ejemplo, todas [!DNL Commerce] productos en `Used` Las condiciones de se asignan a Amazon `Used; Very Good` condición.

   También puede introducir texto descriptivo para las condiciones, excepto `New`.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Condición de lista de productos](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Campo | Descripción |
|---|---|
| [!UICONTROL Listing Product Condition] | La condición de los listados de productos. Opciones: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vende una sola condición de producto, elija una de las condiciones estándar de Amazon. Si su [!DNL Commerce] catálogo contiene productos en varias condiciones, elija `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | El [!DNL Commerce] que define la condición de los productos. Seleccione el atributo Magento que ha creado para asignarlo al atributo de condición Amazon. En el [Ejemplo de tareas previas a la configuración](./ob-creating-magento-attributes.md) recomienda ponerle nombre como `Amazon Condition`. Cuando se seleccionan, aparecen campos adicionales para asignar las condiciones estándar de Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada una de las condiciones estándar de Amazon, elija la condición correspondiente. Las opciones son las etiquetas de condición que agregó al [ha creado su atributo de condición de Amazon](./ob-creating-magento-attributes.md).<br><br>Si tiene productos en la `Used` o `Collectible` condición, pero no distingue más, puede asignar a una sola `Used` o `Collectible` Amazon y deje los demás en blanco. Este método asigna todo `Used` o `Collectible` a la condición Amazon Used o Collectible única. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
