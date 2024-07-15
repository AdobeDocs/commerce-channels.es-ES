---
title: "Introducción a  [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permite a los comerciantes vender productos sin problemas en  [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Introducción a [!DNL Amazon Sales Channel]

Como comerciante de Adobe Commerce o Magento Open Source, puede utilizar la extensión [!DNL Amazon Sales Channel] para integrar sus tiendas con el mayor destino de compras por Internet del mundo. Esta extensión habilita las ventas de Amazon al conectar [!DNL Commerce] con su cuenta de [!DNL Amazon Seller Central] y al proporcionar automatización y sincronización de los datos de catálogo y pedido. Administre completamente todos los listados de Amazon, implemente reglas de precios simples o inteligentes y mantenga sus pedidos e inventario a través de un solo panel de [!DNL Commerce].

Después de la [incorporación](./amazon-onboarding-home.md), [!DNL Commerce] se convierte en un &quot;centro de comandos central&quot; para administrar y controlar los listados de Amazon, los pedidos y el inventario, así como los precios de su tienda Amazon. [Integración de tiendas](./store-integration.md) conecta tu instancia de [!DNL Commerce] y Amazon para sincronizar datos entre ambas plataformas. El canal de ventas de Amazon le permite:

- [Incorpore](./amazon-onboarding-home.md) e integre una o más cuentas de [!DNL Amazon Seller Central] con Adobe Commerce o Magento Open Source.

- Importe y sincronice sus anuncios de Amazon existentes y haga coincidir con los productos de su catálogo [!DNL Commerce], con lo que creará un catálogo de productos centralizado.

- Cree y administre listados de Amazon para productos en su catálogo [!DNL Commerce].

- Ver y cumplir pedidos (de envío) en [!DNL Commerce] y Amazon, sincronizando el estado del pedido, el pago y la información de reembolso.

- Ver registros para análisis y errores de [precios competitivos](./competitive-price-analysis.md), [cambios de listado](./listing-changes-log.md) y [problemas de comunicación](./communication-errors-log.md).

Acceda a sus tiendas Amazon para ver y administrar todas estas funciones, información de cuenta, listados, pedidos y mucho más en la [página de inicio](./amazon-sales-channel-home.md) del canal de ventas de Amazon.

## Promociones y precios

Con la extensión [!DNL Amazon Sales Channel], puede:

- Sincronizar los precios de listado de Amazon con el precio de catálogo [!DNL Commerce] (o atributo de precio alternativo).

- Habilite MSRP [precios de tachado](./listing-price.md#configure-listing-price-settings) en sus anuncios de Amazon para aumentar la propuesta de valor de cliente.

- Habilita y administra [Precio mínimo anunciado (MAP)](./listing-price.md#configure-listing-price-settings) en tus anuncios de Amazon.

- Configura [impuesto sobre el IVA](./listing-price.md#configure-listing-price-settings) adicional en tus precios de Amazon.

- Establece un valor personalizado para &quot;cantidad disponible&quot; en tu [configuración de existencias/cantidad](./stock-quantity.md#configure-stock--quantity-settings) que se mostrará con tus anuncios de Amazon para aumentar la urgencia del comprador.

## Reglas de precios

Con la extensión [!DNL Amazon Sales Channel], puede:

- Cree [reglas de precios](./pricing-products.md) apilables, flexibles y complejas para administrar los precios de Amazon para las promociones diarias o de temporada.

- Cree precios de [suelo](./floor-price.md) y [techo](./optional-ceiling-price.md) para proteger sus precios más bajos y altos.

- Cree y administre [reglas inteligentes de reasignación de precios](./intelligent-repricing-rules.md) que ajusten automáticamente los precios de sus productos en relación con otros competidores de Amazon ([precio más bajo de competidor](./lowest-competitor-pricing.md) y [Buy Box](./buy-box-competitor-pricing.md)).

## Administración de fuentes de catálogo

Con la extensión [!DNL Amazon Sales Channel], puede:

- Importe sus anuncios de Amazon (productos) existentes y haga coincidir con los existentes o cree productos en su catálogo [!DNL Commerce].

- Publish sus productos de [!DNL Commerce] a Amazon para crear anuncios de Amazon.

- Crea [invalidaciones](./creating-editing-overrides.md) para establecer un precio individual, tiempo de manipulación, condición y mensaje de notas del vendedor.

- Importe y asigne [atributos](./attributes-view.md) del producto de sus anuncios de Amazon para que coincidan automáticamente con los productos de su catálogo [!DNL Commerce].

- Defina varios parámetros de búsqueda para que coincidan con los anuncios de Amazon en el catálogo [!DNL Commerce].

- Defina [reglas de listado](./listing-rules.md) para determinar cuáles de sus [!DNL Commerce] productos cumplen los requisitos para listarse en Amazon.

- Establece un [tiempo de manipulación](./product-listing-actions.md) predeterminado para tus nuevos anuncios de Amazon.

- Hacer coincidir las condiciones de listado en función de un atributo [!DNL Commerce].

- Añadir notas del vendedor para cada tipo de condición (opcional).

- Implementar umbrales de cantidad al importar listados de Amazon en el catálogo [!DNL Commerce].

- Ver [mejoras de listado](./listing-improvements.md) recomendadas.

## Gestión de pedidos y servicio al cliente

Con la extensión [!DNL Amazon Sales Channel], puede:

- Soporte técnico y procesamiento de pedidos en Amazon y [!DNL Commerce].

- [Importe](./order-settings.md#configure-order-settings) sus pedidos de Amazon en [!DNL Commerce] o déjelos en Amazon.

- Defina cuál de sus [!DNL Commerce] tiendas de sitios web se asociará con sus pedidos de Amazon para importar y administrar pedidos.

- Ver, cancelar y enviar pedidos de [!DNL Commerce] y/o Amazon según la [configuración de cumplimiento](./fulfilled-by.md).

- Asigne el estado de su pedido de Amazon al estado personalizado en [!DNL Commerce] (opcional).

- Ver y administrar errores de pedidos para resolver problemas y conectarse con clientes.

- Envíe datos de seguimiento de pedidos a su cuenta de [!DNL Amazon Seller Central].

- [Cancelar pedidos](./cancel-unshipped-order.md) y seleccionar una respuesta de motivo.

- Ver la información de [pedidos recientes](./amazon-store-dashboard.md) de sus pedidos de Amazon.

## Informes

Con la extensión [!DNL Amazon Sales Channel], puede revisar la información del informe sobre:

- Anuncios por estados de activo, inactivo, elegible e incompleto.

- Pedidos a la espera de envío.

- Pedidos más recientes.

- Amazon [registro de cambios de anuncio](./listing-changes-log.md) para revisar los cambios de las fuentes de los anuncios o los productos (como precio y cantidad).

- Datos del producto [Buy Box](./buy-box-competitor-pricing.md) de precios del competidor.

- Datos del producto [Precios más bajos para la competencia](./lowest-competitor-pricing.md).

## Soporte para ventas globales

Con la extensión [!DNL Amazon Sales Channel], puede:

- Administrar varias regiones (países) de [!DNL Amazon Marketplace].

- Admitir varias divisas mediante la [herramienta de configuración de divisa de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Administre envíos desde sus ubicaciones de productos y centros de cumplimiento de Amazon.

## Administración de clientes

Genere su base de datos de clientes de [!DNL Commerce] importando los datos de clientes [asociados con sus pedidos de Amazon. ](./order-settings.md#configure-order-settings) Aumente su potencial de marketing a través de esta lista expandida de clientes, a través de sus [!DNL Amazon Marketplace] anuncios y su tienda [!DNL Commerce].


Comenzar es fácil. Un breve proceso de incorporación le guiará a la hora de crear una cuenta de [!DNL Amazon Seller Central] e integrarla con su tienda del canal de ventas de Amazon y su catálogo de [!DNL Commerce] para administrar los listados, los pedidos, el inventario y la satisfacción de pedidos de Amazon. Un panel central muestra las actualizaciones de estado de todas las integraciones de tiendas de canales de ventas de Amazon y los listados de Amazon. Llegue a los nuevos clientes en [!DNL Amazon Marketplace] global con procesos simplificados y automatizados, todo a un costo y mano de obra mínimos o nulos de la configuración de un nuevo sistema.

Después de integrar su cuenta de [!DNL Amazon Seller Central], la extensión [!DNL Amazon Sales Channel] le permite administrar sus cuentas y sincronizar los datos entre [!DNL Commerce] y Amazon. Le permite crear listados, administrar promociones, establecer precios y administrar el inventario y el cumplimiento directamente a través del administrador de [!DNL Commerce]. Estas opciones incluyen reglas de precios que supervisan los precios de Amazon para el mismo artículo y ajustan automáticamente los precios para que sean más competitivos.

