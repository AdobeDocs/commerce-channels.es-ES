---
title: Publicar manualmente anuncios de Amazon
description: Si es necesario, puede publicar manualmente los anuncios de Amazon finalizados desde el administrador de Commerce.
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publicar manualmente anuncios de Amazon

Puedes publicar manualmente uno o más anuncios de Amazon que se hayan finalizado.

1. Ver uno o más listados en la ficha _[!UICONTROL Ended]_de la página [Listados de productos](./managing-product-listings.md) (ficha_[!UICONTROL Inactive]_, _[!UICONTROL Active]_o_[!UICONTROL Ineligible]_).

1. En la columna de la izquierda, haga clic en para comprobar cada uno de los listados que desea volver a publicar.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Publish Product to Amazon]**.

1. Haga clic en **[!UICONTROL OK]** en el mensaje de confirmación.

   Se muestra un mensaje para confirmar que los anuncios seleccionados se están procesando para publicarlos en Amazon.

   La información de la lista se publica en Amazon en función de la configuración de cron. La información de la lista se envía a Amazon en la siguiente sincronización de datos. Hasta que Amazon responda con la confirmación del anuncio, los anuncios publicados manualmente permanecerán en la ficha _Listo para publicar_ con el estado `List in Progress`. Cuando se recibe la confirmación del anuncio de Amazon, los anuncios pasan a la ficha _Activo_ con el estado `Active`.
