---
title: Prácticas recomendadas y limitaciones para el canal de ventas de Amazon
description: Revise las prácticas recomendadas y las limitaciones al utilizar el canal de ventas de Amazon para Adobe Commerce y Magento Open Source.
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Prácticas recomendadas y limitaciones del canal de ventas de Amazon

Las prácticas recomendadas incluyen:

- El canal de ventas de Amazon puede afectar a sus anuncios de Amazon al aumentar o disminuir los precios, sincronizar la información del producto (incluido el inventario disponible) y agregar, actualizar y finalizar (eliminar) anuncios. Revise sus anuncios por estado durante la configuración y ajuste su configuración ([configuración de listado](./listing-settings.md), [reglas de listado](./listing-rules.md), [reglas de precios](./pricing-products.md), [anulaciones](./overrides.md), etc.) antes de completar la configuración de la tienda. Estos ajustes también se pueden modificar después de la configuración, según sea necesario.

- El canal de ventas de Amazon puede establecer sus reglas de precios para ajustar automáticamente su precio de anuncio. Las garantías de precios automatizadas incluyen las características [floor price](./floor-price.md) y [optional techo price](./optional-ceiling-price.md) de [Intelligent reprice rules](./intelligent-repricing-rules.md). El uso de estas salvaguardias ayuda a garantizar que los precios de su cotización no sean inferiores a su coste o superiores a un precio definido.

- La sincronización de datos entre el canal de ventas de Amazon y Amazon se controla mediante la configuración de [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. La regulación integrada entre [!DNL Commerce] y Amazon ayuda a garantizar una transmisión de datos fluida y eficiente, pero durante los tiempos de tráfico de eCommerce elevado (como Black Friday), los sistemas de Amazon podrían tardar más de lo habitual en actualizarse. Configure el cron [!DNL Commerce] para que se ejecute una vez cada cinco minutos.

- El canal de ventas de Amazon importa la información de pedidos de Amazon. Para administrar los pedidos de Amazon en el canal de ventas de Amazon, debe asegurarse de que la [configuración de pedidos](./order-settings.md) está definida para importar y crear un pedido [!DNL Commerce] correspondiente para cada pedido de Amazon. Si no está definida, solo puede ver la información de pedido de Amazon. Todos los impuestos para ventas a través de Amazon se siguen administrando y enviando a través de su cuenta [!DNL Amazon Seller Central]. En algunos estados, Amazon debe recopilar y remitir impuestos automáticamente. Para otros estados, los vendedores tienen la opción de calcular los impuestos de forma manual o automática. Consulte [Amazon: Directivas de impuestos](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}. Es posible que deba iniciar sesión en su cuenta [!DNL Amazon Seller Central] para ver la documentación de la política fiscal de Amazon.

- Para las regiones del Reino Unido, es recomendable inscribirse en el [Servicio de cálculo del IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;} antes de incorporar el canal de ventas de Amazon.


   >[!NOTE]
   >
   >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

Las limitaciones incluyen:

- El canal de ventas de Amazon no admite paquetes, tarjetas de regalo ni tipos de productos agrupados que forman parte del catálogo [!DNL Commerce] para incluirlos en Amazon.

- El canal de ventas de Amazon no puede crear un listado para un producto que no tiene un listado de Amazon existente o anterior. Si un producto no existe en [!DNL Amazon Seller Central] con un ASIN, debe agregarse en [!DNL Amazon Seller Central] para que Amazon pueda asignar al producto un ASIN. Después de agregar un producto en Amazon y crear un anuncio, el anuncio puede coincidir con el catálogo en el canal de ventas de Amazon y sincronizarse.
