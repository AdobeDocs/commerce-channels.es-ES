---
title: '[!DNL Walmart] requisitos'
description: '"Compruebe que dispone de la información y los recursos necesarios para la integración con Channel Manager." [!DNL Walmart Marketplace]'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Requisitos de [!DNL Walmart]

[!DNL Channel Manager] requiere los siguientes recursos e información para configurar un canal de ventas de [!DNL Commerce] para [!DNL Walmart Marketplace.]

* Cuenta de vendedor de [!DNL Walmart]

* Una clave de API para conectar Adobe Commerce o Magento Open Source a [!DNL Walmart Marketplace]

  La clave de API [!DNL Walmart Marketplace] permite la integración entre [!DNL Channel Manager] para el Adobe [!DNL Commerce] o el Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación a Channel Manager.

## Configurar una cuenta de [!DNL Walmart Seller]

Ve a [!DNL Walmart Seller Center] para configurar tu [cuenta de vendedor de Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Generar una clave de API de producción [!DNL Walmart Marketplace]

1. Vaya a [!DNL Walmart Marketplace] para generar una clave de API de producción del proveedor de soluciones [para el Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Cree la clave y configure los permisos:

   * Seleccione Adobe como proveedor de soluciones.

   * Establezca los permisos como se muestra en la tabla siguiente. Para obtener más información, consulte [Credenciales de API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) en la _Ayuda para vendedores de Walmart Marketplace_.

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

## [!DNL Walmart Marketplace] estado de tienda

Al conectar productos al mercado, la disponibilidad del anuncio depende del estado de las tiendas de [!DNL Walmart Marketplace]:

* En las tiendas en directo, las ofertas de productos aparecen en la lista y están disponibles para la venta cuando finaliza la operación de coincidencia.

* En el caso de las tiendas que no están activas, las ofertas de productos se muestran por fases y no son visibles para los clientes. Cuando se activa la tienda [!DNL Walmart Marketplace], los anuncios clasificados se insertan automáticamente en la tienda activa.

![[!DNL Walmart Seller Central] productos clasificados](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>Después de instalar y configurar [!DNL Channel Manager], todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. No conecte [!DNL Channel Manager] a una tienda de Walmart Marketplace activa hasta que haya deshabilitado cualquier otra integración que actualice los datos de productos y pedidos. Si tenía otras integraciones configuradas, compruebe que la cantidad y los precios del artículo en [!DNL Commerce] coinciden con las cantidades en [!DNL Walmart Marketplace] antes de conectarse a una tienda activa.

