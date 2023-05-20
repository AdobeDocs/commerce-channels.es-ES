---
title: '[!DNL Channel Manager] Notas de la versión'
description: La información de la versión más reciente de [!DNL Channel Manager] de Adobe Commerce.
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: d3acde7aa297ba33dffa7854aa7578985ad12c9b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# [!DNL Channel Manager] Notas de versión

Estas notas de la versión describen la versión inicial de [!DNL Channel Manager] e incluir:

![Nuevo](../assets/new.svg) Nuevas funciones
![Problema corregido](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos


## v2.0.0

*20 de marzo de 2023*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg)<!--CHAN-5893--> Channel Manager ahora es compatible con la versión 2.4.6 de Adobe Commerce.

## v1.1.0

*23 de noviembre de 2022*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg)<!--CHAN-5204--> **Devoluciones y reembolsos**—Ahora puede procesar devoluciones y reembolsos de Walmart Marketplace para pedidos enviados a través de una tienda de Adobe Commerce y Magento Open Source Channel Manager. La información y las actualizaciones sobre devoluciones y reembolsos se sincronizan entre Walmart y Adobe Commerce para que los datos actuales estén disponibles tanto en el [!DNL Commerce] tienda y [!DNL Walmart Marketplace]. Consulte [Pedidos de devolución y reembolso](return-refund-orders.md).

![Fijo](../assets/fix.svg)<!--CHAN-5661--> Se ha corregido el `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` error que se producía al volver a sincronizar el Administrador de canales con los datos de `bin/magento saas:resync --feed orders` comando. El error se resolvió al actualizar las dependencias del paquete del Administrador de canales para el módulo Exportador de datos de ventas, cuyo nombre cambió de `magento/module-sales-data-exporter` hasta `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 de enero de 2022*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) Versión inicial de Channel Manager para disponibilidad general

