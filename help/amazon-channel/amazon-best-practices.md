---
title: Prácticas recomendadas y limitaciones de  [!DNL Amazon sales channel]
description: Revise las prácticas recomendadas y las limitaciones al usar el canal de ventas de Amazon para Adobe Commerce y Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Prácticas recomendadas y limitaciones de [!DNL Amazon sales channel]

Las prácticas recomendadas incluyen:

- El canal de ventas de Amazon puede afectar a los anuncios de Amazon al aumentar o reducir los precios, sincronizar la información del producto (incluidas las existencias disponibles) y agregar, actualizar y finalizar (eliminar) anuncios. Revisa tus anuncios por estado durante la configuración y ajusta tu configuración ([configuración de los anuncios](./listing-settings.md), [reglas de anuncios](./listing-rules.md), [reglas de precios](./pricing-products.md), [invalidaciones](./overrides.md), etc.) antes de completar la configuración de tu tienda. Estos ajustes también se pueden modificar una vez configurados, según sea necesario.

- El canal de ventas de Amazon puede establecer las reglas de precios para ajustar automáticamente el precio del anuncio. Las protecciones automatizadas de precios incluyen las características [precio mínimo](./floor-price.md) y [precio máximo opcional](./optional-ceiling-price.md) de [reglas inteligentes de reasignación de precios](./intelligent-repricing-rules.md). El uso de estas garantías ayuda a garantizar que los precios de su anuncio no vayan por debajo de su coste o por encima de un precio definido.

- La sincronización de datos entre el canal de ventas de Amazon y Amazon está controlada por la configuración de [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). La restricción integrada entre [!DNL Commerce] y Amazon ayuda a garantizar una transmisión de datos fluida y eficiente, pero durante los tiempos de alto tráfico de comercio electrónico (como el Black Friday), los sistemas de Amazon podrían tardar más de lo habitual en actualizarse. Configure su cron [!DNL Commerce] para que se ejecute una vez cada cinco minutos.

- El canal de ventas de Amazon importa la información de pedidos de Amazon. Para administrar los pedidos de Amazon en el canal de ventas de Amazon, debe asegurarse de que la [configuración de pedidos](./order-settings.md) esté definida para importar y crear un pedido de [!DNL Commerce] correspondiente para cada pedido de Amazon. Si no está definida, solo puede ver la información del pedido de Amazon. Todos los impuestos de las ventas a través de Amazon se siguen administrando y enviando a través de su cuenta de [!DNL Amazon Seller Central]. En algunos estados, Amazon debe recaudar y remitir impuestos automáticamente. Para otros estados, los vendedores tienen la opción de calcular los impuestos de forma manual o automática. Ver [Amazon: Políticas Fiscales](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. Es posible que deba iniciar sesión en su cuenta de [!DNL Amazon Seller Central] para ver la documentación de la política fiscal de Amazon.

- Para las regiones del Reino Unido, es recomendable inscribirse en el [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} antes de incorporar el canal de ventas de Amazon.

  >[!NOTE]
  >
  >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

Las limitaciones incluyen:

- Los tipos de paquete, tarjeta regalo y producto agrupado que forman parte de su catálogo [!DNL Commerce] no son compatibles con el canal de ventas de Amazon para incluirlos en Amazon.

- el canal de ventas de Amazon no puede crear un anuncio para un producto que no tenga un anuncio de Amazon existente o anterior. Si un producto no existe en [!DNL Amazon Seller Central] con un ASIN, debe agregarse en [!DNL Amazon Seller Central] para que Amazon pueda asignarle un ASIN. Una vez que se añade un producto en Amazon y se crea un anuncio, este se puede hacer coincidir con el catálogo en el canal de ventas de Amazon y sincronizarse.
