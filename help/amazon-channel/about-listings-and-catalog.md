---
title: Acerca de Amazon y el catálogo de comercio
description: El canal de ventas de Amazon importa sus anuncios de Amazon en el backend de Commerce y se sincroniza continuamente con productos y ventas.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Acerca de Amazon y el catálogo [!DNL Commerce]

El servidor back-end de Adobe Commerce o Magento Open Source incluye un catálogo con todos los productos y configuraciones e información asociadas (imágenes, opciones, precios, etc.) y configuraciones de pedidos y envíos. Su cuenta de [!DNL Amazon Seller Central] también tiene un catálogo y configuraciones de pedido, que hacen un seguimiento estricto de sus ventas a través de [!DNL Amazon Marketplace].

Para administrar y revisar mejor el catálogo de productos y las ventas a través de una ubicación, el canal de ventas de Amazon importa sus listados de Amazon en el back-end [!DNL Commerce], se sincroniza continuamente con productos y ventas, y genera informes sobre problemas y tendencias. Admite integraciones con varias cuentas [!DNL Amazon Seller Central], que rastrean todos los datos a través de la interfaz única para varias tiendas.

## Atributos del producto

Adobe Commerce y el Magento Open Source administran las sincronizaciones de catálogo mediante el uso de [attributes](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} para definir la configuración y los datos del producto. Amazon también utiliza atributos, que se asignarán mediante la incorporación. Durante las [tareas previas a la configuración](./amazon-pre-setup-tasks.md) para el canal de ventas de Amazon, se definen atributos de Amazon adicionales (si son necesarios) para garantizar asignaciones de productos correctas al importar los listados de Amazon a su catálogo [!DNL Commerce]. Estos atributos incluyen UPC, EAN, ISBN y ASIN ([!DNL Amazon Standard Identification Number]). Mediante la incorporación, los productos se sincronizan entre los catálogos Amazon y [!DNL Commerce] utilizando sus atributos. La asignación adecuada de sus productos [!DNL Commerce] y Amazon garantiza una sincronización continua de la información del producto, los pedidos y el inventario.

Si no tiene estos atributos creados o configurados para su catálogo, debe agregar un [!DNL Commerce] [atributo de producto](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} y valores a sus productos antes de la incorporación. Cuando se importa un atributo de Amazon, puede utilizarse para búsquedas, navegación, reglas de precios y mucho más. Para obtener más información sobre estos atributos, consulte [Amazon: ¿Qué son los UPC, EAN, ISBN y ASIN?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Después de la incorporación, puede administrar y actualizar los atributos de producto y las asignaciones de Amazon en cualquier momento.

## Listas de productos

Un listado de Amazon es una página de producto para cada producto que vende a través de [!DNL Amazon Marketplace], que muestra descripciones de productos, precios, imágenes y mucho más asignado mediante atributos. Durante la incorporación, puede configurar que sus productos [!DNL Commerce] se puedan publicar automáticamente en las listas de Amazon. También puede importar los listados de Amazon existentes asignándolos a sus productos [!DNL Commerce] .

Cuando haya creado un listado de [!DNL Commerce] productos, estos se envían a Amazon para su aprobación. La mayoría de los anuncios exitosos se aprueban en unas pocas horas. Si se aprueba su anuncio, aparece en el [!DNL Amazon Marketplace] para pedidos inmediatos por parte de los clientes. La extensión [!DNL Amazon Sales Channel] proporciona un conjunto de pestañas para revisar los listados de Amazon. Según el problema o los datos requeridos, debe revisar su cuenta [!DNL Amazon Seller Central] para obtener detalles específicos sobre estos listados.

- [Activo](./active-listings.md): Enumera las listas de productos aprobadas disponibles en el mercado.

- [Listo para la lista](./ready-to-list.md): Enumera los productos que cumplen los requisitos de las reglas de la lista y están listos para publicarse en Amazon.

- [Inactivo](./inactive-listings.md): Enumera los productos que no están disponibles en el mercado debido a que están bloqueados por un motivo específico (como un problema de marca), cerrados y que requieren confianza, etc.

- [Inelegible](./ineligible-listings.md): Debido a las reglas de la lista, enumera los productos que no pueden aparecer en la lista de marketing (como las fechas de  `0` cantidad o venta).

- [Incompleto](./incomplete-listings.md): Enumera los productos que carecen de la información requerida. Actualice los datos del producto para otra revisión.

- [Finalizado](./ended-listings.md): Enumera las listas de productos que pueden incluirse en la lista pero que se eliminan manualmente de Amazon. Puede volver a listar estos productos.

## Sincronización de datos

Adobe Commerce y el Magento Open Source comunican los datos de producto y pedido entre su cuenta [!DNL Amazon Seller Central] y el back-end [!DNL Commerce]. Las actualizaciones continuas proporcionan una única fuente a través de [!DNL Commerce] para administrar y mantener sus inventarios, cumplir pedidos, rastrear ventas y reducir los gastos generales y la duplicación de trabajo. La creación de informes captura los datos más recientes para realizar un seguimiento de las tendencias y resolver los problemas de comunicación entre los dos sistemas.

Toda la sincronización se administra mediante un [trabajo cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, configurado para actualizarse cada cinco minutos en sus [Tareas previas a la instalación](./amazon-pre-setup-tasks.md).
