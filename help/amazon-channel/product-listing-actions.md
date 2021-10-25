---
title: Acciones de lista de productos
description: Utilice la configuración Acciones de lista de productos para definir cómo interactúa el catálogo de comercio con Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Acciones de listado de productos

La configuración de acciones de listado de productos forma parte de la configuración de listado de tiendas. Se accede a la configuración de la lista desde el [tablero de almacenamiento](./amazon-store-dashboard.md).

Esta configuración define la forma en que el catálogo interactúa con Amazon. Esta configuración:

- Indique si su [!DNL Commerce] los productos de catálogo que cumplan los requisitos de elegibilidad de Amazon se envían automáticamente a su [!DNL Amazon Seller Central] para crear anuncios.

- Establezca el tiempo de gestión predeterminado de un pedido. Este valor define el número de días necesarios para procesar y enviar un pedido. Por ejemplo, si alguien selecciona un envío de 2 días, el tiempo de tránsito del envío no comienza hasta que se completa el procesamiento y los paquetes se entregan a un transportista. El tiempo total de entrega es (tiempo de manipulación + tiempo de tránsito + cualquier festivo).

## Configuración

1. Haga clic en **[!UICONTROL Listing Settings]** en el panel de la tienda.

1. Expanda el _[!UICONTROL Product Listing Actions]_para obtener más información.

1. Para **[!UICONTROL Automatic List Action]** (obligatorio), elija una opción:

   - `Automatically List Eligible Products` - (Predeterminado) Elija cuándo desea que su [!DNL Commerce] catálogo de productos (que cumplen los requisitos de elegibilidad de Amazon) para publicar automáticamente en Amazon y crear listas de Amazon.

   - `Do Not Automatically List Eligible Products` - Elija cuándo desea seleccionar manualmente su elegibilidad [!DNL Commerce] catálogo de productos y creación de listas de Amazon. Cuando se elija, los productos de catálogo que cumplan los criterios de su lista y que contengan toda la información necesaria se mostrarán en la [_[!UICONTROL Ready to List]_](./ready-to-list.md) para la publicación manual en Amazon.

1. Para **[!UICONTROL Default Handling Time]** (obligatorio), introduzca el número de días necesarios para el tiempo de espera antes del envío.

   El valor predeterminado es `2` días.

   >[!NOTE]
   >
   >Este valor de tiempo de entrega predeterminado solo es efectivo para anuncios de Amazon creados a través del canal de ventas de Amazon. Cualquier anuncio de Amazon creado en su [!DNL Amazon Seller Central] la cuenta utiliza el tiempo de administración predeterminado establecido en Amazon.

1. Cuando termine, haga clic en **[!UICONTROL Save listing settings]**.

![Acciones de listado de productos](assets/amazon-product-listing-actions.png)

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Automatic List Action] | Opciones:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recomendado) Elija cuándo desea que su [!DNL Commerce] catálogo de productos (que cumplen los requisitos de elegibilidad de Amazon) para publicar automáticamente en Amazon y crear listas de Amazon. Si se elige, la variable [_[!UICONTROL Ready to List]_](./ready-to-list.md) no se muestra. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Elija cuándo desea seleccionar manualmente los elegibles [!DNL Commerce] catálogo de productos y creación de listas de Amazon. Cuando se elija, los productos de catálogo que cumplan los criterios de su lista y que contengan toda la información necesaria se mostrarán en la [_[!UICONTROL Ready to List]_](./ready-to-list.md) para la publicación manual.</li></ul> |
| [!UICONTROL Default Handling Time] | El valor numérico que representa el número de días, en general, que se tarda en procesar y enviar los pedidos. El valor predeterminado es `2`. Este valor se utiliza para anuncios de Amazon creados en [!DNL Commerce] y publicado en Amazon. El tiempo de administración predeterminado para las listas de Amazon antes de la integración con [!DNL Commerce] no se ven afectados por esta configuración.<br><br>El valor definido en el canal de ventas de Amazon no reemplaza el tiempo de administración predeterminado definido en una lista de Amazon existente. Cuando **[!UICONTROL Handling Time Override]** se habilita y, a continuación, se elimina, el tiempo de gestión de un pedido vuelve al valor definido aquí.<br><br>Si tiene productos que tienen tiempos de manipulación diferentes, puede crear una anulación del tiempo de gestión en el nivel específico del producto. Puede administrar las anulaciones de tiempo de administración en la variable [_[!UICONTROL Overrides]_](./overrides.md) , lo que le proporciona flexibilidad para administrar la realización de su producto. Si no hay una anulación del tiempo de administración en [!DNL Commerce] para un producto, el tiempo predeterminado de gestión es el valor definido en la lista de Amazon.<br><br>El tiempo de gestión es un atributo regional. Cuando se cambia el valor de una lista, el cambio afecta a todos los listados que comparten la variable [!DNL Amazon Seller SKU] en todas las tiendas de Amazon que existan para la misma región (definida en [integración de tiendas](./store-integration.md)). Sin embargo, al cambiar el valor de un [!DNL Amazon Seller SKU] en la región de América del Norte no afecta a los mismos productos enumerados en una tienda con una región definida diferente. El almacén de la región con la fecha de creación más antigua controla la prioridad de los ajustes de Tiempo de administración predeterminado. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
