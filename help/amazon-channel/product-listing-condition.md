---
title: Condición de lista de productos
description: Utilice la configuración Condición de lista de productos para asignar los productos de comercio a una condición de producto de Amazon, como "Nuevo" o "Reformado".
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Condición de listado de productos

La configuración de las condiciones de la lista de productos forma parte de la configuración de la lista de tiendas. Puede acceder a la configuración de la lista en el [panel de almacenamiento](./amazon-store-dashboard.md).

Amazon requiere una lista de productos para tener una condición definida. Si todos los productos están en la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos como su valor de condición global. Las condiciones estándar de Amazon incluyen:

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
>Si vende productos renovados (renovados), debe inscribirse en el [!DNL Amazon Renewed Program]. Consulte [Productos renovados](./renewed-products.md).

Sin embargo, si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Reformado), debe elegir **[!UICONTROL Assign Condition Using Product Attribute]**. Esta configuración le permite asignar el atributo y los valores de condición [!DNL Commerce] a las condiciones de su listado de Amazon.

Durante las [tareas previas a la configuración](./amazon-pre-setup-tasks.md), se le recomienda crear un atributo de producto [!DNL Commerce] para la condición de un producto. Si ofrece productos en varias condiciones y no ha creado un atributo de condición, consulte [Crear un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md). Una vez creado el atributo de condición, puede asignar un valor de condición a cada uno de los productos del catálogo [!DNL Commerce].

## Configuración

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección **[!UICONTROL Product Listing Condition]** .

1. Para **[!UICONTROL Listing Product Condition]**, elija una opción.

   Elija una de las condiciones estándar de Amazon para el valor de condición global de todos los anuncios. La configuración predeterminada es `New`.

   Si tiene productos o listas que tienen condiciones diferentes, elija `Assign Condition Using Product Attribute` para definir la configuración de las condiciones del producto en los campos adicionales que aparecen.

1. Para **Condition Attribute**, elija el atributo [!DNL Commerce] para asignar valores para cada uno de los atributos de condición estándar de Amazon.

   Si tiene productos en las condiciones `Used` o `Collectible` pero no distingue más, puede asignar a una única condición de Amazon `Used` o `Collectible` y dejar los demás en blanco. Este método asigna todas las condiciones `Used` o `Collectible` a la condición única de Amazon Utilizado o Colectible.

   Por ejemplo, tiene una sola condición `Used` para sus productos. Al asignar, debe elegir si desea asignar a la condición de Amazon `Used; Like New`, `Used; Very Good`, `Used; Good` o `Used; Acceptable`. Complete únicamente el campo de la condición de Amazon que desee, dejando las demás opciones `Used` configuradas como `--Select Option--`. En la imagen de ejemplo, todos los productos [!DNL Commerce] de la condición `Used` están asignados a la condición `Used; Very Good` de Amazon.

   También puede introducir texto descriptivo para sus condiciones, excepto `New`.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Condición de listado de productos](assets/amazon-product-listing-condition.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Listing Product Condition] | La condición de las listas de productos. Opciones: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vende una sola condición de producto, elija una de las condiciones estándar de Amazon. Si su catálogo [!DNL Commerce] contiene productos en varias condiciones, elija `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | El atributo [!DNL Commerce] que define la condición para sus productos. Seleccione el atributo Magneto que ha creado para asignarlo al atributo de condición de Amazon. En [Pre-Setup Tasks example](./ob-creating-magento-attributes.md) recomienda llamarlo `Amazon Condition`. Cuando se elige, aparecen campos adicionales para asignar las condiciones estándar de Amazon. |
| [!UICONTROL Additional Condition fields] | Para cada una de las condiciones estándar de Amazon, seleccione la condición correspondiente. Las opciones son las etiquetas de condición que agregó cuando [creó el atributo de condición de Amazon](./ob-creating-magento-attributes.md).<br><br>Si tiene productos en la  `Used` condición  `Collectible` o pero no distingue más, puede asignar a una condición única  `Used` o de  `Collectible` Amazon y dejar los demás en blanco. Este método asigna todas las condiciones `Used` o `Collectible` a la condición única de Amazon Utilizado o Colectible. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
