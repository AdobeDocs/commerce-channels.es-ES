---
title: 'Canal de ventas de Amazon: condición de lista de productos'
description: Utilice la configuración de Condición de la lista de productos para asignar los productos de Commerce a una condición de producto de Amazon, como "Nuevo" o "Reacondicionado".
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Condición de lista de productos

La configuración de condición de lista de productos forma parte de la configuración de lista de tiendas. Puede obtener acceso a la configuración del listado en [panel de almacén](./amazon-store-dashboard.md).

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
>Si vende productos renovados (restaurados), debe inscribirse en [!DNL Amazon Renewed Program]. Ver [Productos renovados](./renewed-products.md).

Sin embargo, si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Reacondicionado), debe elegir **[!UICONTROL Assign Condition Using Product Attribute]**. Esta configuración le permite asignar los valores y atributos de condición [!DNL Commerce] a las condiciones del listado de Amazon.

Durante [las tareas previas a la configuración](./amazon-pre-setup-tasks.md), se le recomienda crear un atributo de producto [!DNL Commerce] para la condición de un producto. Si ofrece productos en varias condiciones y no ha creado un atributo de condición, consulte [Crear un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md). Una vez creado el atributo de condición, puede asignar un valor de condición a cada uno de los productos del catálogo [!DNL Commerce].

## Configurar opciones

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección **[!UICONTROL Product Listing Condition]**.

1. Para **[!UICONTROL Listing Product Condition]**, elija una opción.

   Elige una de las condiciones estándar de Amazon para el valor de condición global de todos tus anuncios. La configuración predeterminada es `New`.

   Si tiene productos/listados que tienen condiciones diferentes, elija `Assign Condition Using Product Attribute` para definir la configuración de la condición del producto en los campos adicionales que aparecen.

1. Para **Atributo de condición**, elija el atributo [!DNL Commerce] para asignar valores a cada uno de los atributos de condición estándar de Amazon.

   Si tiene productos en la condición `Used` o `Collectible` pero no distingue más, puede asignar a una única condición de Amazon `Used` o `Collectible` y dejar las demás en blanco. Este método asigna todas las condiciones de `Used` o `Collectible` a la única condición Amazon Used o Collectible.

   Por ejemplo, tiene una sola condición `Used` para sus productos. Al asignar, elige si desea asignar a la condición de Amazon `Used; Like New`, `Used; Very Good`, `Used; Good` o `Used; Acceptable`. Complete solamente el campo de la condición de Amazon que desee, dejando las otras `Used` opciones establecidas en `--Select Option--`. En la imagen de ejemplo, todos los productos de [!DNL Commerce] en la condición `Used` se asignan a la condición `Used; Very Good` de Amazon.

   También puede escribir texto descriptivo para las condiciones, excepto `New`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Condición de lista de productos](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Campo | Descripción |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | La condición de los listados de productos. Opciones: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vende una sola condición de producto, elija una de las condiciones estándar de Amazon. Si el catálogo [!DNL Commerce] contiene productos en diversas condiciones, elija `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | Atributo [!DNL Commerce] que define la condición de los productos. Seleccione el atributo Magento que ha creado para asignarlo al atributo de condición Amazon. En el ejemplo de [tareas previas a la instalación](./ob-creating-magento-attributes.md) se recomienda nombrarla como `Amazon Condition`. Cuando se seleccionan, aparecen campos adicionales para asignar las condiciones estándar de Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada una de las condiciones estándar de Amazon, elija la condición correspondiente. Las opciones son las etiquetas de condición que agregó al [crear su atributo de condición de Amazon](./ob-creating-magento-attributes.md).<br><br>Si tiene productos en la condición `Used` o `Collectible` pero no distingue más, puede asignar a una sola condición de Amazon `Used` o `Collectible` y dejar las demás en blanco. Este método asigna todas las condiciones `Used` o `Collectible` a la condición única Amazon Used o Collectible. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
