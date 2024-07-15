---
title: Configuración del canal de ventas
description: Para administrar el registro, el origen cron y la sincronización de las funciones del canal de ventas de Amazon, actualice la configuración de Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Configuración del canal de ventas

Cuando se instala la extensión [!DNL Amazon Sales Channel], los valores predeterminados se establecen en el canal de ventas Administrador para Amazon. Estos ajustes se pueden modificar en los ajustes de configuración de la tienda de Amazon. Esta configuración incluye:

- Intervalos para borrar el historial del registro de actividades
- Selección de origen de Cron
- Opciones de sincronización de registros

## Modificar la configuración de canales de Commerce

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales Channels]** y elija **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, elija una opción:

   - `Once Daily`: elige borrar el historial de actividades de la tienda una vez al día.

   - `Once Weekly`: elige borrar el historial de actividades de la tienda una vez por semana.

   - `Once Monthly` - (Predeterminado) Elige borrar el historial de actividad de la tienda una vez al mes.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, elija `Magento CRON`.

   Esta opción permite que el canal de ventas de Amazon use la configuración de [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) para determinar la comunicación y los intervalos de sincronización de datos con [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, elija `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas.

   El registro del canal de ventas de Amazon se ha escrito en el archivo `{Commerce Root}/var/log/channel_amazon.log` y se puede ver en [modo de desarrollador](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). El registro solo debe ser `Enabled` durante la solución de problemas y debe ser `Disabled` cuando se complete la solución de problemas.

1. Para **[!UICONTROL Read-Only Mode]**, seleccione `Enabled` para bloquear todas las solicitudes de API salientes que cambien de estado.

   Con esta configuración, los cambios potenciales se guardan, pero no se envían, hasta que se deshabilite [!UICONTROL Read-Only Mode]. La caché de configuración debe borrarse para que se active el modo de solo lectura. Para volver a iniciar las transferencias de datos, seleccione `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] está diseñado para copias de la instancia de producción, como ensayo o control de calidad, y no debe usarse en la instancia de producción.
   >
   >Cuando se migra una base de datos a una nueva copia de la instancia (detectada cuando la dirección URL de un almacén cambia en la configuración), [!UICONTROL Read-Only Mode] se habilita automáticamente.

1. Haga clic en **[!UICONTROL Save Config]**.

![Configuración de Sales Channel](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
