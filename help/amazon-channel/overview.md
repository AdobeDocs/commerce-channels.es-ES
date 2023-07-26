---
title: "Introducción a [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permite a los comerciantes vender productos sin problemas en [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Introducción a [!DNL Amazon Sales Channel]

Como comerciante de Adobe Commerce o Magento Open Source, puede utilizar el [!DNL Amazon Sales Channel] extensión para integrar sus tiendas con el mayor destino global de compras por internet del mundo. Esta extensión habilita las ventas de Amazon conectándose [!DNL Commerce] con su [!DNL Amazon Seller Central] y proporciona automatización y sincronización de los datos de catálogo y pedido. Administre completamente todos los listados de Amazon, implemente reglas de precios simples o inteligentes y mantenga sus pedidos e inventario a través de un único [!DNL Commerce] panel.

Después [incorporación](./amazon-onboarding-home.md), [!DNL Commerce] se convierte en un &quot;centro de control central&quot; para administrar y controlar los listados, pedidos e inventario de Amazon, así como los precios de su tienda Amazon. [Integración de tienda](./store-integration.md) conecta su [!DNL Commerce] y Amazon para sincronizar datos entre ambas plataformas. El canal de ventas de Amazon le permite:

- [A bordo](./amazon-onboarding-home.md) e integrar una o más [!DNL Amazon Seller Central] cuentas con Adobe Commerce o Magento Open Source.

- Importe y sincronice sus anuncios de Amazon existentes y vincúlelos con los productos de su [!DNL Commerce] catálogo, crear un catálogo de productos centralizado.

- Crear y administrar listados de Amazon para productos de su [!DNL Commerce] catálogo.

- Ver y cumplir pedidos (de envío) en [!DNL Commerce] y Amazon, sincronizando el estado del pedido, el pago y la información de reembolso.

- Visualización de registros para análisis y errores de [precios competitivos](./competitive-price-analysis.md), [enumerar cambios](./listing-changes-log.md), y [problemas de comunicación](./communication-errors-log.md).

Acceda a sus tiendas Amazon para ver y administrar todas estas funciones, información de cuenta, anuncios, pedidos y mucho más en el canal de ventas de Amazon [página principal](./amazon-sales-channel-home.md).

## Promociones y precios

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede:

- Sincronizar precios de listado de Amazon con [!DNL Commerce] precio de catálogo (o atributo de precio alternativo).

- Habilitar MSRP [precios de liquidación](./listing-price.md#configure-listing-price-settings) en tus anuncios de Amazon para aumentar la propuesta de valor del cliente.

- Habilitar y administrar [Precio Mínimo Anunciado (MAP)](./listing-price.md#configure-listing-price-settings) en tus anuncios de Amazon.

- Configuración de más [IVA](./listing-price.md#configure-listing-price-settings) en los precios de Amazon.

- Establezca un valor personalizado para &quot;cantidad disponible&quot; en su [configuración de stock/cantidad](./stock-quantity.md#configure-stock--quantity-settings) para mostrar con tus anuncios de Amazon para aumentar la urgencia del comprador.

## Reglas de precios

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede:

- Crear apilables, flexibles y complejas [reglas de precios](./pricing-products.md) para administrar los precios de Amazon para promociones diarias o de temporada.

- Crear [suelo](./floor-price.md) y [techo](./optional-ceiling-price.md) precios para proteger sus precios más bajos y más altos.

- Crear y administrar [reglas inteligentes de reasignación de precios](./intelligent-repricing-rules.md) que ajustan automáticamente los precios de sus productos en relación con otros competidores de Amazon ([competidor más bajo](./lowest-competitor-pricing.md) y [Buy Box](./buy-box-competitor-pricing.md) precio).

## Administración de fuentes de catálogo

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede:

- Importe sus anuncios de Amazon (productos) existentes y haga coincidir con los existentes o cree productos en su [!DNL Commerce] catálogo.

- Publique su [!DNL Commerce] productos a Amazon para crear anuncios de Amazon.

- Crear [invalidaciones](./creating-editing-overrides.md) para establecer un mensaje de precio, tiempo de manipulación, condición y notas del vendedor individual.

- Importación y asignación de productos [atributos](./attributes-view.md) de tus anuncios de Amazon para que coincidan automáticamente con los productos de tu [!DNL Commerce] catálogo.

- Defina varios parámetros de búsqueda para que coincidan con los anuncios de Amazon [!DNL Commerce] catálogo.

- Definir [enumerar reglas](./listing-rules.md) para determinar cuál de sus [!DNL Commerce] los productos pueden aparecer en la lista de Amazon.

- Establecer un valor predeterminado [tiempo manipulación](./product-listing-actions.md) para tus nuevos anuncios de Amazon.

- Hacer coincidir condiciones de listado basadas en un [!DNL Commerce] atributo.

- Añadir notas del vendedor para cada tipo de condición (opcional).

- Implemente umbrales de cantidad al importar listados de Amazon en su [!DNL Commerce] catálogo.

- Vista recomendada [mejoras de listado](./listing-improvements.md).

## Gestión de pedidos y servicio al cliente

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede:

- Soporte y procesamiento de pedidos en Amazon y [!DNL Commerce].

- [Importar](./order-settings.md#configure-order-settings) sus pedidos de Amazon a [!DNL Commerce] o déjelas en Amazon.

- Defina cuál de sus [!DNL Commerce] tiendas de sitios web que se asocian a los pedidos de Amazon para importar y administrar pedidos.

- Ver, cancelar y enviar pedidos desde [!DNL Commerce] y/o Amazon según su [configuración de cumplimiento](./fulfilled-by.md).

- Asignación del estado del pedido de Amazon al estado personalizado en [!DNL Commerce] (opcional).

- Ver y administrar errores de pedidos para resolver problemas y conectarse con clientes.

- Envíe datos de seguimiento de pedidos a su [!DNL Amazon Seller Central] cuenta.

- [Cancelar pedidos](./cancel-unshipped-order.md) y seleccione una respuesta de motivo.

- Ver el [pedido reciente](./amazon-store-dashboard.md) para sus pedidos de Amazon.

## Informes

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede revisar la información del informe sobre:

- Anuncios por estados de activo, inactivo, elegible e incompleto.

- Pedidos a la espera de envío.

- Pedidos más recientes.

- Amazon [registro de cambios de listado](./listing-changes-log.md) para revisar los cambios en la fuente del producto/anuncio (como precio y cantidad).

- Product [Buy Box](./buy-box-competitor-pricing.md) Datos de precios del competidor.

- Product [Precios más bajos para competidores](./lowest-competitor-pricing.md) datos.

## Soporte para ventas globales

Con el [!DNL Amazon Sales Channel] Con esta extensión, puede:

- Administrar varios [!DNL Amazon Marketplace] regiones (países).

- Admitir varias monedas mediante [Herramienta de configuración de moneda de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Administre envíos desde sus ubicaciones de productos y centros de cumplimiento de Amazon.

## Administración de clientes

Cree su [!DNL Commerce] base de datos de clientes por [importación de datos de clientes](./order-settings.md#configure-order-settings) asociadas a sus pedidos de Amazon. Aumente su potencial de marketing a través de esta lista ampliada de clientes y de sus [!DNL Amazon Marketplace] listados y [!DNL Commerce] tienda.


Comenzar es fácil. Un breve proceso de incorporación le guiará en la creación de un [!DNL Amazon Seller Central] y la integración con su tienda de canales de ventas de Amazon y su [!DNL Commerce] catálogo para administrar listados, pedidos, inventario y satisfacción de pedidos de Amazon. Un panel central muestra las actualizaciones de estado de todas las integraciones de tiendas de canales de ventas de Amazon y los listados de Amazon. Llegue a nuevos clientes en la [!DNL Amazon Marketplace] con procesos simplificados y automatizados, todo a un costo mínimo o ninguno de los costos y mano de obra de la creación de un nuevo sistema.

Después de integrar su [!DNL Amazon Seller Central] cuenta, la [!DNL Amazon Sales Channel] La extensión de permite administrar las cuentas y sincronizar datos entre [!DNL Commerce] y Amazon. Permite crear listados, gestionar promociones, fijar precios y gestionar inventario y satisfacción de pedidos directamente a través de [!DNL Commerce] Administrador. Estas opciones incluyen reglas de precios que supervisan los precios de Amazon para el mismo artículo y ajustan automáticamente los precios para que sean más competitivos.

