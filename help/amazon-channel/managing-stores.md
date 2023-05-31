---
title: "[!UICONTROL Amazon Stores] view"
description: Vaya a la vista Tiendas Amazon para revisar rápidamente las estadísticas básicas de cada una de las tiendas Amazon y acceder a las opciones de administración.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores] vista

Al ver la página de inicio del canal de ventas de Amazon, la variable _Tiendas Amazon_ La vista se abre de forma predeterminada.

![Vista de tiendas Amazon](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

El _[!UICONTROL Amazon Stores]_La vista muestra una &quot;tarjeta de tienda&quot; para cada una de las tiendas Amazon, junto con algunas estadísticas básicas y opciones de administración. La información de resumen que se muestra en cada tarjeta incluye cada estado de tienda, fecha de creación, fecha de última actualización, anuncios que requieren atención (por ejemplo: anuncios incompletos) y el asignado [!DNL Commerce] sitio web.

Al ver el _[!UICONTROL Amazon Store]_vista, cada tarjeta de tienda le permite:

- Para abrir una tienda [tablero](./amazon-store-dashboard.md), haga clic en **[!UICONTROL View Store]**.

- Para cambiar el estado de una tienda o eliminarla, haga clic en **[!UICONTROL Action]** y elija:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Elija cambiar el estado de la tienda a `Active` o `Inactive`, respectivamente.

      Cambio de un `Inactive` almacenar en `Active` El estado activa los anuncios y la actividad de pedidos de la tienda mediante la configuración actual de la tienda (por ejemplo, la configuración de anuncios, las reglas de precios y las invalidaciones).

      Cambiar el estado de una tienda de `Active` hasta `Inactive` El estado suspende los anuncios y la actividad de pedidos de la tienda. Un almacén inactivo conserva todos los ajustes y listados de almacén, pero detiene temporalmente la sincronización de precios, cantidad y gestión de pedidos hasta que el almacén se cambia de nuevo a `Active` estado. Esta función le permite controlar la actividad de su tienda a nivel regional sin necesidad de volver a crear o reintegrar su tienda Amazon ni perder los datos históricos de pedidos y ventas.

   - **[!UICONTROL Delete]** - Elige eliminar una tienda que ya no sea necesaria.

      Elija cuándo desea eliminar una tienda de Amazon existente y su configuración de integración con su [!DNL Amazon Seller Central] cuenta. Al eliminar la cuenta, se quita el almacén del canal de ventas de Amazon, junto con toda la configuración de la cuenta, los listados, los registros y demás información relacionada con el almacén. El almacén no se puede recuperar después de la eliminación, se debe crear un nuevo almacén.

>[!NOTE]
>Para cambiar el sitio web asignado a la tienda durante la integración, debe eliminar la tienda y volver a añadirla con el sitio web diferente definido durante la integración de la tienda.

| Tarjeta de tienda | Descripción |
|--- |--- |
| Sección superior | Incluye: <br>El icono de región de la tienda, definido durante [integración de tienda](./store-integration.md).<br> El asignado _[!UICONTROL Magento Website]_, definido durante la integración de la tienda.<br>El_[!UICONTROL Status]_ de su tienda. Opciones: **[!UICONTROL Active]** : la integración de la tienda se ha completado y verificado con Amazon, y está disponible para la actividad de ventas. **[!UICONTROL Inactive]** : la integración de la tienda se ha completado, pero no está en uso ni disponible para la actividad de ventas. Cuándo `Inactive`, las ventas de Amazon se pausan. Cuándo `Active`, los ingresos de ventas y la configuración adicional se guardan para actualizarse antes de activarse.<br>El *[!UICONTROL Last Updated]* fecha del cambio más reciente en la configuración de la tienda Amazon.<br>El *[!UICONTROL Created]* fecha en la que se creó la tienda Amazon en el canal de ventas de Amazon. |
| Sección central | Incluye un gráfico de resumen de la actividad de la tienda de los últimos 30 días e incluye una alerta para todos los anuncios que requieran atención. |
| Sección inferior | Incluye las opciones Ver tienda y Acción.<br>Para abrir la tienda [tablero](./amazon-store-dashboard.md), haga clic en **[!UICONTROL View Store]**.<br>Para activar, desactivar o eliminar un almacén, haga clic en **[!UICONTROL Actions]**. |
