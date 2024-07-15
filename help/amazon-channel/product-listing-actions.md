---
title: 'Canal de ventas de Amazon: acciones de lista de productos'
description: Utilice la configuración de Acciones de lista de productos para definir cómo interactúa el catálogo de Commerce con Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Acciones de lista de productos

La configuración de acciones de listado de productos forma parte de la configuración de listado de tiendas. Se tiene acceso a la configuración de lista desde el [panel de almacén](./amazon-store-dashboard.md).

Esta configuración define cómo el catálogo interactúa con Amazon. Esta configuración:

- Indica si los productos del catálogo [!DNL Commerce] que cumplen los requisitos de elegibilidad de Amazon se envían automáticamente a tu cuenta de [!DNL Amazon Seller Central] para crear anuncios.

- Establecer el tiempo de manipulación predeterminado para un pedido. Este valor define el número de días necesarios para procesar y enviar un pedido. Por ejemplo, si alguien selecciona el envío en 2 días, ese tiempo de tránsito de envío no comienza hasta que se completa el procesamiento y los paquetes se entregan a un transportista. El tiempo total de entrega es (tiempo de manipulación + tiempo de tránsito + cualquier feriado).

## Configurar opciones

1. Haga clic en **[!UICONTROL Listing Settings]** en el tablero del almacén.

1. Expanda la sección _[!UICONTROL Product Listing Actions]_.

1. Para **[!UICONTROL Automatic List Action]** (obligatorio), elija una opción:

   - `Automatically List Eligible Products` - (Predeterminado) Elige cuándo quieres que los productos del catálogo [!DNL Commerce] (que cumplen los requisitos de elegibilidad de Amazon) se publiquen automáticamente en Amazon y creen anuncios de Amazon.

   - `Do Not Automatically List Eligible Products`: elige cuándo quieres seleccionar manualmente los productos de catálogo [!DNL Commerce] aptos y crear anuncios de Amazon. Si se elige, los productos del catálogo que cumplan los criterios del anuncio y contengan toda la información necesaria se mostrarán en la ficha [_[!UICONTROL Ready to List]_](./ready-to-list.md) para su publicación manual en Amazon.

1. Para **[!UICONTROL Default Handling Time]** (obligatorio), ingrese el número de días necesarios para el tiempo de espera antes del envío.

   El valor predeterminado es `2` días.

   >[!NOTE]
   >
   >Este valor de tiempo de entrega predeterminado solo es efectivo para anuncios de Amazon creados mediante el canal de ventas de Amazon. Cualquier anuncio de Amazon que se haya creado en su cuenta de [!DNL Amazon Seller Central] usa el tiempo de administración predeterminado establecido en Amazon.

1. Una vez finalizado, haga clic en **[!UICONTROL Save listing settings]**.

![Acciones de lista de productos](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| Campo | Descripción |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | Opciones:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recomendado) Elige cuándo quieres que los productos del catálogo [!DNL Commerce] (que cumplen los requisitos de elegibilidad de Amazon) se publiquen automáticamente en Amazon y se creen anuncios de Amazon. Cuando se elige, no se muestra la ficha [_[!UICONTROL Ready to List]_](./ready-to-list.md). </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**: elige cuándo quieres seleccionar manualmente los productos de catálogo [!DNL Commerce] aptos y crear anuncios de Amazon. Si se elige, los productos del catálogo que cumplan los criterios del anuncio y contengan toda la información necesaria se mostrarán en la ficha [_[!UICONTROL Ready to List]_](./ready-to-list.md) para su publicación manual.</li></ul> |
| [!UICONTROL Default Handling Time] | El valor numérico que representa el número de días, en general, que le toma procesar y enviar sus pedidos. El valor predeterminado es `2`. Este valor se usa para los anuncios de Amazon creados en [!DNL Commerce] y publicados en Amazon. El tiempo de administración predeterminado de los anuncios de Amazon antes de integrarse con [!DNL Commerce] no se ve afectado por esta configuración.<br><br>El valor definido en el canal de ventas de Amazon no reemplaza el tiempo de manipulación predeterminado definido en un listado de Amazon existente. Cuando se habilita **[!UICONTROL Handling Time Override]** y, a continuación, se elimina, el tiempo de control de un pedido vuelve al valor definido aquí.<br><br>Si tiene productos que tienen tiempos de manejo diferentes, puede crear una anulación de tiempo de manejo a nivel de producto específico. Puede administrar las invalidaciones de tiempo de administración en la ficha [_[!UICONTROL Overrides]_](./overrides.md), lo que le proporciona flexibilidad para administrar la satisfacción del producto. Si no hay anulación del tiempo de manipulación en [!DNL Commerce] para un producto, el valor predeterminado del tiempo de manipulación es el definido en la lista de Amazon.<br><br>El tiempo de manipulación es un atributo regional. Cuando se cambia el valor de un listado, el cambio afecta a todos los listados que comparten [!DNL Amazon Seller SKU] en todas las tiendas Amazon que existen para la misma región (definida en [integración de tiendas](./store-integration.md)). Sin embargo, cambiar el valor de un elemento compartido [!DNL Amazon Seller SKU] en la región de Norteamérica no afecta a los mismos productos enumerados en un almacén con una región definida diferente. El almacén de la región con la fecha de creación más antigua controla la prioridad de la configuración de Tiempo de gestión predeterminado. |

**Acceso rápido** - [!UICONTROL Listing Settings] secciones

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
