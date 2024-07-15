---
title: '[!DNL Channel Manager] notas de la versión'
description: La información de la versión más reciente de  [!DNL Channel Manager]  de Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Notas de la versión [!DNL Channel Manager]

Estas notas de la versión describen la versión inicial de [!DNL Channel Manager] e incluyen:

![Nuevas](../assets/new.svg) nuevas características
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para obtener más información sobre las programaciones de versiones y la compatibilidad.

Consulte [Disponibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para saber qué versiones de Adobe Commerce admiten esta extensión.

## Versión 2.1.0

*3 de octubre de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

El nuevo Administrador de canales ![New](../assets/new.svg) ya es compatible con las versiones [Adobe Commerce versión 2.4.7 beta](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html).

## Versión 2.0.0

*20 de marzo de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![El nuevo Administrador de canales](../assets/new.svg)<!--CHAN-5893--> ya es compatible con la versión 2.4.6 de Adobe Commerce.

## Versión 1.1.0

*23 de noviembre de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg)<!--CHAN-5204--> **Devoluciones y reembolsos**: ahora puede procesar devoluciones y reembolsos de Walmart Marketplace para pedidos enviados a través de una tienda de Adobe Commerce y Magento Open Source Channel Manager. La información y las actualizaciones sobre devoluciones y reembolsos se sincronizan entre Walmart y Adobe Commerce para que los datos actuales estén disponibles tanto en la tienda [!DNL Commerce] como en [!DNL Walmart Marketplace]. Ver [Pedidos de devolución y reembolso](return-refund-orders.md).

![Corregido](../assets/fix.svg)<!--CHAN-5661--> Se ha corregido el error `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` que se producía al resincronizar el Administrador de canales para datos usando el comando `bin/magento saas:resync --feed orders`. El error se resolvió al actualizar las dependencias del paquete del Administrador de canales para el módulo Exportador de datos de ventas, cuyo nombre cambió de `magento/module-sales-data-exporter` a `magento/module-sales-orders-data-exporter`.

## Versión 1.0.0

*14 de enero de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) lanzamiento inicial de Channel Manager para disponibilidad general

