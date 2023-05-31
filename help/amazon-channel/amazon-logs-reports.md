---
title: Registros e informes de tienda para listados de Amazon
description: Utilice los registros y los informes de tienda para ver qué está sucediendo en su tienda Adobe Commerce o de Magento Open Source y en sus anuncios de Amazon Marketplace.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Registros e informes de tienda para listados de Amazon

La extensión de canal de ventas de Amazon incluye algunos registros valiosos e informes de tienda que le permiten ver los cambios que afectan a los anuncios y pedidos de Amazon. Puedes usar estos informes para ver lo que está sucediendo en tu tienda y entender los distintos estados de las mismas.

No hay acciones disponibles para los registros o los informes de tienda, ya que son funciones de solo revisión.

Se puede acceder a los siguientes registros desde el [tablero de tienda](./amazon-store-dashboard.md).

- El [Registro de cambios de lista](./listing-changes-log.md) muestra los cambios que se han producido en tu cuenta de vendedor de Amazon como reflejo de la configuración de tu canal de ventas de Amazon.

- El [Registro de errores de comunicación](./communication-errors-log.md) muestra los errores de comunicación notificados con Amazon.

Se puede acceder a los siguientes informes específicos del almacén desde el [tablero de tienda](./amazon-store-dashboard.md).

- El [Análisis de precios competitivos](./competitive-price-analysis.md) El informe muestra que su Amazon _precio aterrizado_ (precio de venta más precio de envío) en relación con el [Buy Box](./buy-box-competitor-pricing.md) precio y [competidor más bajo](./lowest-competitor-pricing.md) precio.

- El [Mejoras de anuncios](./listing-improvements.md) Este informe muestra todas las mejoras de anuncio sugeridas proporcionadas por Amazon para la tienda seleccionada.

>[!TIP]
>
>También puede buscar información adicional en el archivo de registro cuando necesite solucionar problemas. Consulte [Configuración de administración del canal de ventas](./sales-channel-settings.md). el registro de sincronización del canal de ventas de Amazon se escribe en `{Commerce Root}/var/log/channel_amazon.log` y se pueden ver en [modo de desarrollador](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
