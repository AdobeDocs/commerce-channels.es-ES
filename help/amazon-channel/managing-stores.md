---
title: "[!UICONTROL Amazon Stores] vista"
description: Vaya a la vista Tiendas Amazon para revisar rápidamente las estadísticas básicas de cada una de las tiendas Amazon y acceder a las opciones de administración.
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Vista de [!UICONTROL Amazon Stores]

Al ver la página de inicio del canal de ventas de Amazon, la vista _Amazon Stores_ se abre de manera predeterminada.

![Vista de tiendas Amazon](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

La vista _[!UICONTROL Amazon Stores]_muestra una &quot;tarjeta de almacenamiento&quot; para cada una de las tiendas Amazon, además de algunas estadísticas básicas y opciones de administración. La información de resumen que se muestra en cada tarjeta incluye cada estado de tienda, fecha de creación, fecha de última actualización, anuncios que requieren atención (por ejemplo: Anuncios incompletos) y el sitio web [!DNL Commerce] asignado.

Al ver la vista _[!UICONTROL Amazon Store]_, cada tarjeta de tienda le permite:

- Para abrir un [panel](./amazon-store-dashboard.md) de almacén, haga clic en **[!UICONTROL View Store]**.

- Para cambiar el estado de un almacén o eliminar un almacén, haga clic en **[!UICONTROL Action]** y elija:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Elija cambiar el estado del almacén a `Active` o `Inactive`, respectivamente.

     Si se cambia el estado de una tienda `Inactive` a `Active`, se activan los anuncios y la actividad de pedidos de la tienda mediante la configuración actual de la tienda (por ejemplo, la configuración de los anuncios, las reglas de precios y las invalidaciones).

     Al cambiar el estado de un almacén de `Active` a `Inactive`, se suspenden los listados y la actividad de pedidos del almacén. Un almacén inactivo conserva todos los valores y listados de almacén, pero detiene temporalmente la sincronización de precios, cantidad y administración de pedidos hasta que el almacén vuelva a cambiar a estado `Active`. Esta función le permite controlar la actividad de su tienda a nivel regional sin necesidad de volver a crear o reintegrar su tienda Amazon ni perder los datos históricos de pedidos y ventas.

   - **[!UICONTROL Delete]**: elija eliminar un almacén que ya no sea necesario.

     Elija cuándo desea eliminar una tienda Amazon existente y su configuración de integración con su cuenta de [!DNL Amazon Seller Central]. Al eliminar la cuenta, se quita el almacén del canal de ventas de Amazon, junto con toda la configuración de la cuenta, los listados, los registros y demás información relacionada con el almacén. El almacén no se puede recuperar después de la eliminación, se debe crear un nuevo almacén.

>[!NOTE]
>Para cambiar el sitio web asignado a la tienda durante la integración, debe eliminar la tienda y volver a añadirla con el sitio web diferente definido durante la integración de la tienda.

| Tarjeta de tienda | Descripción |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sección superior | Incluye: <br>El icono de región de la tienda, definido durante la [integración de la tienda](./store-integration.md).<br>: el _[!UICONTROL Magento Website]_asignado, definido durante la integración del almacén.<br>El_[!UICONTROL Status]_ de su tienda. Opciones: **[!UICONTROL Active]**: la integración de la tienda se ha completado y verificado con Amazon, y está disponible para la actividad de ventas. **[!UICONTROL Inactive]**: la integración de la tienda se ha completado, pero no está en uso ni disponible para la actividad de ventas. Cuando `Inactive`, las ventas de Amazon se pausan. Cuando `Active`, los ingresos de ventas y la configuración adicional se guardan para actualizarse antes de activarse.<br>La fecha *[!UICONTROL Last Updated]* del cambio más reciente en la configuración de la tienda Amazon.<br>La fecha *[!UICONTROL Created]* en que se creó la tienda Amazon en el canal de ventas de Amazon. |
| Sección central | Incluye un gráfico de resumen de la actividad de la tienda de los últimos 30 días e incluye una alerta para todos los anuncios que requieran atención. |
| Sección inferior | Incluye las opciones Ver tienda y Acción.<br>Para abrir el [panel](./amazon-store-dashboard.md) de la tienda, haga clic en **[!UICONTROL View Store]**.<br>Para activar, desactivar o eliminar un almacén, haga clic en **[!UICONTROL Actions]**. |
