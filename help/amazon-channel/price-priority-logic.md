---
title: 'Canal de ventas de Amazon: lógica de prioridad de precios'
description: El canal de ventas de Amazon aplica la priorización al determinar el precio publicado para un anuncio de Amazon.
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# Lógica de prioridad de precios

En el ejemplo siguiente, ¿cómo determina el sistema si debe publicar 31,99, 24,99 o 27,99 $?

![Ámbito del precio comercial](assets/amazon-price-scope.png){width="400"}

Para determinar qué precio se utiliza si un producto está en dos sitios web y tiene un precio variable por sitio web, utilice la lógica de prioridad de precios (determinada por la variable [Orden de clasificación](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).

Para ver el criterio de ordenación de las tiendas, vaya a **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** en el _Administrador_ barra lateral. En el _[!UICONTROL Web Site]_, haga clic en el nombre del sitio web. El_[!UICONTROL Web Site Information]_ La página muestra la _[!UICONTROL Sort Order]_configuración del sitio web, que determina la prioridad del sitio web. Un valor de `1` indica la prioridad más alta.

Si el precio del producto está establecido en `Use Default`Sin embargo, vuelve al valor de precio predeterminado en lugar del valor de precio del sitio web.

## Ejemplo 1

|         | Prioridad del sitio web | Precio (sitio web) | Usar valor predeterminado |
|---------|------------------|-----------------|-------------|
| Predeterminado | 0 | $31.99 | — |
| Almacén 1 | 1 | $24.99 | No |
| Almacén 2 | 2 | $27.99 | Sí |

- El **[!UICONTROL Magento Price Source]** (definido en su [Precio del anuncio](./listing-price.md) se establece en `Price` atributo.
- Examine el sitio web con la prioridad más alta, que es la Tienda 1 (definida por la variable [Orden de clasificación](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Dado que la Tienda 1 está configurada para utilizar el precio del sitio web (Utilizar predeterminado = No), el precio publicado es de 24,99 $.

## Ejemplo 2

|         | Prioridad del sitio web | Sitio web de precios | Usar valor predeterminado |
|---------|------------------|---------------|-------------|
| Predeterminado | 0 | $31.99 | -- |
| Almacén 1 | 1 | $24.99 | Sí |
| Almacén 2 | 2 | $27.99 | No |

- El **[!UICONTROL Magento Price Source]** (definido en su [Precio del anuncio](./listing-price.md) se establece en `Price` atributo.
- Examine el sitio web con la prioridad más alta, que es la Tienda 1 (definida por la variable [criterio de ordenación](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Desde la tienda 1 **no es** configurado para utilizar el precio del sitio web (Usar predeterminado = Sí), busque el siguiente sitio web en el orden.
- Desde la tienda 2 **es** configurado para utilizar el precio del sitio web (Usar predeterminado = No), el precio publicado es de 27,99 $.

## Ejemplo 3

|         | Prioridad del sitio web | Sitio web de precios | Usar valor predeterminado |
|---------|------------------|---------------|-------------|
| Predeterminado | 0 | $31.99 | $30.00 |
| Almacén 1 | 1 | $24.99 | -- |
| Almacén 2 | 2 | $27.99 | $20.00 |

En este ejemplo se agrega el valor que no es price, que se utiliza si selecciona otro valor para _[!UICONTROL Magento Price Source_] (definido en su [Precio del anuncio](./listing-price.md) configuración). El valor que no es de precio siempre utiliza precio como precio de reserva.

- El **[!UICONTROL Magento Price Source]** (definido en [[!UICONTROL Listing Price]](./listing-price.md) configuración) se ha establecido en `Non-Price`.
- Examine el sitio web con la prioridad más alta, que es `Store 1`(definida por la variable [Orden de clasificación](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) valor).
- Desde la tienda 1 **no es** configurado para utilizar `Non-Price` , observe el siguiente sitio web en el orden.
- Desde la tienda 2 **es** configurado para utilizar `Non-Price` atributo (No precio) [Sitio web] = 20,00 $), el precio publicado es de 20,00 $.
