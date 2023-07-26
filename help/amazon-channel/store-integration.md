---
title: Integración de tienda con un [!DNL Amazon Seller Account]
description: Antes de iniciar el proceso de incorporación, debes crear (añadir) un almacén de Sales Channel de Amazon y conectarlo a tu cuenta de vendedor de Amazon.
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Integración de tienda con un [!DNL Amazon Seller Account]

Para empezar a usar el canal de ventas de Amazon, debe crear (añadir) un almacén de canales de ventas de Amazon y conectarlo a su [!DNL Amazon Seller Account]. Estos dos pasos integran su [!DNL Commerce] y cuentas de Amazon para compartir datos, sincronizar productos y mucho más.

_Necesita las credenciales de inicio de sesión principales para su [!DNL Amazon Seller Central] cuenta (el correo electrónico o teléfono usado para crear la cuenta de vendedor) para conectar tu tienda._

>[!NOTE]
>
>Después de integrar su primera tienda, se le pedirá anualmente que renueve su conexión de canal de ventas de Amazon a Amazon concediendo acceso de nuevo. Puede renovar o revocar esta autorización en el _Autorizaciones actuales_ tabla en el _Permisos de desarrollador de Amazon MWS_ de la sección **Configuración** > **Permisos de usuario** de tu cuenta de Seller Central.

## Añadir una tienda Amazon

1. En el _Administrador_ barra lateral, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

   Al añadir su primer almacén de canales de ventas de Amazon, la variable _Tareas previas a la instalación_ modal aparece. Una vez añadida la primera tienda, se puede acceder a las tareas de preconfiguración en la [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página debajo de _Aprendizaje y preparación_ en el menú del lado izquierdo.

1. Clic **[!UICONTROL Add Amazon Store]**.

   El _[!UICONTROL Add Amazon sales channel]_se abre la página.

   ![Añadir el almacén del canal de ventas de Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, elija cuál de sus [!DNL Commerce] sitios web a los que conectarse para esta tienda de canales de ventas de Amazon.

   Esta configuración también define el valor predeterminado [!DNL Commerce] almacenar para [importación de pedidos de Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, introduzca su dirección de correo electrónico de contacto preferida.

1. Para **[!UICONTROL New Store Name]**, escriba un nombre descriptivo para el nuevo almacén de canales de ventas de Amazon.

   >[!NOTE]
   >
   >Este nombre se utiliza como [!DNL Commerce] solo de referencia e identifica el almacén en [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página. Desea que sea algo que su equipo pueda identificar fácilmente. Por ejemplo, la tienda de Amazon que vende en la región de Estados Unidos podría llamarse `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, elija la región o el país en el que Amazon vende sus productos. Opciones:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. En el _[!UICONTROL Map your Magento attributes to Amazon]_, haga lo siguiente:

   - Para **[!UICONTROL Product ID on the Amazon market]**, elija el atributo de Amazon para asignarlo al [!DNL Commerce] atributo seleccionado a continuación.

     Este ID ayuda a que los productos correspondientes de su [!DNL Commerce] catálogo.

   - Para **[!UICONTROL Map a Magento attribute]**, elija la [!DNL Commerce] atributo de producto para asignarlo al atributo de Amazon seleccionado anteriormente.

     [Atributos de asignación](./ob-creating-magento-attributes.md) le ayuda a garantizar que su anuncio de Amazon coincide correctamente con el producto correspondiente de su [!DNL Commerce] catálogo.

1. Clic **[!UICONTROL Connect]**.

   El cuadro de diálogo se cierra y aparece el nuevo almacén en [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) con un mensaje de confirmación.

## Conectar una tienda a [!DNL Amazon Seller Central]

1. En el tablero de la tienda, haga clic en **[!UICONTROL Connect store]** en la tarjeta de la tienda para iniciar [!DNL Amazon Seller Central] en una pestaña nueva.

1. Introduzca su [!DNL Amazon Seller Central] credenciales de la cuenta y haga clic en **[!UICONTROL Sign in]**.

   Para completar esta conexión, debe iniciar sesión en su [!DNL Amazon Seller Central] cuenta con las credenciales de inicio de sesión del usuario principal (el correo electrónico o teléfono usado para crear la cuenta de vendedor).

1. Si se le solicita, complete la Autorización de dos factores de Amazon (2FA) introduciendo el código que recibe de Amazon y haga clic en **[!UICONTROL Sign in]**.

1. En el _[!UICONTROL Amazon Marketplace Web Service]_página de confirmación, seleccione la &quot;[!UICONTROL I understand...]&quot; y haga clic en **[!UICONTROL Next]**.

1. En el _[!UICONTROL You are almost done]_Mensaje, haga clic en **[!UICONTROL Continue]**.

   Ha concedido permiso al canal de ventas de Amazon para acceder a datos y compartirlos con su [!DNL Amazon Seller Central] cuenta. La página de Amazon se cierra y aparece un mensaje de confirmación.

   El [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) se abre la página mostrando las tarjetas de la tienda Amazon.

   Para ver el tablero de la tienda, haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

![inicio del canal de ventas de Amazon con la nueva tarjeta de la tienda](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

El nuevo almacén del canal de ventas de Amazon ya está conectado a su [!DNL Amazon Seller Central] cuenta.

![Icono Siguiente](assets/btn-next.png) [**Continuar para crear una regla de anuncio**](./ob-create-listing-rule.md)
