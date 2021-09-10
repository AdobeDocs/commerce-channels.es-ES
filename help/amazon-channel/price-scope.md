---
title: Alcance del precio
description: Utilice el ámbito de precios de Commerce para administrar los precios según varios sitios web o globalmente.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Ámbito del precio

[!DNL Commerce] proporciona configuración para el ámbito [ de ](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price)precios{:target=&quot;_blank&quot;} que se debe configurar en  `Global` o  `Website`. Si el precio se establece en `Global`, existe una única fuente de precios para todos los sitios web. Si el precio está establecido en `Website`, los sitios web pueden variar sus precios entre sí y también tienen un valor de precio predeterminado de reserva. Consulte [Precio del catálogo](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} en la guía del usuario principal de Commerce.

Si cambia el ámbito del precio del catálogo de `Global` a `Website`, todos los atributos de tipo de precio también cambian a `Website`. Consulte [Adición de sitios web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target=&quot;_blank&quot;}.

Cuando se elige el precio de un sitio web, hay dos fuentes de precios:

- El precio del sitio web
- El precio predeterminado (reserva)

Para la integración del canal de ventas de Amazon, en función de las [reglas de listado](./listing-rules.md), puede asignar productos de varios sitios web a un único [!DNL Amazon Marketplace] país (definido durante la [integración del almacén](./store-integration.md)). Sin embargo, esta asignación introduce el problema de qué precio debe publicarse si el producto existe en varios sitios web con precios diferentes.
