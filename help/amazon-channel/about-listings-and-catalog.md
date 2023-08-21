---
title: Amazon y el catálogo de Commerce
description: El canal de ventas de Amazon importa los anuncios de Amazon en el backend de Commerce y se sincroniza continuamente con los productos y las ventas.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# AMAZON y [!DNL Commerce] Catálogo

El backend de Adobe Commerce o Magento Open Source incluye un catálogo con todos los productos y la configuración e información asociados (imágenes, opciones, precios y mucho más) y configuraciones de pedidos y envíos. Su [!DNL Amazon Seller Central] cuenta también tiene un catálogo y configuraciones de pedidos, rastreando estrictamente sus ventas a través de la [!DNL Amazon Marketplace].

Para administrar y revisar mejor el catálogo de productos y las ventas a través de una ubicación, el canal de ventas de Amazon importa los anuncios de Amazon a su [!DNL Commerce] backend, se sincroniza continuamente con productos y ventas, e informa de problemas y tendencias. Admite integraciones con varios [!DNL Amazon Seller Central] cuentas de, rastreando todos los datos a través de la sola interfaz para varias tiendas.

## Atributos del producto

Adobe Commerce y Magento Open Source administran las sincronizaciones de catálogo con el uso del producto [atributos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) para definir la configuración y los datos del producto. Amazon también utiliza atributos que se van a asignar mediante la incorporación. Durante [tareas previas a la configuración](./amazon-pre-setup-tasks.md) para el canal de ventas de Amazon, puede definir atributos de Amazon adicionales (si es necesario) para garantizar que las asignaciones de productos sean correctas al importar los anuncios de Amazon en su [!DNL Commerce] catálogo. Estos atributos incluyen UPC, EAN, ISBN y ASIN ([!DNL Amazon Standard Identification Number]). Mediante la incorporación, los productos se sincronizan entre Amazon y [!DNL Commerce] catálogos con sus atributos. Asignación adecuada de su [!DNL Commerce] y los productos de Amazon garantizan una sincronización continua de la información del producto, los pedidos y el inventario.

Si no tiene estos atributos creados o configurados para su catálogo, debe agregar un [!DNL Commerce] [atributo de producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) y valores a sus productos antes de la incorporación. Cuando se importa un atributo de Amazon, se puede utilizar para búsquedas, navegación, reglas de precios y mucho más. Consulte [¿Qué significan ASIN, UPC, EAN, ISBN, SKU y otros códigos de barras?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Después de la incorporación, puede administrar y actualizar los atributos del producto y las asignaciones de Amazon en cualquier momento.

## Listados de productos

Una lista de Amazon es una página de producto para cada producto que vende a través de [!DNL Amazon Marketplace], mostrando descripciones de productos, precios, imágenes y mucho más asignados a través de atributos. Durante la incorporación, puede configurar sus [!DNL Commerce] los productos se pueden publicar automáticamente en anuncios de Amazon. También puedes importar tus anuncios de Amazon existentes asignándolos a tu [!DNL Commerce] productos.

Cuando hayas creado un anuncio [!DNL Commerce] productos, se envían a Amazon para su aprobación. La mayoría de los anuncios que han tenido éxito se aprueban en unas horas. Si el anuncio se aprueba, aparecerá en el [!DNL Amazon Marketplace] para pedidos inmediatos de los clientes. El [!DNL Amazon Sales Channel] La extensión de proporciona un conjunto de pestañas para revisar los listados de Amazon. Según el problema o los datos requeridos, debe revisar su [!DNL Amazon Seller Central] Tener en cuenta los detalles específicos de estos anuncios.

- [Activo](./active-listings.md): enumera las listas de productos aprobados disponibles a través del mercado.

- [Listo para la lista](./ready-to-list.md): enumera los productos que cumplen los requisitos de reglas de listado y están listos para publicar en Amazon.

- [Inactivo](./inactive-listings.md): enumera los productos que no están disponibles en el mercado debido a que se bloquearon por un motivo específico (como un problema de marca), se cerraron y requieren volver a ponerse en venta, etc.

- [No apto](./ineligible-listings.md): Debido a las reglas de listado, enumera los productos que no se pueden listar de forma activa en el mercado (como `0` fechas de venta o cantidad).

- [Incompleto](./incomplete-listings.md): enumera los productos que carecen de información necesaria. Actualice los datos del producto para otra revisión.

- [Finalizado](./ended-listings.md): enumera las listas de productos que pueden incluirse en la lista, pero que se han eliminado manualmente de Amazon. Puedes volver a poner en venta estos productos.

## Sincronización de datos

Adobe Commerce y Magento Open Source comunican los datos de productos y pedidos entre sus [!DNL Amazon Seller Central] y la [!DNL Commerce] servidor. Las actualizaciones continuas proporcionan un único origen a través de [!DNL Commerce] para administrar y mantener sus inventarios, cumplir pedidos, realizar un seguimiento de las ventas y reducir los gastos generales y la duplicación del trabajo. Los informes capturan los datos más recientes para rastrear tendencias y resolver problemas de comunicación atrapados entre los dos sistemas.

Toda la sincronización se administra mediante una [trabajo cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html), configurado para actualizar cada cinco minutos en su [Tareas previas a la instalación](./amazon-pre-setup-tasks.md).
