---
title: Conectar el canal de ventas a [!DNL Walmart Marketplace]
description: Configure el canal de ventas y conéctese a Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: e0b7f971f8eb4bc0827a7792ef94d88766adf82e
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# Conectar el canal de ventas a [!DNL Walmart Marketplace]

Después de instalar el Administrador de canales en su [!DNL Commerce] por ejemplo, conecte una tienda de comercio a Walmart Marketplace.

1. [Crear el canal de ventas](#create-the-sales-channel) seleccionando Commerce store para listas de productos.

1. [Conecte el canal a [!DNL Walmart Marketplace] añadiendo credenciales de API de Walmart](#connect-the-channel-to-walmart-marketplace).

1. [Configuración completa del canal de ventas](#complete-store-setup) para administrar anuncios, inventario, precios y pedidos de su gama de productos de Walmart Marketplace.

## Crear el canal de ventas

1. Apertura [!DNL Channel Manager].

   - En el Administrador, seleccione **[!UICONTROL Marketing** > _Canales _> **Administrador de canales]**.

   - Select **[!UICONTROL Connect New Store]**.

      ![Conectar el almacén de comercio a [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Configure el almacén y la conexión:

   - Escriba un **[!UICONTROL store name]**.

   - Seleccione el **[!UICONTROL Adobe Commerce site]** para listas de productos.

   - Agregue un **[!UICONTROL email address]** para recibir notificaciones de servicio relacionadas con [!DNL Channel Manager].

      ![Configurar la conexión entre Commerce y [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

## Conecte el canal a Walmart Marketplace

1. Agregue las credenciales para la [[!DNL Walmart Marketplace Adobe Production API key]](connect-marketplace.md#generate-a-walmart-marketplace-production-api-key) de su [!DNL Walmart Marketplace Seller] cuenta.

   - Si no dispone de las credenciales, seleccione **[!UICONTROL Get API credentials]** para obtenerlos de la variable [!DNL Walmart Marketplace Developer Portal].

      Si se le solicita, seleccione su región (EE. UU. y Canadá) e inicie sesión.

      ![[!DNL Walmart Marketplace] inicio de sesión en la cuenta](assets/walmart-marketplace-login-page.png)

   - En el formulario de clave de API, copie y guarde el **[!UICONTROL Client ID]** y **[!UICONTROL Client Secret]** los valores de la variable [!UICONTROL Adobe Inc Production API key] a una ubicación segura.

      ![[!DNL Walmart Marketplace API key] página de configuración](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Si la variable [!DNL Adobe Inc] La clave no aparece en Developer Portal, seleccione **[!UICONTROL Add New Key for a Solution Provider]** para configurar permisos y generar la clave. Para obtener más información sobre la configuración, consulte [Genere un [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - Volver a [!DNL Channel Manager] para agregar las credenciales al **[!UICONTROL Walmart Connection]** información.

      Al agregar credenciales a [!DNL Channel Manager], el Adobe oculta el secreto del cliente y almacena el valor en un almacén seguro.

1. Select [!UICONTROL Save] para aplicar la configuración y conectarse al [!DNL Walmart marketplace].

Después de conectarse correctamente, administre el canal desde **[!UICONTROL Channel Manager > Marketplace Stores]**.

![[!DNL Walmart Marketplace API key] página de configuración](assets/manage-connected-stores.png)


### Solución de problemas de conexión

Si falla la conexión a Walmart, consulte la [Preguntas frecuentes sobre Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} para obtener sugerencias para la resolución de problemas.

- En el [!DNL Walmart Developer Portal], compruebe que ha copiado las credenciales correctas para la clave de API de producción para [!UICONTROL Adobe Inc.]

- Compruebe que la configuración de acceso para la clave de API de Adobe de Walmart tiene los permisos correctos. Consulte [Requisitos previos de Walmart](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Confirme que la variable [!DNL Walmart API] está disponible en el [Página de estado de la API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.

## Configuración completa de la tienda

Después de conectar una tienda de comercio a [!DNL Walmart Marketplace], puede completar la configuración de la tienda desde el [!DNL Channel Manager Stores] vista.

Para completar la configuración de la tienda:

1. En el Administrador, seleccione **[!UICONTROL Marketing** > **Administrador de canales**].

   ![[!DNL Walmart Marketplace API key] página de configuración](assets/connect-commerce-store-config.png)

1. Abra un canal de ventas conectado seleccionando el icono de lápiz en una fila de entrada de tienda.

1. Iniciar operaciones de canal de ventas.

   - [Agregar productos del catálogo de comercio al administrador de canales](add-products-to-connected-channel.md)

   - [Publicar productos en Walmart utilizando la combinación de productos](publish-listings-to-marketplace.md)

   - [Ver y administrar inventario y precios](inventory-and-price-updates.md)

   - [Ver y administrar pedidos de Walmart desde el Administrador de comercio](manage-orders.md)
