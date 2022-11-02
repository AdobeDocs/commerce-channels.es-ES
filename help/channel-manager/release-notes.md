---
title: '[!DNLChannel Manager] Notas de la versión'
description: '"La información de la última versión de [!DNL Channel Manager] de Adobe Commerce".'
source-git-commit: 501a76a126f090805f95e64078ec2c73de003aa4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# [!DNL Channel Manager] Notas de la versión

Estas notas de la versión describen la versión inicial de [!DNL Channel Manager] e incluyen:

![Nuevo](../assets/new.svg) Nuevas funciones
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos


## Versión 1.1.0

![Nuevo](../assets/new.svg)<!--CHAN-5204--> **Devoluciones y reembolsos**: ahora puede procesar devoluciones y reembolsos de Walmart Marketplace para pedidos enviados a través de una tienda de Adobe Commerce y Magento Open Source Channel Manager. La información y las actualizaciones sobre devoluciones y reembolsos se sincronizan entre Walmart y Adobe Commerce para que los datos actuales estén disponibles tanto en la variable [!DNL Commerce] tienda y [!DNL Walmart Marketplace]. Consulte [Pedidos de devolución y devolución](return-refund-orders.md).

![Fijo](../assets/fix.svg)<!--CHAN-5661--> Se ha corregido la variable `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` error que se producía al volver a sincronizar el Administrador de canales solicita datos mediante la variable `bin/magento saas:resync --feed orders` comando. El error se resolvió actualizando las dependencias del paquete del Administrador de canales para el módulo del Exportador de datos de ventas, desde el que se cambió el nombre `magento/module-sales-data-exporter` a `magento/module-sales-orders-data-exporter`.

## v1.0.0

Versión inicial, compatible con las siguientes versiones de Commerce:

* Código abierto (CE): 2.4.x
* Adobe Commerce (EE): 2.4.x
* Adobe Commerce para Cloud (ECE): 2.4.x
* Estabilidad: Estable
