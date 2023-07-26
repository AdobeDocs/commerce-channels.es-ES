---
title: "Instale el [!DNL Amazon Sales Channel] extension"
description: Para integrar su [!DNL Commerce] catálogo con [!DNL Amazon Seller Accounts] y vender a través de [!DNL Amazon Marketplace], descargue e instale la extensión de Sales Channel de Amazon.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Instale el [!DNL Amazon Sales Channel] extensión

>[!IMPORTANT]
>
>Solo [!DNL Amazon Sales Channel] las versiones posteriores a la extensión 4.0 son compatibles con las versiones de Adobe Commerce y Magento Open Source 2.4.x. Si está ejecutando una versión 2.3.x, consulte la documentación de [versión compatible del canal de ventas de Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Para obtener más información sobre la compatibilidad de versiones, consulte la [Disponibilidad](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) en la documentación para desarrolladores.

El [!UICONTROL Amazon Sales Channel] instala y agrega funciones para integrar su catálogo de Commerce con [!DNL Amazon Seller Accounts] para vender a través de [!DNL Amazon Marketplace]. Para obtener más información, consulte la [Sales Channel de Amazon](https://marketplace.magento.com/magento-module-amazon.html) página en [!DNL Commerce Marketplace] y el [notas de la versión](release-notes.md).

## Requisitos

- **Instancia de Commerce**: La [!DNL Amazon Sales Channel] La extensión de se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x o posteriores de la infraestructura en la nube. Ya no es compatible con las versiones 2.1, 2.2 o 1.x.
- **Cuenta web de Commerce**: Debe tener una cuenta web de Commerce, que se utiliza para crear y rastrear una clave de API.
- **Clave de API**: Cree una clave de API de canal de ventas de Amazon a través de su cuenta web de Commerce. Las siguientes instrucciones incluyen estos pasos.

## Instalar

Para obtener información más detallada sobre cómo usar Composer para este proceso, consulte la [instalación de extensiones](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) instrucciones en la documentación para desarrolladores.

1. Inicie sesión en [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Haga clic en **[!UICONTROL Marketplace]** y haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión.

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Utilice la información de nombre y versión para actualizar la entrada del conector de servicios en su `composer.json` archivo.

   - Añada el nombre y la versión de la extensión a su `composer.json` archivo.

   - Navegue hasta su [!DNL Commerce] directorio del proyecto y actualice su `composer.json` archivo.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Introduzca su [claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Su clave pública es su nombre de usuario; su clave privada es su contraseña.

   - Espere a que Composer termine de actualizar las dependencias del proyecto y asegúrese de que no haya errores.

1. [Verificar la extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Añadir la clave de API del canal de ventas de Amazon

Después de la instalación, introduzca un [Clave de API](./amazon-verify-api-key.md) para completar la configuración.

## Determinar las opciones de configuración del canal de Amazon

Dispone de las siguientes opciones para configurar el canal de ventas de Amazon. No es necesario modificar esta configuración para comenzar a incorporar y vender en Amazon. Se recomienda que los administradores avanzados tengan en cuenta estas opciones.

1. Inicie sesión en Admin.

1. En el _Administrador_ barra lateral, vaya a **Tiendas** > _Configuración_ > **Configuración**.

1. Clic **Sales Channel**, entonces **Configuración global**.

1. Para **Borrar historial de registro**, defina el intervalo para borrar los registros recopilados.

   Las opciones incluyen `Once Daily`, `Once Weekly`, y `Once Monthly` (valor predeterminado).

1. (Opcional) Para **Origen de tareas en segundo plano (CRON)**, cambie la configuración a `Command Line (CLI) CRON`.

   Se recomienda esta configuración para **_usuarios/administradores avanzados_**.

1. Clic **[!UICONTROL Save Config]**.

## Actualización de la extensión

1. Inicie sesión en [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Haga clic en **[!UICONTROL Marketplace]** y haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión.

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Complete la [instrucciones de actualización de extensiones](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) en el _Guía de instalación_.
