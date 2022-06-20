---
title: '"[!DNL Walmart] Requisitos"'
description: '"Compruebe que dispone del[!DNL Walmart Marketplace]información y recursos que se integrarán con el administrador de canales".'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 07e1faf90676b404e3f5ee28ddc13d81ea82a5a5
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# [!DNL Walmart] requisitos

[!DNL Channel Manager] requiere los siguientes recursos e información para configurar un [!DNL Commerce] canal de ventas para [!DNL Walmart Marketplace.]

* Aprobación para vender [!DNL Walmart] y credenciales para iniciar sesión en la cuenta registrada del vendedor de Marketplace

* Una clave de API para conectar Adobe Commerce o el Magento Open Source a [!DNL Walmart Marketplace]

   La variable [!DNL Walmart Marketplace] La clave de API permite la integración entre [!DNL Channel Manager] para Adobe Commerce o Magento Open Source y Walmart Marketplace. Configure la clave de API en Seller Central antes de iniciar el proceso de incorporación del Administrador de canales.

## Configure un [!DNL Walmart Seller] account

1. [Envíe su aplicación Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Después de obtener la aprobación de [!DNL Walmart], [configure su cuenta de vendedor de Walmart](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

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
>Después [!DNL Channel Manager] está instalado y configurado, todas las actualizaciones de inventario, precio y pedido se sincronizan automáticamente. No conecte Channel Manager a una tienda de Walmart en directo hasta que no haya deshabilitado ninguna otra integración que actualice los datos de productos y pedidos, y esté listo para que las actualizaciones de Commerce se sincronicen con [!DNL Walmart Marketplace].

