---
title: Instalación de la extensión
description: Para integrar su [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] y venda a través de la variable [!DNL Amazon Marketplace], descargue e instale la extensión de Sales Channel de Amazon.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Instalación de la extensión

>[!IMPORTANT]
>
>Solo [!DNL Amazon Sales Channel] las versiones de la extensión 4.0 y posteriores son compatibles con las versiones de Adobe Commerce y Magento Open Source 2.4.x. Si está ejecutando una versión 2.3.x, consulte la documentación de [versión compatible del canal de ventas de Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Para obtener más información sobre la compatibilidad de versiones, consulte la [Disponibilidad](https://devdocs.magento.com/release/availability.html)página {target=&quot;_blank&quot;} en la documentación del desarrollador.

La variable [!UICONTROL Amazon Sales Channel] instala y agrega funciones para integrar su catálogo de comercio con [!DNL Amazon Seller Accounts] para vender a través de la variable [!DNL Amazon Marketplace]. Para revisar información adicional, consulte la [Sales Channel de Amazon](https://marketplace.magento.com/magento-module-amazon.html) en [!DNL Commerce Marketplace] y [notas de la versión](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) en la documentación para desarrolladores.

## Requisitos

- **Instancia de comercio**: La variable [!DNL Amazon Sales Channel] se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x o posteriores de la infraestructura de nube. Ya no es compatible con las versiones 2.1, 2.2 o 1.x.
- **Cuenta web de comercio**: Debe tener una cuenta web de comercio que se utilice para crear y rastrear una clave de API.
- **Clave de API**: Cree una clave de API de canal de ventas de Amazon a través de su cuenta web de comercio. Las siguientes instrucciones incluyen estos pasos.

## Instalar

Para obtener información más detallada sobre el uso de Composer para este proceso, consulte la [instalación de extensión](https://devdocs.magento.com/extensions/install/)Instrucciones de {target=&quot;_blank&quot;} en la documentación para desarrolladores.

1. Inicie sesión en la [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Haga clic en el **[!UICONTROL Marketplace]** y, a continuación, haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión .

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Utilice el nombre y la información de versión para actualizar la entrada del conector de servicios en su `composer.json` archivo.

   - Añada el nombre y la versión de la extensión a su `composer.json` archivo.

   - Vaya a la [!DNL Commerce] directorio de proyectos y actualice su `composer.json` archivo.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Escriba la [claves de autenticación](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Su clave pública es su nombre de usuario; la clave privada es su contraseña.

   - Espere a que el Compositor termine de actualizar las dependencias del proyecto y asegúrese de que no haya errores.


1. [Verificar la extensión](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Añadir la clave de API del canal de ventas de Amazon

Después de la instalación, introduzca un [Clave de API](./amazon-verify-api-key.md) para completar la configuración.

## Definir las opciones de configuración del canal de Amazon

Tiene las siguientes opciones para configurar el canal de ventas de Amazon. No es necesario modificar esta configuración para empezar a incorporar y vender en Amazon. Se recomienda que los administradores avanzados consideren estas opciones.

1. Inicie sesión en el administrador.

1. En el _Administrador_ barra lateral, vaya a **Almacenes** > _Configuración_ > **Configuración**.

1. Haga clic en **Sales Channel**, luego **Configuración global**.

1. Para **Borrar historial de registros**, defina el intervalo para borrar los registros recopilados.

   Las opciones incluyen `Once Daily`, `Once Weekly`y `Once Monthly` (predeterminado).

1. (Opcional) Para **Origen de tareas en segundo plano (CRON)**, cambie la configuración a `Command Line (CLI) CRON`.

   Esta configuración es recomendada para **_usuarios/administradores avanzados_**.

1. Haga clic en **[!UICONTROL Save Config]**.

## Actualizar la extensión

1. Inicie sesión en la [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Haga clic en el **[!UICONTROL Marketplace]** y, a continuación, haga clic en **[!UICONTROL My Purchases]**.

1. Busque y seleccione **[!UICONTROL Amazon Sales Channel]**.

1. En la página de extensión, seleccione la versión .

1. Para el nombre y la versión del componente, haga clic en **[!UICONTROL Technical Details]**.

1. Complete el [instrucciones de actualización de la extensión](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} en la documentación del desarrollador.
