---
title: Acerca de [!DNL Channel Manager]
description: Obtenga información sobre cómo instalar y utilizar [!DNL Channel Manager] para integrar tiendas de Adobe Commerce y Magento Open Source con mercados de terceros, y crear un canal de ventas para administrar ofertas de venta, precios, inventarios y ventas sin problemas desde su administrador de comercio.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ac084bf968a262dd4e7f6b6040aea2e6dc6197c2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# Información general

El Administrador de canales para Adobe Commerce y Magento Open Source proporciona un cómodo espacio de trabajo en el Administrador para administrar las ventas de canal en mercados de terceros como Walmart, Amazon y eBay. Aumente las ventas y amplíe a nuevos mercados mientras gestiona las operaciones del canal de ventas sin problemas desde el administrador de comercio.

![[!DNL Channel Manager] vista de administración de extensiones](assets/channel-manager-admin-entry-page.png)

## Información general sobre la versión beta

La versión beta de Channel Manager es compatible con los vendedores de Adobe Commerce o Magento Open Source que desean ofrecer productos en Walmart Marketplace.

Esta versión es compatible con las siguientes capacidades para administrar las operaciones del canal de ventas:

* Establecer una conexión API entre Adobe Commerce o Magento Open Source y Walmart Marketplace

* Publicar productos de Channel Manager en Walmart mediante la coincidencia de productos

* Ver el estado de la lista de productos en el Administrador de canales, por ejemplo *borrador*, *procesamiento*, *matched*, *error*.

* Sincronizar las cantidades de inventario de los productos coincidentes desde Commerce a Walmart

* Sincronizar los precios de catálogo de los productos coincidentes desde Commerce a Walmart

* Reciba pedidos de Walmart Marketplace y visualícelos en el [!DNL Commerce] panel de pedidos

### Latencia esperada para las operaciones del Administrador de canales

Los procesos de sincronización de datos entre [!DNL Channel Manager] y un [!DNL Walmart Marketplace] la tienda requiere un poco de tiempo para completarse. Revise el tiempo de procesamiento esperado para [!DNL Channel Manager] para ayudar a planificar las operaciones del canal de ventas.

**Latencia estimada para operaciones del Administrador de canales**

| **Operación** | **Descripción** | **Retraso esperado** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Agregar productos al Administrador de canales | Seleccione productos del catálogo de productos de Commerce e impórtelos en el Administrador de canales. | **Hasta 5 minutos**-Si selecciona muchos productos, por ejemplo, un catálogo completo de productos, el proceso de importación tarda más. |
| Hacer coincidir productos en Walmart Marketplace | Seleccione las listas de productos en Channel Manager y envíelas a Walmart para que coincidan. | **Hasta 30 minutos**-Si selecciona muchos productos, el proceso de coincidencia tardará más en función de la cantidad seleccionada. |
| Actualizaciones de inventario | Cuando la cantidad de inventario cambia en Commerce. Channel Manager sincroniza la actualización con Walmart. | **Hasta 10 minutos** |
| Actualizaciones de precios | Cuando el precio de un producto cambia, Channel Manager sincroniza la actualización con Walmart. | **Hasta 5 minutos** |
| Solicite sincronizaciones de Walmart a Commerce | El cliente solicita un producto Commerce en el mercado Walmart. Walmart envía el pedido a Channel Manager. El orden se muestra en el panel de pedidos. | **Hasta 30 minutos** |
| Pedido creado en Commerce Order Management | Channel Manager crea el pedido de comercio a partir del pedido de Walmart y actualiza el panel de pedidos para incluir el número de pedido de comercio. | **Hasta 5 minutos** |

## Requisitos previos de Walmart

Necesita la siguiente información de Walmart para integrar Commerce con Walmart Marketplace:

* Aprobación para vender en Walmart y credenciales para iniciar sesión en la cuenta registrada de Marketplace Seller

* Una clave de API para conectar Adobe Commerce o Magento Open Source a Walmart Marketplace

   La clave de la API de Walmart Marketplace permite la integración entre Channel Manager para Adobe Commerce o Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación del Administrador de canales.

### Configuración de una cuenta de vendedor de Marketplace

1. [Envíe su aplicación Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. Después de obtener la aprobación de Walmart, [configure su cuenta de vendedor de Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Generar una clave de API de Walmart Marketplace

1. Vaya a Walmart Marketplace para generar un [clave de API de producción del proveedor de soluciones para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Cree la clave y configure los permisos:

   * Seleccione Adobe como proveedor de soluciones.

   * Establezca los permisos como se muestra en la tabla siguiente. Para obtener más información, consulte [Credenciales de API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) en el *Ayuda del vendedor de Walmart Marketplace*.

   **Configuración clave de API de Adobe para Walmart**

   | **Permiso** | **Configuración** |
   |----------------|-------------|
   | Contenido | Acceso completo |
   | Obtener fuentes | Ver solo |
   | Inventario | Acceso completo |
   | Elementos | Acceso completo |
   | Tiempo de retraso | Acceso completo |
   | Pedido | Acceso completo |
   | Precio | Acceso completo |
   | Informes | Ver solo |
   | Devuelve | Acceso completo |
   | Reglas | Acceso completo |
   | Envío | Acceso completo |

## Estado de Walmart Marketplace Store

Cuando publica productos en Walmart Marketplace, la disponibilidad de los anuncios depende del estado de sus tiendas Walmart:

* En las tiendas en directo, las ofertas de productos se enumeran y están disponibles para la venta en cuanto se complete la operación de coincidencia.

* En el caso de las tiendas que no están activas, las ofertas de productos están organizadas y no son visibles para los clientes. Tan pronto como la tienda entre en funcionamiento, los anuncios clasificados por etapas se envían automáticamente a la tienda en directo.


![[!DNL Walmart Seller Central] productos clasificados](assets/walmart-seller-central-staged.png)
