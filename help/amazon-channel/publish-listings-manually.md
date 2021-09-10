---
title: Publicar manualmente anuncios de Amazon
description: Cuando sea necesario, puede publicar manualmente sus anuncios de Amazon finalizados desde el administrador de comercio.
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publicar manualmente anuncios de Amazon

Puede publicar manualmente una o más listas de Amazon que hayan finalizado.

1. Vea uno o más listados en la pestaña _[!UICONTROL Ended]_de la página [Listings de productos](./managing-product-listings.md) (pestaña_[!UICONTROL Inactive]_, _[!UICONTROL Active]_o_[!UICONTROL Ineligible]_).

1. En la columna izquierda, haga clic en para comprobar cada uno de los anuncios que desea volver a publicar.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Publish Product to Amazon]**.

1. Haga clic en **[!UICONTROL OK]** en el mensaje de confirmación.

   Se muestra un mensaje para confirmar que los anuncios seleccionados se están procesando para publicarse en Amazon.

   La información de la lista se publica en Amazon en función de la configuración de cron. La información de la lista se envía a Amazon en la siguiente sincronización de datos. Hasta que Amazon responda con la confirmación de la lista, las listas publicadas manualmente permanecen en la pestaña _Ready to List_ con el estado `List in Progress`. Cuando se recibe la confirmación de la lista de Amazon, las listas se mueven a la pestaña _Activo_ con el estado `Active`.
