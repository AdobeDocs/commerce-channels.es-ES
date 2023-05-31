---
title: 'Canal de ventas de Amazon: ámbito del precio'
description: Utilice el ámbito de precios de Commerce para administrar los precios de acuerdo con varios sitios web o a nivel global.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Alcance del precio

[!DNL Commerce] proporciona la configuración de su [ámbito de precios](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) que se establecerá en `Global` o `Website`. Si el precio se establece en `Global`Sin embargo, hay una única fuente de precios para todos los sitios web. Si el precio se establece en `Website`, los sitios web pueden variar sus precios y también tienen un valor de precios predeterminado alternativo (consulte [Alcance del precio](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Si cambia el ámbito del precio de catálogo de `Global` hasta `Website`, todos los atributos de tipo de precio también cambian a `Website`. Consulte [Adición de sitios web](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Cuando se elige un precio de sitio web, hay dos fuentes de precios:

- El precio del sitio web
- El precio predeterminado (alternativa)

Para la integración con el canal de ventas de Amazon, en función de sus [enumerar reglas](./listing-rules.md), puede asignar productos de varios sitios web en uno solo [!DNL Amazon Marketplace] País (definido durante [integración de tienda](./store-integration.md)). Sin embargo, esta asignación introduce el problema de qué precio debe publicarse si el producto existe en varios sitios web con precios diferentes.
