---
title: Amazon y el catálogo de Commerce
description: El canal de ventas de Amazon importa los anuncios de Amazon en el backend de Commerce y se sincroniza continuamente con los productos y las ventas.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazon y el catálogo [!DNL Commerce]

El backend de Adobe Commerce o Magento Open Source incluye un catálogo con todos los productos y la configuración e información asociados (imágenes, opciones, precios y mucho más) y configuraciones de pedidos y envíos. Su cuenta de [!DNL Amazon Seller Central] también tiene un catálogo y configuraciones de pedidos, que realiza un seguimiento estricto de sus ventas a través de [!DNL Amazon Marketplace].

Para administrar y revisar mejor el catálogo de productos y las ventas a través de una ubicación, el canal de ventas de Amazon importa los anuncios de Amazon en el backend de [!DNL Commerce], se sincroniza continuamente con los productos y las ventas, e informa de problemas y tendencias. Admite integraciones con varias cuentas de [!DNL Amazon Seller Central], rastreando todos los datos a través de la sola interfaz para varias tiendas.

## Atributos del producto

Adobe Commerce y el Magento Open Source administran las sincronizaciones de catálogo con el uso de [atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) del producto para definir la configuración y los datos del producto. Amazon también utiliza atributos que se van a asignar mediante la incorporación. Durante [las tareas previas a la configuración](./amazon-pre-setup-tasks.md) del canal de ventas de Amazon, usted define atributos de Amazon adicionales (si es necesario) para garantizar asignaciones de productos correctas al importar sus anuncios de Amazon en el catálogo [!DNL Commerce]. Estos atributos incluyen UPC, EAN, ISBN y ASIN ([!DNL Amazon Standard Identification Number]). Mediante la incorporación, los productos se sincronizan entre Amazon y [!DNL Commerce] catálogos usando sus atributos. La asignación adecuada de sus productos de [!DNL Commerce] y Amazon garantiza una sincronización continua de la información del producto, los pedidos y el inventario.

Si no tiene estos atributos creados o configurados para su catálogo, debe agregar un [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) y valores a sus productos antes de la incorporación. Cuando se importa un atributo de Amazon, se puede utilizar para búsquedas, navegación, reglas de precios y mucho más. Ver [¿Qué significan ASIN, UPC, EAN, ISBN, SKU y otros códigos de barras?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Después de la incorporación, puede administrar y actualizar los atributos del producto y las asignaciones de Amazon en cualquier momento.

## Listados de productos

Un listado de Amazon es una página de producto para cada producto que vende a través de [!DNL Amazon Marketplace], que muestra descripciones de productos, precios, imágenes y mucho más asignados a través de atributos. Durante la incorporación, puede configurar que los productos de [!DNL Commerce] se publiquen automáticamente en los anuncios de Amazon. También puedes importar tus anuncios de Amazon existentes asignándolos a tus productos [!DNL Commerce].

Cuando haya creado un listado de [!DNL Commerce] productos, estos se envían a Amazon para su aprobación. La mayoría de los anuncios que han tenido éxito se aprueban en unas horas. Si el anuncio se aprueba, aparecerá en [!DNL Amazon Marketplace] para que los clientes realicen pedidos inmediatos. La extensión [!DNL Amazon Sales Channel] proporciona un conjunto de fichas para revisar los listados de Amazon. En función del problema o de los datos necesarios, deberías revisar tu cuenta de [!DNL Amazon Seller Central] para obtener detalles específicos sobre estos anuncios.

- [Activo](./active-listings.md): enumera las listas de productos aprobados disponibles en el mercado.

- [Listo para publicar](./ready-to-list.md): enumera los productos que cumplen los requisitos de las reglas de listado y están listos para publicar en Amazon.

- [Inactivo](./inactive-listings.md): enumera los productos que no están disponibles en el mercado debido a que se bloquearon por un motivo específico (como un problema de marca), se cerraron y es necesario volver a ponerlos en venta, etc.

- [No apto](./ineligible-listings.md): debido a las reglas de listado, enumera los productos que no pueden listarse de forma activa en el mercado (como `0` cantidad o fechas de venta).

- [Incompleto](./incomplete-listings.md): enumera productos que carecen de la información necesaria. Actualice los datos del producto para otra revisión.

- [Finalizado](./ended-listings.md): enumera las listas de productos que cumplen los requisitos para la inclusión en la lista, pero se eliminan manualmente de Amazon. Puedes volver a poner en venta estos productos.

## Sincronización de datos

Adobe Commerce y el Magento Open Source comunican los datos de productos y pedidos entre su cuenta de [!DNL Amazon Seller Central] y el servidor de [!DNL Commerce]. Las actualizaciones continuas proporcionan un único origen a través de [!DNL Commerce] para administrar y mantener sus inventarios, cumplir pedidos, realizar un seguimiento de las ventas y reducir la sobrecarga y la duplicación de trabajo. Los informes capturan los datos más recientes para rastrear tendencias y resolver problemas de comunicación atrapados entre los dos sistemas.

Toda la sincronización es administrada por un [trabajo cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html), configurado para actualizarse cada cinco minutos en sus [tareas previas a la configuración](./amazon-pre-setup-tasks.md).
