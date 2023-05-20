---
title: 'Conectar [!DNL Channel Manager] hasta [!DNL Walmart Marketplace]'
description: "Conectar una vista de la tienda de Commerce a [!DNL Walmart Marketplace] crear el canal de ventas para administrar las listas de productos de Commerce, el inventario, el precio y los pedidos de ventas de Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Connect [!DNL Channel Manager] hasta [!DNL Walmart Marketplace]

Después de instalar el Administrador de canales en su [!DNL Commerce] Por ejemplo, cree un canal de ventas en el Administrador de canales y configure las credenciales para conectarse [!DNL Channel Manager] hasta [!DNL Walmart Marketplace].

1. [Creación del canal de ventas](#create-the-sales-channel) seleccionando la opción [!DNL Commerce] almacenar para listados de productos.

1. [Conecte el canal a [!DNL Walmart Marketplace] añadiendo [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Configuración completa del canal de ventas](#complete-sales-channel-store-setup) para administrar listados, inventario, precios y pedidos de su [!DNL Walmart Marketplace] surtido de productos.

>[!NOTE]
>
>Channel Manager requiere una conexión uno a uno entre una cuenta de Walmart y una [!DNL Commerce] vista de la tienda. No puede conectar la misma vista de tienda a varias cuentas de Walmart.

## Creación del canal de ventas

1. En Admin, abra. [!DNL Channel Manager] seleccionando **[!UICONTROL Marketing** > _Canales _> **Administrador de canales]**.

1. En el **[!UICONTROL Marketplaces available to connect]** , seleccione **[!UICONTROL Get Started]**.

   ![Conectar nuevo [!DNL Walmart] almacenar en [!DNL Channel Manager]](assets/channel-manager-home.png)

1. Si es necesario, configure su [!DNL Walmart Marketplace Seller] cuenta.

1. Configure la tienda y la conexión:

   - Seleccionar **[!UICONTROL Add Credentials]**.

   - Seleccione el [!DNL Commerce] vista de tienda que ofrece los productos que desea vender en el mercado.

      ![Configurar conexión entre [!DNL Commerce] y [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - Introduzca un único **[!UICONTROL store name]**.

   - Seleccione el **[!UICONTROL Adobe [!DNL Commerce] site]** para listados de productos y procesamiento de pedidos.

   - Para recibir notificaciones relacionadas con [!DNL Channel Manager], añada un **[!UICONTROL email address]**.

1. Conecte el canal a [!DNL Walmart Marketplace].

   - Añada las credenciales de para la [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de su [!DNL Walmart Marketplace Seller] cuenta.

   - Si no tiene las credenciales, consígalas en el [!DNL Walmart Marketplace Developer Portal] seleccionando **[!UICONTROL Get API credentials]**.

      En el portal para desarrolladores, seleccione su región (EE. UU. y Canadá) y, a continuación, inicie sesión.

      ![[!DNL Walmart Marketplace] inicio de sesión de cuenta](assets/walmart-marketplace-login-page.png)

   - En el formulario de clave de API, copie y guarde la variable **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]** valores para [!UICONTROL Adobe Inc Production API key] a una ubicación segura.

      ![[!DNL Walmart Marketplace API key] página de configuración](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Si la variable [!DNL Adobe Inc] La clave no aparece en el portal del desarrollador, seleccione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permisos y generar la clave. Para obtener más información, consulte [Generación de un [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Volver a [!DNL Channel Manager] para agregar las credenciales a **[!UICONTROL Walmart Connection]** información.

      Cuando se agregan credenciales, la Adobe oculta el secreto de cliente y almacena el valor en un almacén seguro.

1. Seleccionar **[!UICONTROL Save Store]** para aplicar la configuración de y conectarse a [!DNL Walmart marketplace].

1. Después de conectarse correctamente, [configuración completa de la tienda](complete-sales-channel-store-setup.md) desde el **[!UICONTROL Channel Manager]** página de la tienda.

![Configurar la primera tienda](assets/channel-manager-setup-first-store.png)

### Solucionar problemas de conexión

Si la conexión a [!DNL Walmart] falla, consulte la [Preguntas frecuentes sobre Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} para obtener sugerencias de solución de problemas.

- Desde el [!DNL Walmart Developer Portal], compruebe que ha copiado las credenciales correctas para la clave de API de producción para [!UICONTROL Adobe Inc.]

- Compruebe que la configuración de acceso del [!UICONTROL Walmart Adobe API key] tiene los permisos correctos. Consulte [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme que la variable [!DNL Walmart API] El servicio está disponible en [Página de estado de API de Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
