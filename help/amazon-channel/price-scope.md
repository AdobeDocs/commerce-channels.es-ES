---
title: Precios y alcance
description: Utilice el ámbito de precios de Commerce para administrar los precios de acuerdo con varios sitios web o a nivel global.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Precios y alcance

[!DNL Commerce] proporciona la configuración de su [ámbito de precios](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} en la guía del usuario principal de Commerce.

Si cambia el ámbito del precio de catálogo de `Global` hasta `Website`, todos los atributos de tipo de precio también cambian a `Website`. Consulte [Adición de sitios web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

Cuando se elige un precio de sitio web, hay dos fuentes de precios:

- El precio del sitio web
- El precio predeterminado (alternativa)

Para la integración con el canal de ventas de Amazon, en función de sus [enumerar reglas](./listing-rules.md), puede asignar productos de varios sitios web en uno solo [!DNL Amazon Marketplace] País (definido durante [integración de tienda](./store-integration.md)). Sin embargo, esta asignación introduce el problema de qué precio debe publicarse si el producto existe en varios sitios web con precios diferentes.
