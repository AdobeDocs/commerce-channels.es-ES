---
title: Instalar la extensión  [!DNL Amazon Sales Channel]
description: Para integrar tu  [!DNL Commerce] catálogo con [!DNL Amazon Seller Accounts] y vender a través de [!DNL Amazon Marketplace], descarga e instala la extensión de Sales Channel de Amazon.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Instalar la extensión [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
>Solo se admiten las versiones de la extensión [!DNL Amazon Sales Channel] 4.0+ para las versiones de Adobe Commerce y Magento Open Source 2.4.x. Si está ejecutando una versión 2.3.x, consulte la documentación de la [versión compatible del canal de ventas de Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Para obtener más información sobre la compatibilidad de versiones, consulte la página [Disponibilidad](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) en la documentación para desarrolladores.

La extensión [!UICONTROL Amazon Sales Channel] instala y agrega características para integrar su catálogo de Commerce con [!DNL Amazon Seller Accounts] para venderlo a través de [!DNL Amazon Marketplace]. Para revisar información adicional, consulte la página [Sales Channel de Amazon](https://marketplace.magento.com/magento-module-amazon.html) en [!DNL Commerce Marketplace] y las [notas de la versión](release-notes.md).

## Requisitos

- **Commerce instance**: La extensión [!DNL Amazon Sales Channel] se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x o posteriores de la infraestructura en la nube. Ya no es compatible con las versiones 2.1, 2.2 o 1.x.
- **cuenta web de Commerce**: debe tener una cuenta web de Commerce que se use para crear y realizar el seguimiento de una clave de API.
- **clave API**: crea una clave API de canal de ventas de Amazon a través de tu cuenta web de Commerce. Las siguientes instrucciones incluyen estos pasos.

## Instalar

Para obtener información más detallada sobre cómo usar Composer para este proceso, consulte las instrucciones de [instalación de extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) en la documentación para desarrolladores.

1. Inicie sesión en [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Haga clic en la ficha **[!UICONTROL Marketplace]** y, a continuación, en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión.

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Use el nombre y la información de versión para actualizar la entrada del conector de servicios en el archivo `composer.json`.

   - Agregue el nombre y la versión de la extensión al archivo `composer.json`.

   - Vaya al directorio del proyecto [!DNL Commerce] y actualice el archivo `composer.json`.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Escriba sus [claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Su clave pública es su nombre de usuario; su clave privada es su contraseña.

   - Espere a que Composer termine de actualizar las dependencias del proyecto y asegúrese de que no haya errores.

1. [Compruebe la extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Añadir la clave de API del canal de ventas de Amazon

Después de la instalación, escribe una [clave de API](./amazon-verify-api-key.md) para completar la configuración.

## Determinar las opciones de configuración del canal de Amazon

Dispone de las siguientes opciones para configurar el canal de ventas de Amazon. No es necesario modificar esta configuración para comenzar a incorporar y vender en Amazon. Se recomienda que los administradores avanzados tengan en cuenta estas opciones.

1. Inicie sesión en Admin.

1. En la barra lateral de _Admin_, ve a **Tiendas** > _Configuración_ > **Configuración**.

1. Haga clic en **Sales Channel** y luego en **Configuración global**.

1. Para **Borrar historial de registros**, defina el intervalo para borrar los registros recopilados.

   Las opciones incluyen `Once Daily`, `Once Weekly` y `Once Monthly` (predeterminado).

1. (Opcional) Para **Tareas en segundo plano (CRON) Source**, cambie el valor a `Command Line (CLI) CRON`.

   Se recomienda esta configuración para **_usuarios/administradores avanzados_**.

1. Haga clic en **[!UICONTROL Save Config]**.

## Actualización de la extensión

1. Inicie sesión en [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Haga clic en la ficha **[!UICONTROL Marketplace]** y, a continuación, en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión.

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Complete las [instrucciones de actualización de la extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) en la _Guía de instalación_.
