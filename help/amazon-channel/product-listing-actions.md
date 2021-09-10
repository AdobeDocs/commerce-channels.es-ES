---
title: Acciones de lista de productos
description: Utilice la configuración Acciones de lista de productos para definir cómo interactúa el catálogo de comercio con Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html: 
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 0%

---

# Acciones de listado de productos

La configuración de acciones de listado de productos forma parte de la configuración de listado de tiendas. Se accede a la configuración de la lista desde el [panel de almacenamiento](./amazon-store-dashboard.md).

Esta configuración define la forma en que el catálogo interactúa con Amazon. Esta configuración:

- Indique si los productos del catálogo de [!DNL Commerce] que cumplen los requisitos de elegibilidad de Amazon se envían automáticamente a su cuenta de [!DNL Amazon Seller Central] para crear anuncios.

- Establezca el tiempo de gestión predeterminado de un pedido. Este valor define el número de días necesarios para procesar y enviar un pedido. Por ejemplo, si alguien selecciona un envío de 2 días, el tiempo de tránsito del envío no comienza hasta que se completa el procesamiento y los paquetes se entregan a un transportista. El tiempo total de entrega es (tiempo de manipulación + tiempo de tránsito + cualquier festivo).

## Configuración

1. Haga clic **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda la sección _[!UICONTROL Product Listing Actions]_.

1. Para **[!UICONTROL Automatic List Action]** (obligatorio), elija una opción:

   - `Automatically List Eligible Products` - (Predeterminado) Elija cuándo desea que sus productos de  [!DNL Commerce] catálogo (que cumplen los requisitos de elegibilidad de Amazon) publiquen automáticamente en Amazon y creen Listas de Amazon.

   - `Do Not Automatically List Eligible Products` - Elija cuándo desea seleccionar manualmente sus productos de  [!DNL Commerce] catálogo aptos y crear listas de Amazon. Cuando se elige, los productos de catálogo que cumplen los criterios de su lista y contienen toda la información necesaria se muestran en la pestaña [_[!UICONTROL Ready to List]_](./ready-to-list.md) para la publicación manual en Amazon.

1. Para **[!UICONTROL Default Handling Time]** (obligatorio), introduzca el número de días necesarios para el tiempo de espera antes del envío.

   El valor predeterminado es `2` días.

   >[!NOTE]
   >
   >Este valor de tiempo de entrega predeterminado solo es efectivo para anuncios de Amazon creados a través del canal de ventas de Amazon. Cualquier lista de Amazon creada en su cuenta [!DNL Amazon Seller Central] utiliza el tiempo de administración predeterminado establecido en Amazon.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Acciones de listado de productos](assets/amazon-product-listing-actions.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Automatic List Action] | Opciones:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recomendado) Elija cuándo desea que sus productos de  [!DNL Commerce] catálogo (que cumplen los requisitos de elegibilidad de Amazon) publiquen automáticamente en Amazon y creen Listas de Amazon. Cuando se elige, la pestaña [_[!UICONTROL Ready to List]_](./ready-to-list.md) no se muestra. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Elija cuándo desea seleccionar manualmente los productos de  [!DNL Commerce] catálogo aptos y crear listas de Amazon. Cuando se elige, los productos de catálogo que cumplen con los criterios de su lista y contienen toda la información necesaria se muestran en la pestaña [_[!UICONTROL Ready to List]_](./ready-to-list.md) para la publicación manual.</li></ul> |
| [!UICONTROL Default Handling Time] | El valor numérico que representa el número de días, en general, que se tarda en procesar y enviar los pedidos. El valor predeterminado es `2`. Este valor se utiliza para anuncios de Amazon creados en [!DNL Commerce] y publicados en Amazon. Este ajuste no afecta al tiempo de administración predeterminado para las listas de Amazon antes de la integración con [!DNL Commerce].<br><br>El valor definido en el canal de ventas de Amazon no reemplaza el tiempo de administración predeterminado definido en una lista de Amazon existente. Cuando se habilita **[!UICONTROL Handling Time Override]** y luego se elimina, el tiempo de administración de un pedido vuelve al valor definido aquí.<br><br>Si tiene productos que tienen tiempos de manipulación diferentes, puede crear una anulación del tiempo de gestión en el nivel específico del producto. Puede administrar las anulaciones de tiempo de gestión en la pestaña [_[!UICONTROL Overrides]_](./overrides.md), lo que le ofrece flexibilidad para administrar la satisfacción del producto. Si no hay una anulación del tiempo de gestión en [!DNL Commerce] para un producto, el tiempo predeterminado de gestión es el valor definido en la lista de Amazon.<br><br>El tiempo de gestión es un atributo regional. Cuando se cambia el valor para una lista, el cambio afecta a todos los listados que comparten el [!DNL Amazon Seller SKU] en todos los almacenes de Amazon que existen para la misma región (definidos en [store integration](./store-integration.md)). Sin embargo, el cambio del valor de un [!DNL Amazon Seller SKU] compartido en la región de América del Norte no afecta a los mismos productos enumerados en un almacén con una región definida diferente. El almacén de la región con la fecha de creación más antigua controla la prioridad de los ajustes de Tiempo de administración predeterminado. |

**Acceso**  rápido:  [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
