---
title: '[!DNL Walmart] Requisitos'
description: '''Compruebe que dispone de los [!DNL Walmart Marketplace]información y recursos para integrar con Channel Manager".'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] Requisitos

[!DNL Channel Manager] requiere los siguientes recursos e información para configurar un [!DNL Commerce] canal de ventas para [!DNL Walmart Marketplace.]

* A [!DNL Walmart] Cuenta de vendedor

* Una clave de API para conectar Adobe Commerce o Magento Open Source a [!DNL Walmart Marketplace]

  El [!DNL Walmart Marketplace] La clave de API permite la integración entre [!DNL Channel Manager] para Adobe [!DNL Commerce] o Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación a Channel Manager.

## Configuración de un [!DNL Walmart Seller] account

Vaya a la [!DNL Walmart Seller Center] para configurar su [Cuenta de vendedor de Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Generación de un [!DNL Walmart Marketplace] Clave de API de producción

1. Ir a [!DNL Walmart Marketplace] para generar un [clave de API de producción del proveedor de soluciones para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Cree la clave y configure los permisos:

   * Seleccione Adobe como proveedor de soluciones.

   * Establezca los permisos como se muestra en la tabla siguiente. Para obtener más información, consulte [Credenciales de API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) en el _Ayuda para vendedores de Walmart Marketplace_.

   **Configuración de la clave API de Adobe para Walmart**

   | **Permiso** | **Configuración** |
   |----------------|-------------|
   | Contenido | Acceso total |
   | Obtener fuentes | Solo ver |
   | Inventario | Acceso total |
   | Elementos | Acceso total |
   | Tiempo de retardo | Acceso total |
   | Pedido | Acceso total |
   | Precio | Acceso total |
   | Informes | Solo ver |
   | Devuelve | Acceso total |
   | Reglas | Acceso total |
   | Envío | Acceso total |

## [!DNL Walmart Marketplace] Estado del almacén

Al conectar los productos al mercado, la disponibilidad de la lista depende del estado de su [!DNL Walmart Marketplace] tiendas:

* En las tiendas en directo, las ofertas de productos aparecen en la lista y están disponibles para la venta cuando finaliza la operación de coincidencia.

* En el caso de las tiendas que no están activas, las ofertas de productos se muestran por fases y no son visibles para los clientes. Si la variable [!DNL Walmart Marketplace] La tienda se activa y los anuncios clasificados se transfieren automáticamente a la tienda activa.

![[!DNL Walmart Seller Central] productos clasificados](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>Después [!DNL Channel Manager] está instalado y configurado, todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. No conectar [!DNL Channel Manager] a una tienda Walmart Marketplace activa hasta que haya deshabilitado cualquier otra integración que actualice los datos de productos y pedidos. Si tenía otras integraciones configuradas, compruebe que la cantidad y los precios del artículo estén en [!DNL Commerce] hacer coincidir las cantidades en [!DNL Walmart Marketplace] antes de conectarse a una tienda en directo.

