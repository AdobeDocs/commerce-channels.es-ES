---
title: Instalación de la extensión
description: Para integrar su [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] y vender a través de la [!DNL Amazon Marketplace], descargue e instale la extensión de Sales Channel de Amazon.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Instalación de la extensión

>[!IMPORTANT]
>
>Solo se admiten las versiones de [!DNL Amazon Sales Channel] extensión 4.0+ para Adobe Commerce y Magento Open Source 2.4.x. Si está ejecutando una versión 2.3.x, consulte la documentación de la [versión compatible del canal de ventas de Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Para obtener más información sobre la compatibilidad de versiones, consulte la página [Availability](https://devdocs.magento.com/release/availability.html){target=&quot;_blank&quot;} en la documentación para desarrolladores.

La extensión [!UICONTROL Amazon Sales Channel] instala y agrega características para integrar su catálogo de comercio con [!DNL Amazon Seller Accounts] para venderlo a través de [!DNL Amazon Marketplace]. Para revisar información adicional, consulte la página [Sales Channel de Amazon](https://marketplace.magento.com/magento-module-amazon.html) en [!DNL Commerce Marketplace] y las [notas de la versión](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) en la documentación para desarrolladores.

## Requisitos

- **Instancia** de comercio: La  [!DNL Amazon Sales Channel] extensión se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x o posteriores de la infraestructura de la nube. Ya no es compatible con las versiones 2.1, 2.2 o 1.x.
- **Cuenta** web de comercio: Debe tener una cuenta web de comercio que se utilice para crear y rastrear una clave de API.
- **Clave** de API: Cree una clave de API de canal de ventas de Amazon a través de su cuenta web de comercio. Las siguientes instrucciones incluyen estos pasos.

## Instalar

Para obtener información más detallada sobre el uso de Composer para este proceso, consulte las instrucciones de [instalación de extensión](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} en la documentación para desarrolladores.

1. Inicie sesión en el [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Haga clic en la pestaña **[!UICONTROL Marketplace]** y, a continuación, haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión .

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Utilice el nombre y la información de versión para actualizar la entrada del conector de servicios en su archivo `composer.json`.

   - Añada el nombre y la versión de la extensión al archivo `composer.json` .

   - Vaya al directorio del proyecto [!DNL Commerce] y actualice el archivo `composer.json`.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Introduzca sus [claves de autenticación](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Su clave pública es su nombre de usuario; la clave privada es su contraseña.

   - Espere a que el Compositor termine de actualizar las dependencias del proyecto y asegúrese de que no haya errores.


1. [Compruebe la extensión](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Añadir la clave de API del canal de ventas de Amazon

Después de la instalación, introduzca una [clave de API](./amazon-verify-api-key.md) para completar la configuración.

## Definir las opciones de configuración del canal de Amazon

Tiene las siguientes opciones para configurar el canal de ventas de Amazon. No es necesario modificar esta configuración para empezar a incorporar y vender en Amazon. Se recomienda que los administradores avanzados consideren estas opciones.

1. Inicie sesión en el administrador.

1. En la barra lateral _Admin_, vaya a **Stores** > _Settings_ > **Configuration**.

1. Haga clic en **Sales Channel** y luego en **Configuración global**.

1. Para **Borrar historial de registro**, defina el intervalo para borrar los registros recopilados.

   Las opciones son `Once Daily`, `Once Weekly` y `Once Monthly` (predeterminado).

1. (Opcional) Para **Tareas en segundo plano (CRON) Origen**, cambie la configuración a `Command Line (CLI) CRON`.

   Se recomienda esta configuración para **_usuarios/administradores avanzados_**.

1. Haga clic en **[!UICONTROL Save Config]**.

## Actualizar la extensión

1. Inicie sesión en el [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Haga clic en la pestaña **[!UICONTROL Marketplace]** y, a continuación, haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión .

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Complete las [instrucciones de actualización de la extensión](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} en la documentación del desarrollador.
