---
title: '''[!DNL Walmart] Requisitos"'
description: 'Compruebe que dispone del [!DNL Walmart Marketplace]información y recursos que se integrarán con el administrador de canales.'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 618bbd6d6c889d555f0ff74ade3dd84b412e1e59
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] requisitos

[!DNL Channel Manager] requiere los siguientes recursos e información para configurar un [!DNL Commerce] canal de ventas para [!DNL Walmart Marketplace.]

* A [!DNL Walmart] Cuenta de vendedor

* Una clave de API para conectar Adobe Commerce o el Magento Open Source a [!DNL Walmart Marketplace]

   La variable [!DNL Walmart Marketplace] La clave de API permite la integración entre [!DNL Channel Manager] para Adobe [!DNL Commerce] o Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación del Administrador de canales.

## Configure un [!DNL Walmart Seller] account

Vaya a la [!DNL Walmart Seller Center] para configurar su [Cuenta de vendedor Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Genere un [!DNL Walmart Marketplace] Clave de API de producción

1. Vaya a [!DNL Walmart Marketplace] para generar un [clave de API de producción del proveedor de soluciones para Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

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

## [!DNL Walmart Marketplace] Estado de la tienda

Al conectar productos al mercado, la disponibilidad de los anuncios depende del estado de su [!DNL Walmart Marketplace] tiendas:

* En las tiendas en directo, las ofertas de productos aparecen en la lista y están disponibles para la venta cuando finaliza la operación de coincidencia.

* En el caso de las tiendas que no están activas, las ofertas de productos están organizadas y no son visibles para los clientes. Cuando la variable [!DNL Walmart Marketplace] la tienda se activa, los anuncios clasificados por etapas se envían automáticamente a la tienda en directo.

![[!DNL Walmart Seller Central] productos clasificados](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>Después [!DNL Channel Manager] está instalado y configurado, todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. No conectar [!DNL Channel Manager] a una tienda de Walmart en directo hasta que haya deshabilitado cualquier otra integración que actualice los datos de productos y pedidos. Si tenía otras integraciones configuradas, compruebe que la cantidad y los precios del artículo estén en [!DNL Commerce] coincide con las cantidades de [!DNL Walmart Marketplace] antes de conectarse a una tienda en directo.

