---
title: Registros e informes de tienda para listados de Amazon
description: Utilice los registros y los informes de tienda para ver qué está sucediendo en su tienda Adobe Commerce o de Magento Open Source y en sus anuncios de Amazon Marketplace.
feature: Sales Channels, Logs
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Registros e informes de tienda para listados de Amazon

La extensión de canal de ventas de Amazon incluye algunos registros valiosos e informes de tienda que le permiten ver los cambios que afectan a los anuncios y pedidos de Amazon. Puedes usar estos informes para ver lo que está sucediendo en tu tienda y entender los distintos estados de las mismas.

No hay acciones disponibles para los registros o los informes de tienda, ya que son funciones de solo revisión.

Se puede acceder a los siguientes registros desde el [tablero del almacén](./amazon-store-dashboard.md).

- El [registro de cambios del anuncio](./listing-changes-log.md) muestra los cambios que se han producido en tu cuenta de vendedor de Amazon como reflejo de la configuración de tu canal de ventas de Amazon.

- El [registro de errores de comunicación](./communication-errors-log.md) muestra los errores de comunicación notificados con Amazon.

Se puede obtener acceso a los siguientes informes específicos de la tienda desde el [tablero de la tienda](./amazon-store-dashboard.md).

- El informe de [Análisis de precios competitivos](./competitive-price-analysis.md) muestra que tu Amazon _precio de aterrizaje_ (precio de anuncio más precio de envío) está relacionado con el precio de [Buy Box](./buy-box-competitor-pricing.md) y el precio de [competidor más bajo](./lowest-competitor-pricing.md).

- El informe [Mejoras de anuncios](./listing-improvements.md) muestra todas las mejoras de anuncios sugeridas que proporciona Amazon para la tienda seleccionada.

>[!TIP]
>
>También puede buscar información adicional en el archivo de registro cuando necesite solucionar problemas. Consulte [configuración de administración de canales de ventas](./sales-channel-settings.md). el registro de sincronización del canal de ventas de Amazon se ha escrito en el archivo `{Commerce Root}/var/log/channel_amazon.log` y se puede ver en [modo de desarrollador](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
