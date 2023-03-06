---
title: Configuración de Sales Channel
description: Para administrar el registro, el origen cron y la sincronización de las funciones del canal de ventas de Amazon, actualice la configuración de Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Configuración de Sales Channel

Si la variable [!DNL Amazon Sales Channel] Una vez instalada la extensión de, los valores predeterminados se establecen en Admin para el canal de ventas de Amazon. Estos ajustes se pueden modificar en los ajustes de configuración de la tienda de Amazon. Esta configuración incluye:

- Intervalos para borrar el historial del registro de actividades
- Selección de origen de Cron
- Opciones de sincronización de registros

## Modifique la configuración de los canales de comercio

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales Channels]** y elija **[!UICONTROL Global Settings]**.

1. Para **[!UICONTROL Clear Log History]**, elija una opción:

   - `Once Daily` - Elige borrar el historial de actividad de tu tienda una vez al día.

   - `Once Weekly` - Elige borrar el historial de actividad de la tienda una vez por semana.

   - `Once Monthly` - (Predeterminado) Elige borrar el historial de actividad de la tienda una vez al mes.

1. Para **[!UICONTROL Background Tasks (CRON) Source]**, elija `Magento CRON`.

   Esta opción permite que el canal de ventas de Amazon utilice su [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) configuración para determinar los intervalos de comunicación y sincronización de datos con [!DNL Amazon Seller Central].

1. Para **[!UICONTROL Enable Debug Logging]**, elija `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas.

   El registro de canal de ventas de Amazon se escribe en `{Commerce Root}/var/log/channel_amazon.log` y se pueden ver en [modo de desarrollador](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}. El registro solo debe ser `Enabled` durante la localización de averías y debe `Disabled` cuando se complete la localización de averías.

1. Para **[!UICONTROL Read-Only Mode]**, seleccione `Enabled` para bloquear todas las solicitudes de API salientes de cambio de estado.

   Con esta configuración, los cambios potenciales se guardan, pero no se envían, hasta que [!UICONTROL Read-Only Mode] está deshabilitada. La caché de configuración debe borrarse para que se active el modo de solo lectura. Para volver a iniciar las transferencias de datos, seleccione `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] está diseñado para copias de la instancia de producción, como ensayo o control de calidad, y no debe utilizarse en la instancia de producción.
   >
   >Cuando se migra una base de datos a una nueva copia de la instancia (se detecta cuando cambia la dirección URL de un almacén en la configuración), [!UICONTROL Read-Only Mode] se activa automáticamente.

1. Clic **[!UICONTROL Save Config]**.

![Ajustes de configuración de Sales Channel](assets/config-sales-channel-global-settings.png)
