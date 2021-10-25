---
title: Vista de tiendas de Amazon
description: Vaya a la vista Amazon Stores para revisar rápidamente las estadísticas básicas de cada una de las tiendas de Amazon y acceder a las opciones de administración.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Vista Amazon Stores

Al ver la página de inicio del canal de ventas de Amazon, la variable _Amazon Stores_ vista se abre de forma predeterminada.

![Vista Amazon Stores](assets/amazon-sales-channel-home-tabs.png)

La variable _[!UICONTROL Amazon Stores]_la vista muestra una &quot;tarjeta de tienda&quot; para cada una de las tiendas de Amazon, así como algunas opciones básicas de administración y estadística. La información de resumen mostrada en cada tarjeta incluye cada estado de tienda, fecha de creación, fecha de última actualización, anuncios que necesitan atención (ejemplo: Listas incompletas) y el [!DNL Commerce] sitio web.

Al ver la variable _[!UICONTROL Amazon Store]_vista, cada tarjeta de tienda le permite:

- Para abrir una tienda [tablero](./amazon-store-dashboard.md), haga clic en **[!UICONTROL View Store]**.

- Para cambiar el estado de una tienda o eliminarla, haga clic en **[!UICONTROL Action]** y elija:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Elija cambiar el estado de la tienda a `Active` o `Inactive`, respectivamente.

      Cambio de un `Inactive` almacenar en `Active` activa los anuncios y la actividad de pedidos de la tienda, utilizando la configuración de la tienda actual (como la configuración de los anuncios, las reglas de precios y las anulaciones).

      Cambio del estado de una tienda desde `Active` a `Inactive` status suspende los anuncios y la actividad de pedidos de la tienda. Una tienda inactiva conserva todos los valores de configuración y listados de la tienda, pero detiene temporalmente la sincronización de la administración de precios, cantidades y pedidos hasta que la tienda vuelva a cambiar a `Active` estado. Esta función le permite controlar la actividad de su tienda a nivel regional sin necesidad de volver a crear o reintegrar su tienda de Amazon ni la pérdida de datos históricos de pedidos y ventas.

   - **[!UICONTROL Delete]** - Elige eliminar un almacén que ya no sea necesario.

      Elija cuándo desea eliminar una tienda de Amazon existente y su configuración de integración con su [!DNL Amazon Seller Central] cuenta. Al eliminar la cuenta, se elimina la tienda del canal de ventas de Amazon, junto con toda la configuración de la cuenta, los anuncios, los registros y otra información relacionada con esta tienda. El almacén no se puede recuperar después de la eliminación; se debe crear un almacén nuevo.

>[!NOTE]
>Para cambiar el sitio web asignado a la tienda durante la integración, debe eliminar la tienda y volver a agregarla con el diferente sitio web definido durante la integración de la tienda.

| Tarjeta de almacenamiento | Descripción |
|--- |--- |
| Sección superior | Incluye: <br>El icono de región de la tienda, definido durante [integración de tiendas](./store-integration.md).<br> El _[!UICONTROL Magento Website]_, definida durante la integración del almacén.<br>La variable_[!UICONTROL Status]_ de su tienda. Opciones: **[!UICONTROL Active]** : la integración de la tienda se completa y verifica con Amazon y está disponible para la actividad de ventas. **[!UICONTROL Inactive]** : la integración de la tienda ha finalizado, pero no está en uso ni disponible para la actividad de ventas. When `Inactive`, las ventas de Amazon se pausan. When `Active`, los ingresos de ventas y la configuración adicional se guardan para actualizarse antes de activarse.<br>La variable *[!UICONTROL Last Updated]* fecha del cambio más reciente en la configuración de la tienda de Amazon.<br>La variable *[!UICONTROL Created]* fecha en la que se creó la tienda de Amazon en el canal de ventas de Amazon. |
| Sección central | Incluye un gráfico de resumen de las actividades de la tienda de los últimos 30 días e incluye y alerta para cualquier anuncio que necesite atención. |
| Sección inferior | Incluye las opciones Ver almacén y Acción.<br>Para abrir la tienda [tablero](./amazon-store-dashboard.md), haga clic en **[!UICONTROL View Store]**.<br>Para activar, desactivar o eliminar una tienda, haga clic en **[!UICONTROL Actions]**. |
