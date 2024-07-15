---
title: 'Canal de ventas de Amazon: lógica de prioridad de precios'
description: El canal de ventas de Amazon aplica la priorización al determinar el precio publicado para un anuncio de Amazon.
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---

# Lógica de prioridad de precios

En el ejemplo siguiente, ¿cómo determina el sistema si debe publicar 31,99, 24,99 o 27,99 $?

![Ámbito de precios de Commerce](assets/amazon-price-scope.png){width="400"}

Para determinar qué precio se usa si un producto está en dos sitios web y tiene un precio variable por sitio web, use la lógica de prioridad de precios (determinada por el valor [Orden](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).

Para ver el orden de las tiendas, ve a **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** en la barra lateral de _Admin_. En la columna _[!UICONTROL Web Site]_, haga clic en el nombre del sitio web. La página_[!UICONTROL Web Site Information]_ muestra la configuración _[!UICONTROL Sort Order]_del sitio web, que determina su prioridad. El valor `1` indica la prioridad más alta.

Si el precio del producto está establecido en `Use Default`, vuelve al valor de precio predeterminado en lugar del valor de precio del sitio web.

## Ejemplo 1

|         | Prioridad del sitio web | Precio (sitio web) | Usar valor predeterminado |
|---------|------------------|-----------------|-------------|
| Predeterminado | 0 | 31,99 USD | — |
| Almacén 1 | 1 | 24,99 USD | No |
| Almacén 2 | 2 | 27,99 USD | Sí |

- El **[!UICONTROL Magento Price Source]** (definido en tu [precio del anuncio](./listing-price.md)) está establecido en el atributo `Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es la Tienda 1 (definida por el valor [Orden](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Dado que la Tienda 1 está configurada para utilizar el precio del sitio web (Utilizar predeterminado = No), el precio publicado es de 24,99 $.

## Ejemplo 2

|         | Prioridad del sitio web | Sitio web de precios | Usar valor predeterminado |
|---------|------------------|---------------|-------------|
| Predeterminado | 0 | 31,99 USD | — |
| Almacén 1 | 1 | 24,99 USD | Sí |
| Almacén 2 | 2 | 27,99 USD | No |

- El **[!UICONTROL Magento Price Source]** (definido en tu [precio del anuncio](./listing-price.md)) está establecido en el atributo `Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es la Tienda 1 (definida por el valor [criterio de ordenación](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Dado que la Tienda 1 **no está** configurada para usar el precio del sitio web (Usar predeterminado = Sí), consulte el siguiente sitio web en el criterio de ordenación.
- Dado que la tienda 2 **está** configurada para usar el precio del sitio web (Usar predeterminado = No), el precio publicado es de 27,99 $.

## Ejemplo 3

|         | Prioridad del sitio web | Sitio web de precios | Usar valor predeterminado |
|---------|------------------|---------------|-------------|
| Predeterminado | 0 | 31,99 USD | 30,00 $ |
| Almacén 1 | 1 | 24,99 USD | — |
| Almacén 2 | 2 | 27,99 USD | 20,00 $ |

En este ejemplo se agrega el valor que no es price, que se usa si selecciona otro valor para _[!UICONTROL Magento Price Source_] (definido en la configuración de [Precio de anuncio](./listing-price.md)). El valor que no es de precio siempre utiliza precio como precio de reserva.

- **[!UICONTROL Magento Price Source]** (definido en la configuración de [[!UICONTROL Listing Price]](./listing-price.md)) está establecido en `Non-Price`.
- Observe el sitio web con la prioridad de sitio web más alta, que es `Store 1` (definida por el valor [Orden](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)).
- Dado que la Tienda 1 **no está** configurada para usar el atributo `Non-Price`, consulte el siguiente sitio web en el criterio de ordenación.
- Dado que la tienda 2 **está** configurada para usar el atributo `Non-Price` (sin precio [Sitio web] = 20,00 $), el precio publicado es de 20,00 $.
