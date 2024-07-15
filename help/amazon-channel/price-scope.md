---
title: 'Canal de ventas de Amazon: ámbito del precio'
description: Utilice el ámbito de precios de Commerce para administrar los precios según varios sitios web o a nivel global.
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Alcance del precio

[!DNL Commerce] proporciona la configuración para que el [ámbito de precios](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) se establezca en `Global` o `Website`. Si el precio se establece en `Global`, existe una única fuente de precios para todos los sitios web. Si el precio se establece en `Website`, los sitios web pueden variar sus precios y también tener un valor de precios predeterminado alternativo (consulte [Alcance del precio](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Si cambia el ámbito del precio de catálogo de `Global` a `Website`, todos los atributos del tipo de precio también cambiarán a `Website`. Consulte [Agregar sitios web](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Cuando se elige un precio de sitio web, hay dos fuentes de precios:

- El precio del sitio web
- El precio predeterminado (alternativa)

Para la integración del canal de ventas de Amazon, en función de las [reglas de listado](./listing-rules.md), puede asignar productos de varios sitios web a un único país de [!DNL Amazon Marketplace] (definido durante [integración de tienda](./store-integration.md)). Sin embargo, esta asignación introduce el problema de qué precio debe publicarse si el producto existe en varios sitios web con precios diferentes.
