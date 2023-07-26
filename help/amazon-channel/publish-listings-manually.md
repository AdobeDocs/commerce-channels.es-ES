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

1. Consulta uno o más anuncios de la _[!UICONTROL Ended]_de la pestaña [Listados de productos](./managing-product-listings.md) página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_, o_[!UICONTROL Ineligible]_ pestaña).

1. En la columna de la izquierda, haga clic en para comprobar cada uno de los listados que desea volver a publicar.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Publish Product to Amazon]**.

1. Clic **[!UICONTROL OK]** en el mensaje de confirmación.

   Se muestra un mensaje para confirmar que los anuncios seleccionados se están procesando para publicarlos en Amazon.

   La información de la lista se publica en Amazon en función de la configuración de cron. La información de la lista se envía a Amazon en la siguiente sincronización de datos. Hasta que Amazon responda con la confirmación del anuncio, los anuncios publicados manualmente permanecerán en la _Listo para la lista_ pestaña con un `List in Progress` estado. Cuando se recibe la confirmación de anuncio de Amazon, los anuncios pasan al _Activo_ pestaña con un `Active` estado.
