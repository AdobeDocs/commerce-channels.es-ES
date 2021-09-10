---
title: Registros e informes de tienda
description: Utilice los registros y almacene informes para ver qué está sucediendo en la tienda de Adobe o Magento Open Source y en los anuncios de Amazon Marketplace.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Registros y almacene informes

La extensión del canal de ventas de Amazon incluye algunos registros valiosos e informes de almacén que le permiten ver los cambios que están afectando a sus anuncios y pedidos de Amazon. Puede usar estos informes para ver qué está sucediendo en la tienda y para comprender los distintos estados de las listas.

No hay acciones disponibles para los registros o los informes de almacenamiento, ya que son funciones de solo revisión.

Se puede acceder a los siguientes registros desde el [panel de almacenamiento](./amazon-store-dashboard.md).

- El [Registro de cambios en la lista](./listing-changes-log.md) muestra los cambios que se han producido en su cuenta de vendedor de Amazon como un reflejo de la configuración de su canal de ventas de Amazon.

- El [Registro de errores de comunicación](./communication-errors-log.md) muestra los errores de comunicación notificados con Amazon.

Se puede acceder a los siguientes informes específicos del almacén desde el [panel del almacén](./amazon-store-dashboard.md).

- El informe [Análisis de precios competitivos](./competitive-price-analysis.md) muestra que su _precio aterrizado_ de Amazon (precio de listado más precio de envío) en relación con el precio [Buy Box](./buy-box-competitor-pricing.md) y el precio [competidor más bajo](./lowest-competitor-pricing.md).

- El informe [Mejoras en el listado](./listing-improvements.md) muestra todas las mejoras sugeridas en el listado que proporciona Amazon para el almacén seleccionado.

>[!TIP]
>
>También puede consultar el archivo de registro para obtener información adicional cuando sea necesario solucionar el problema. Consulte [configuración de administración del canal de ventas](./sales-channel-settings.md). El registro de sincronización del canal de ventas de Amazon se escribe en el archivo `{Commerce Root}/var/log/channel_amazon.log` y se puede ver en [developer mode](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}.
