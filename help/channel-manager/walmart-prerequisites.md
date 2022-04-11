---
title: Requisitos previos de Walmart
description: Compruebe que dispone de la información y los recursos necesarios de Walmart Marketplace para integrarse con Channel Manager.
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Requisitos previos de Walmart

Channel Manager requiere los siguientes recursos e información para configurar un canal de ventas de comercio para Walmart Marketplace.

* Aprobación para vender en Walmart y credenciales para iniciar sesión en la cuenta registrada de Marketplace Seller

* Una clave de API para conectar Adobe Commerce o Magento Open Source a Walmart Marketplace

   La clave de la API de Walmart Marketplace permite la integración entre Channel Manager para Adobe Commerce o Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación del Administrador de canales.

## Configuración de una cuenta de vendedor de Marketplace

1. [Envíe su aplicación Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Después de obtener la aprobación de Walmart, [configure su cuenta de vendedor de Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Generar una clave de API de producción de Walmart Marketplace

1. Vaya a Walmart Marketplace para generar un [clave de API de producción del proveedor de soluciones para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Cree la clave y configure los permisos:

   * Seleccione Adobe como proveedor de soluciones.

   * Establezca los permisos como se muestra en la tabla siguiente. Para obtener más información, consulte [Credenciales de API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) en el _Ayuda del vendedor de Walmart Marketplace_.

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

* En las tiendas en directo, las ofertas de productos aparecen en la lista y están disponibles para la venta cuando finaliza la operación de coincidencia.

* En el caso de las tiendas que no están activas, las ofertas de productos están organizadas y no son visibles para los clientes. Cuando la tienda se pone en marcha, los anuncios clasificados se envían automáticamente a la tienda en directo.

![[!DNL Walmart Seller Central] productos clasificados](assets/walmart-seller-central-staged.png)
