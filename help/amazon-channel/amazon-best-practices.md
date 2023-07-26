---
title: Prácticas recomendadas y limitaciones para [!DNL Amazon sales channel]
description: Revise las prácticas recomendadas y las limitaciones al usar el canal de ventas de Amazon para Adobe Commerce y Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Prácticas recomendadas y limitaciones para [!DNL Amazon sales channel]

Las prácticas recomendadas incluyen:

- El canal de ventas de Amazon puede afectar a los anuncios de Amazon al aumentar o reducir los precios, sincronizar la información del producto (incluidas las existencias disponibles) y agregar, actualizar y finalizar (eliminar) anuncios. Revisa tus anuncios por estado durante la configuración y ajusta tu configuración ([configuración de listado](./listing-settings.md), [enumerar reglas](./listing-rules.md), [reglas de precios](./pricing-products.md), [invalidaciones](./overrides.md), etc.) antes de completar la configuración de la tienda. Estos ajustes también se pueden modificar una vez configurados, según sea necesario.

- El canal de ventas de Amazon puede establecer las reglas de precios para ajustar automáticamente el precio del anuncio. Las protecciones de precios automatizadas incluyen [precio mínimo](./floor-price.md) y [precio máximo opcional](./optional-ceiling-price.md) características de [Reglas de reasignación de precios inteligentes](./intelligent-repricing-rules.md). El uso de estas garantías ayuda a garantizar que los precios de su anuncio no vayan por debajo de su coste o por encima de un precio definido.

- La sincronización de datos entre el canal de ventas de Amazon y Amazon está controlada por su [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) configuración. Regulación integrada entre [!DNL Commerce] y Amazon ayudan a garantizar una transmisión de datos fluida y eficaz, pero durante los tiempos de alto tráfico de comercio electrónico (como el Black Friday), los sistemas de Amazon podrían tardar más de lo habitual en actualizarse. Configure su [!DNL Commerce] cron se ejecuta una vez cada cinco minutos.

- El canal de ventas de Amazon importa la información de pedidos de Amazon. Para administrar los pedidos de Amazon en el canal de ventas de Amazon, debe asegurarse de que su [configuración de pedidos](./order-settings.md) están definidos para importar y crear una [!DNL Commerce] para cada pedido de Amazon. Si no está definida, solo puede ver la información del pedido de Amazon. Todos los impuestos de las ventas a través de Amazon se siguen gestionando y remitiendo a través de su [!DNL Amazon Seller Central] cuenta. En algunos estados, Amazon debe recaudar y remitir impuestos automáticamente. Para otros estados, los vendedores tienen la opción de calcular los impuestos de forma manual o automática. Consulte [Amazon: Políticas Fiscales](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. Es posible que deba iniciar sesión en su [!DNL Amazon Seller Central] cuenta para ver la documentación de la política fiscal de Amazon.

- Para las regiones del Reino Unido, es una práctica recomendada inscribirse en el [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} antes de incorporar el canal de ventas de Amazon.

  >[!NOTE]
  >
  >Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

Las limitaciones incluyen:

- Los tipos de paquete, tarjeta regalo y productos agrupados que forman parte de su [!DNL Commerce] el canal de ventas de Amazon no admite catálogos para publicar anuncios en Amazon.

- el canal de ventas de Amazon no puede crear un anuncio para un producto que no tenga un anuncio de Amazon existente o anterior. Si un producto no existe en [!DNL Amazon Seller Central] con un ASIN, debe añadirse en [!DNL Amazon Seller Central] para que Amazon pueda asignar al producto un ASIN. Una vez que se añade un producto en Amazon y se crea un anuncio, este se puede hacer coincidir con el catálogo en el canal de ventas de Amazon y sincronizarse.
