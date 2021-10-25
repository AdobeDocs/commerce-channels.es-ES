---
title: Lógica de prioridad de precio
description: El canal de ventas de Amazon aplica la priorización al determinar el precio publicado para un anuncio de Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# lógica de prioridad de precio

En el siguiente ejemplo, ¿cómo determina el sistema si debe publicar 31,99 $, 24,99 $ o 27,99 $?

![Ámbito del precio del comercio](assets/amazon-price-scope.png)

Para determinar qué precio se utiliza si un producto está en dos sitios web y tiene un precio variable por sitio web, utilice la lógica de prioridad de precio (determinada por la variable [Orden](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}).

Para ver el orden de las tiendas, vaya a **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** en el _Administrador_ barra lateral. En el _[!UICONTROL Web Site]_, haga clic en el nombre del sitio web. La variable_[!UICONTROL Web Site Information]_ La página muestra los _[!UICONTROL Sort Order]_para el sitio web, que determina la prioridad del sitio web. Un valor de `1` indica la prioridad más alta.

Si el precio del producto está establecido en `Use Default`, vuelve al valor de precio predeterminado en lugar del valor de precio del sitio web.

## Ejemplo 1

|  | Prioridad del sitio web | Precio (sitio web) | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | — |
| Tienda 1 | 1 | 24,99 $ | No |
| Tienda 2 | 2 | 27,99 $ | Sí |

- La variable **[!UICONTROL Magento Price Source]** (definida en el [Precio de anuncio](./listing-price.md) se configura como `Price` atributo.
- Observe el sitio web con la prioridad de sitio web más alta, que es Store 1 (definida por la variable [Orden](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}).
- Dado que la Tienda 1 está configurada para usar el precio del sitio web (Usar predeterminado = No), el precio publicado es de $24.99.

## Ejemplo 2

|  | Prioridad del sitio web | sitio web de precios | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | — |
| Tienda 1 | 1 | 24,99 $ | Sí |
| Tienda 2 | 2 | 27,99 $ | No |

- La variable **[!UICONTROL Magento Price Source]** (definida en el [Precio de anuncio](./listing-price.md) se configura como `Price` atributo.
- Observe el sitio web con la prioridad de sitio web más alta, que es Store 1 (definida por la variable [orden](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}).
- Desde la tienda 1 **no es** configurado para utilizar el precio del sitio web (Use Default = Yes), consulte el siguiente sitio web en el orden de clasificación.
- Desde la tienda 2 **es** configurado para utilizar el precio del sitio web (use predeterminado = no), el precio publicado es de 27,99 $.

## Ejemplo 3

|  | Prioridad del sitio web | sitio web de precios | Utilizar predeterminado |
|---|---|---|---|
| Predeterminado | 0 | 31,99 $ | 30,00 $ |
| Tienda 1 | 1 | 24,99 $ | — |
| Tienda 2 | 2 | 27,99 $ | 20,00 $ |

Este ejemplo agrega el valor que no es de precio, que se utiliza si selecciona otro valor para _[!UICONTROL Magento Price Source_] (definida en el [Precio de anuncio](./listing-price.md) configuración). El valor que no es de precio siempre utiliza el precio como precio alternativo.

- La variable **[!UICONTROL Magento Price Source]** (definida en el [[!UICONTROL Listing Price]](./listing-price.md) configuración) está establecido en `Non-Price`.
- Observe el sitio web con la prioridad más alta, que es `Store 1`(definido por la variable [Orden](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}).
- Desde la tienda 1 **no es** configure para usar la variable `Non-Price` , consulte el siguiente sitio web en el orden de clasificación.
- Desde la tienda 2 **es** configure para usar la variable `Non-Price` (no precio) [Sitio web] = $20,00), el precio publicado es $20,00.
