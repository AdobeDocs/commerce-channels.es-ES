---
title: 'Conectar [!DNL Channel Manager] a [!DNL Walmart Marketplace]'
description: '"Conecte una vista de tienda Commerce a  [!DNL Walmart Marketplace] para crear el canal de ventas y administrar las listas de productos, el inventario, el precio y los pedidos de ventas de Commerce para Walmart Marketplace".'
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Conectar [!DNL Channel Manager] a [!DNL Walmart Marketplace]

Después de instalar el Administrador de canales en su instancia de [!DNL Commerce], cree un canal de ventas en el Administrador de canales y configure las credenciales para conectar a [!DNL Channel Manager] con [!DNL Walmart Marketplace].

1. [Crea el canal de ventas](#create-the-sales-channel) seleccionando la tienda [!DNL Commerce] para las listas de productos.

1. [Conecta el canal a [!DNL Walmart Marketplace] agregando [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Complete la configuración del canal de ventas](#complete-sales-channel-store-setup) para administrar los listados, el inventario, los precios y los pedidos de su surtido de productos [!DNL Walmart Marketplace].

>[!NOTE]
>
>El Administrador de canales requiere una conexión uno a uno entre una cuenta de Walmart y una vista de tienda [!DNL Commerce]. No puede conectar la misma vista de tienda a varias cuentas de Walmart.

## Creación del canal de ventas

1. En el Administrador, abra [!DNL Channel Manager] seleccionando **[!UICONTROL Marketing** > _Canales _> **Administrador de canales]**.

1. En la sección **[!UICONTROL Marketplaces available to connect]**, seleccione **[!UICONTROL Get Started]**.

   ![Conectar el nuevo almacén de [!DNL Walmart] a [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Si es necesario, configure su cuenta de [!DNL Walmart Marketplace Seller].

1. Configure la tienda y la conexión:

   - Seleccione **[!UICONTROL Add Credentials]**.

   - Seleccione la vista de tienda [!DNL Commerce] que ofrece los productos que desea vender en el mercado.

     ![Configurar conexión entre [!DNL Commerce] y [!DNL Walmart Marketplace] desde [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Escriba un(a) **[!UICONTROL store name]** único.

   - Seleccione **[!UICONTROL Adobe [!DNL Commerce] site]** para las listas de productos y el procesamiento de pedidos.

   - Para recibir notificaciones relacionadas con [!DNL Channel Manager], agregue un **[!UICONTROL email address]**.

1. Conectar el canal a [!DNL Walmart Marketplace].

   - Agregue las credenciales para [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) desde su cuenta de [!DNL Walmart Marketplace Seller].

   - Si no tiene las credenciales, obtenerlas de [!DNL Walmart Marketplace Developer Portal] seleccionando **[!UICONTROL Get API credentials]**.

     En el portal para desarrolladores, seleccione su región (EE. UU. y Canadá) y, a continuación, inicie sesión.

     ![[!DNL Walmart Marketplace] inicio de sesión de cuenta](assets/walmart-marketplace-login-page.png){width="600"}

   - En el formulario de clave de API, copie y guarde los valores **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]** para [!UICONTROL Adobe Inc Production API key] en una ubicación segura.

     ![[!DNL Walmart Marketplace API key] página de configuración](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Si la clave [!DNL Adobe Inc] no aparece en el portal de desarrollador, seleccione **[!UICONTROL Add New Key for a Solution Provider]** para configurar los permisos y generar la clave. Para obtener detalles de configuración, consulte [Generar un [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Vuelva a [!DNL Channel Manager] para agregar las credenciales a la información de **[!UICONTROL Walmart Connection]**.

     Cuando se agregan credenciales, la Adobe oculta el secreto de cliente y almacena el valor en un almacén seguro.

1. Seleccione **[!UICONTROL Save Store]** para aplicar la configuración y conectarse a [!DNL Walmart marketplace].

1. Después de conectarse correctamente, [complete la configuración de la tienda](complete-sales-channel-store-setup.md) desde la página de la tienda **[!UICONTROL Channel Manager]**.

![Configurar primer almacén](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Solucionar problemas de conexión

Si falla la conexión con [!DNL Walmart], consulte las [Preguntas frecuentes sobre Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} para obtener sugerencias para la solución de problemas.

- Desde [!DNL Walmart Developer Portal], compruebe que ha copiado las credenciales correctas para la clave de API de producción de [!UICONTROL Adobe Inc.]

- Compruebe que la configuración de acceso de [!UICONTROL Walmart Adobe API key] tiene los permisos correctos. Ver [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirme que el servicio [!DNL Walmart API] está disponible en la [página de estado de la API de Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
