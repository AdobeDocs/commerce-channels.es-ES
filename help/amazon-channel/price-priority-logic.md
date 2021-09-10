---
title: Lógica de prioridad de precio
description: El canal de ventas de Amazon aplica la priorización al determinar el precio publicado para un anuncio de Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# lógica de prioridad de precio

En el siguiente ejemplo, ¿cómo determina el sistema si debe publicar 31,99 $, 24,99 $ o 27,99 $?

![Ámbito del precio del comercio](assets/amazon-price-scope.png)

Para determinar qué precio se utiliza si un producto está en dos sitios web y tiene un precio variable por sitio web, utilice la lógica de prioridad de precio (determinada por el valor [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).

Para ver el orden de las tiendas, vaya a **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** en la barra lateral _Admin_. En la columna _[!UICONTROL Web Site]_, haga clic en el nombre del sitio web. La página_[!UICONTROL Web Site Information]_ muestra la configuración _[!UICONTROL Sort Order]_del sitio Web, que determina la prioridad del sitio Web. Un valor de `1` indica la prioridad más alta.

Si el precio del producto está establecido en `Use Default`, vuelve al valor de precio predeterminado en lugar del valor de precio del sitio web.

## Ejemplo 1

|  | Prioridad del sitio web | Precio (sitio web) | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | — |
| Tienda 1 | 1 | 24,99 $ | No |
| Tienda 2 | 2 | 27,99 $ | Sí |

- El **[!UICONTROL Magento Price Source]** (definido en su [Precio de anuncio](./listing-price.md) se establece en el atributo `Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es Store 1 (definida por el valor [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Dado que la Tienda 1 está configurada para usar el precio del sitio web (Usar predeterminado = No), el precio publicado es de $24.99.

## Ejemplo 2

|  | Prioridad del sitio web | sitio web de precios | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | — |
| Tienda 1 | 1 | 24,99 $ | Sí |
| Tienda 2 | 2 | 27,99 $ | No |

- El **[!UICONTROL Magento Price Source]** (definido en su [Precio de anuncio](./listing-price.md) se establece en el atributo `Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es Store 1 (definida por el valor [sort order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Dado que la Tienda 1 **no está** configurada para usar el precio del sitio web (Usar predeterminado = Sí), mire el siguiente sitio web en el orden de clasificación.
- Dado que Store 2 **está** configurado para usar el precio del sitio web (use predeterminado = no), el precio publicado es de $27,99.

## Ejemplo 3

|  | Prioridad del sitio web | sitio web de precios | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | 30,00 $ |
| Tienda 1 | 1 | 24,99 $ | — |
| Tienda 2 | 2 | 27,99 $ | 20,00 $ |

Este ejemplo agrega el valor que no es de precio, que se utiliza si selecciona otro valor para _[!UICONTROL Magento Price Source_] (definido en la configuración [Precio de anuncio](./listing-price.md)). El valor que no es de precio siempre utiliza el precio como precio alternativo.

- El **[!UICONTROL Magento Price Source]** (definido en la configuración [[!UICONTROL Listing Price]](./listing-price.md)) se establece en `Non-Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es `Store 1`(definido por el valor [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Dado que la Tienda 1 **no está** configurada para utilizar el atributo `Non-Price`, observe el siguiente sitio web en el orden de clasificación.
- Dado que la Tienda 2 **está** configurada para utilizar el atributo `Non-Price` (no de precio [Sitio web] = 20,00 dólares), el precio publicado es de 20,00 dólares.
