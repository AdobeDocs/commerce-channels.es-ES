---
title: 'Connect [!DNL Channel Manager] a [!DNL Walmart Marketplace]'
description: '"Conecte una vista de Commerce store a [!DNL Walmart Marketplace] para crear el canal de ventas para administrar las listas de productos, el inventario, el precio y los pedidos de ventas de Walmart Marketplace".'
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 3f6039ad78ff500c31129bee12d65e291e226567
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Connect [!DNL Channel Manager] a [!DNL Walmart Marketplace]

Después de instalar el Administrador de canales en su [!DNL Commerce] , cree un canal de ventas en el Administrador de canales y configure las credenciales para conectarse [!DNL Channel Manager] a [!DNL Walmart Marketplace].

1. [Crear el canal de ventas](#create-the-sales-channel) seleccionando [!DNL Commerce] almacenar para listas de productos.

1. [Conecte el canal a [!DNL Walmart Marketplace] añadiendo [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Configuración completa del canal de ventas](#complete-sales-channel-store-setup) para administrar anuncios, inventario, precios y pedidos para su [!DNL Walmart Marketplace] gama de productos.

>[!NOTE]
>
>Channel Manager requiere una conexión uno a uno entre una cuenta de Walmart y una [!DNL Commerce] vista de tienda. No se puede conectar la misma vista de tienda a varias cuentas de Walmart.

## Crear el canal de ventas

1. En el Administrador, abra [!DNL Channel Manager] seleccionando **[!UICONTROL Marketing** > _Canales _> **Administrador de canales]**.

1. En el **[!UICONTROL Marketplaces available to connect]** , seleccione **[!UICONTROL Get Started]**.

   ![Conectar nuevo [!DNL Walmart] almacenar en [!DNL Channel Manager]](assets/channel-manager-home.png)

1. Si es necesario, configure su [!DNL Walmart Marketplace Seller] cuenta.

1. Configure el almacén y la conexión:

   - Select **[!UICONTROL Add Credentials]**.

   - Seleccione el [!DNL Commerce] vista de tienda que ofrece los productos que desea vender en el mercado.

      ![Configurar la conexión entre [!DNL Commerce] y [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - Escriba un **[!UICONTROL store name]**.

   - Seleccione el **[!UICONTROL Adobe [!DNL Commerce] site]** para listas de productos y procesamiento de pedidos.

   - Para recibir notificaciones relacionadas con [!DNL Channel Manager], agregue un **[!UICONTROL email address]**.

1. Conecte el canal a [!DNL Walmart Marketplace].

   - Agregue las credenciales para la [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de su [!DNL Walmart Marketplace Seller] cuenta.

   - Si no dispone de las credenciales, consígalas desde el [!DNL Walmart Marketplace Developer Portal] seleccionando **[!UICONTROL Get API credentials]**.

      En Developer Portal, seleccione su región (EE. UU. y Canadá) y, a continuación, inicie sesión.

      ![[!DNL Walmart Marketplace] inicio de sesión en la cuenta](assets/walmart-marketplace-login-page.png)

   - En el formulario de clave de API, copie y guarde el **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]** los valores de la variable [!UICONTROL Adobe Inc Production API key] a una ubicación segura.

      ![[!DNL Walmart Marketplace API key] página de configuración](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Si la variable [!DNL Adobe Inc] La clave no aparece en Developer Portal, seleccione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permisos y generar la clave. Para obtener más información sobre la configuración, consulte [Genere un [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Volver a [!DNL Channel Manager] para agregar las credenciales al **[!UICONTROL Walmart Connection]** información.

      Cuando agrega credenciales, Adobe oculta el secreto del cliente y almacena el valor en un almacén seguro.

1. Select **[!UICONTROL Save Store]** para aplicar la configuración y conectarse al [!DNL Walmart marketplace].

1. Después de conectarse correctamente, [configuración completa de la tienda](complete-sales-channel-store-setup.md) de la variable **[!UICONTROL Channel Manager]** almacenar página.

![Configuración de la primera tienda](assets/channel-manager-setup-first-store.png)

### Solución de problemas de conexión

Si la conexión a [!DNL Walmart] falla, consulte [Preguntas frecuentes sobre Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} para obtener sugerencias para la resolución de problemas.

- En el [!DNL Walmart Developer Portal], compruebe que ha copiado las credenciales correctas para la clave de API de producción para [!UICONTROL Adobe Inc.]

- Compruebe que la configuración de acceso para la variable [!UICONTROL Walmart Adobe API key] tiene los permisos correctos. Consulte [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme que la variable [!DNL Walmart API] está disponible en el [Página de estado de la API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.
