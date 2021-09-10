---
title: Configuración de Sales Channel
description: Para administrar el registro, el origen cron y la sincronización para las funciones de canal de ventas de Amazon, actualice la configuración de comercio.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Configuración de Sales Channel

Cuando se instala la extensión [!DNL Amazon Sales Channel] , los valores predeterminados se establecen en el canal de ventas de Administración para Amazon . Estos ajustes se pueden modificar en los ajustes de configuración de la tienda de Amazon. Estos ajustes incluyen:

- Intervalos para borrar el historial del registro de actividades
- Selección de origen cron
- Opciones de sincronización de registros

## Modificación de la configuración de los canales de comercio

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales Channels]** y elija **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, elija una opción:

   - `Once Daily` - Elige borrar el historial de actividad de tu tienda una vez al día.

   - `Once Weekly` - Elige borrar el historial de actividad de tu tienda una vez a la semana.

   - `Once Monthly` - (Predeterminado) Elija borrar el historial de actividad de la tienda una vez al mes.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, elija `Magento CRON`.

   Esta opción permite que el canal de ventas de Amazon utilice la configuración [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) para determinar los intervalos de comunicación y sincronización de datos con [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, elija `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar el problema.

   El registro de canal de ventas de Amazon se escribe en el archivo `{Commerce Root}/var/log/channel_amazon.log` y se puede ver en [developer mode](https://docs.magento.com/user-guide/magento/installation-modes.html){:target=&quot;_blank&quot;}. El registro solo debe ser `Enabled` durante la resolución de problemas y debe ser `Disabled` cuando se haya completado la resolución de problemas.

1. Haga clic en **[!UICONTROL Save Config]**.

![Ajustes de configuración de Sales Channel](assets/config-sales-channel-global-settings.png)
