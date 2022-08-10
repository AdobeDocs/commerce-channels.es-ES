---
title: Acerca de Amazon y el catálogo de comercio
description: El canal de ventas de Amazon importa sus anuncios de Amazon en el backend de Commerce y se sincroniza continuamente con productos y ventas.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 5d30a5282ede2db0d9619eb2263b733328d26426
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Acerca de Amazon y el [!DNL Commerce] catálogo

El servidor back-end de Adobe Commerce o Magento Open Source incluye un catálogo con todos los productos y la configuración e información asociada (imágenes, opciones, precios, etc.), así como configuraciones de pedidos y envíos. Su [!DNL Amazon Seller Central] cuenta también tiene un catálogo y configuraciones de pedido, lo que hace un seguimiento estricto de las ventas a través de la variable [!DNL Amazon Marketplace].

Para administrar y revisar mejor el catálogo de productos y las ventas a través de una ubicación, el canal de ventas de Amazon importa sus anuncios de Amazon en su [!DNL Commerce] backend, se sincroniza continuamente con productos y ventas, e informa de problemas y tendencias. Admite integraciones con varias [!DNL Amazon Seller Central] , rastreando todos los datos a través de la interfaz única para varias tiendas.

## Atributos del producto

Adobe Commerce y el Magento Open Source administran las sincronizaciones de catálogo mediante el uso del producto [attributes](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} para definir la configuración y los datos del producto. Amazon también utiliza atributos, que se asignarán mediante la incorporación. Durante [tareas previas a la configuración](./amazon-pre-setup-tasks.md) para el canal de ventas de Amazon, debe definir atributos de Amazon adicionales (si es necesario) para garantizar las asignaciones de productos correctas al importar los anuncios de Amazon en su [!DNL Commerce] catálogo. Estos atributos incluyen UPC, EAN, ISBN y ASIN ([!DNL Amazon Standard Identification Number]). Mediante la incorporación, los productos se sincronizan entre Amazon y [!DNL Commerce] catálogos con sus atributos. Asignación adecuada de su [!DNL Commerce] y los productos de Amazon garantizan una sincronización continua de la información del producto, los pedidos y el inventario.

Si no tiene estos atributos creados o configurados para el catálogo, debe agregar un [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} y los valores de sus productos antes de la incorporación. Cuando se importa un atributo de Amazon, puede utilizarse para búsquedas, navegación, reglas de precios y mucho más. Consulte [¿Qué significan ASIN, UPC, EAN, ISBN, SKU y otros códigos de barras?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target=&quot;_blank&quot;}

Después de la incorporación, puede administrar y actualizar los atributos de producto y las asignaciones de Amazon en cualquier momento.

## Listas de productos

Un anuncio de Amazon es una página de producto para cada producto que se vende a través de la variable [!DNL Amazon Marketplace], mostrando descripciones de productos, precios, imágenes y mucho más asignado mediante atributos. Durante la incorporación, puede configurar la [!DNL Commerce] los productos se pueden publicar automáticamente en las listas de Amazon. También puede importar los listados de Amazon existentes asignándolos a su [!DNL Commerce] productos.

Cuando haya creado un listado [!DNL Commerce] se envían a Amazon para su aprobación. La mayoría de los anuncios exitosos se aprueban en unas pocas horas. Si su anuncio está aprobado, aparecerá en la [!DNL Amazon Marketplace] para pedidos inmediatos de clientes. La variable [!DNL Amazon Sales Channel] proporciona un conjunto de pestañas para revisar los listados de Amazon. Según el problema o los datos requeridos, debe revisar su [!DNL Amazon Seller Central] para obtener detalles específicos sobre estas listas.

- [Activo](./active-listings.md): Enumera las listas de productos aprobadas disponibles en el mercado.

- [Listo para la lista](./ready-to-list.md): Enumera los productos que cumplen los requisitos de las reglas de la lista y están listos para publicarse en Amazon.

- [Inactivo](./inactive-listings.md): Enumera los productos que no están disponibles en el mercado debido a que están bloqueados por un motivo específico (como un problema de marca), cerrados y que requieren confianza, etc.

- [Inelegible](./ineligible-listings.md): Debido a las reglas de listado, enumera los productos que no pueden enumerarse activamente en el mercado (como `0` cantidad o fechas de venta).

- [Incompleto](./incomplete-listings.md): Enumera los productos que carecen de la información requerida. Actualice los datos del producto para otra revisión.

- [Finalizado](./ended-listings.md): Enumera las listas de productos que pueden incluirse en la lista pero que se eliminan manualmente de Amazon. Puede volver a listar estos productos.

## Sincronización de datos

Adobe Commerce y el Magento Open Source comunican los datos de producto y pedido entre sus [!DNL Amazon Seller Central] y [!DNL Commerce] backend. Las actualizaciones continuas proporcionan un único origen a través de [!DNL Commerce] para administrar y mantener sus inventarios, cumplir los pedidos, realizar un seguimiento de las ventas y reducir los gastos generales y la duplicación del trabajo. La creación de informes captura los datos más recientes para realizar un seguimiento de las tendencias y resolver los problemas de comunicación entre los dos sistemas.

Toda sincronización se administra mediante una [trabajo cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, configure para que se actualice cada cinco minutos en su [Tareas previas a la configuración](./amazon-pre-setup-tasks.md).
