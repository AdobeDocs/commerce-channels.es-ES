---
title: Integración de tienda con  [!DNL Amazon Seller Account]
description: Antes de iniciar el proceso de incorporación, debes crear (añadir) un almacén de Sales Channel de Amazon y conectarlo a tu cuenta de vendedor de Amazon.
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Integración de tienda con [!DNL Amazon Seller Account]

Para comenzar con el canal de ventas de Amazon, debe crear (agregar) un almacén de canales de ventas de Amazon y conectarlo a su [!DNL Amazon Seller Account]. Estos dos pasos integran tus cuentas de [!DNL Commerce] y Amazon para compartir datos, sincronizar productos y mucho más.

_Necesitas las credenciales de inicio de sesión principales de tu cuenta de [!DNL Amazon Seller Central] (el correo electrónico o el teléfono usado para crear la cuenta de vendedor) para conectar tu tienda._

>[!NOTE]
>
>Después de integrar su primera tienda, se le pedirá anualmente que renueve su conexión de canal de ventas de Amazon a Amazon concediendo acceso de nuevo. Puede renovar o revocar esta autorización en la tabla _Autorizaciones actuales_ de la sección _Permisos de desarrollador de Amazon MWS_ de la página **Configuración** > **Permisos de usuario** de su cuenta de Seller Central.

## Añadir una tienda Amazon

1. En la barra lateral de _Admin_, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

   Al agregar su primer almacén de canales de ventas de Amazon, aparece el modal _Tareas previas a la configuración_. Una vez agregada la primera tienda, puede acceder a las tareas de preconfiguración en la página de inicio del [canal de ventas de Amazon](./amazon-sales-channel-home.md), en _Aprendizaje y preparación_, en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Add Amazon Store]**.

   Se abre la página _[!UICONTROL Add Amazon sales channel]_.

   ![Agregar el almacén del canal de ventas de Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, elige a cuál de tus [!DNL Commerce] sitios web conectar para este almacén de canales de ventas de Amazon.

   Esta configuración también define el almacén predeterminado de [!DNL Commerce] para [importar pedidos de Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, escribe tu dirección de correo electrónico de contacto preferida.

1. Para **[!UICONTROL New Store Name]**, escriba un nombre descriptivo para el nuevo almacén de canales de ventas de Amazon.

   >[!NOTE]
   >
   >Este nombre se usa solamente como referencia de [!DNL Commerce] e identifica la tienda en la página [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md). Desea que sea algo que su equipo pueda identificar fácilmente. Por ejemplo, la tienda Amazon que vende en la región de Estados Unidos podría llamarse `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, elija la región o el país en el que el almacén del canal de ventas de Amazon vende productos. Opciones:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. En la sección _[!UICONTROL Map your Magento attributes to Amazon]_, haga lo siguiente:

   - Para **[!UICONTROL Product ID on the Amazon market]**, elija el atributo de Amazon que desea asignar al atributo [!DNL Commerce] seleccionado a continuación.

     Este identificador ayuda a hacer coincidir correctamente los productos correspondientes del catálogo [!DNL Commerce].

   - Para **[!UICONTROL Map a Magento attribute]**, elija el atributo de producto [!DNL Commerce] que desea asignar al atributo de Amazon seleccionado anteriormente.

     [Asignar atributos](./ob-creating-magento-attributes.md) ayuda a garantizar que su anuncio de Amazon coincida correctamente con el producto correspondiente de su catálogo [!DNL Commerce].

1. Haga clic en **[!UICONTROL Connect]**.

   El cuadro de diálogo se cierra y la nueva tienda aparece en la página de inicio del [canal de ventas Amazon](./amazon-sales-channel-home.md) con un mensaje de confirmación.

## Conectar un almacén a [!DNL Amazon Seller Central]

1. En el panel de la tienda, haga clic en **[!UICONTROL Connect store]** en la tarjeta de la tienda para iniciar [!DNL Amazon Seller Central] en una nueva pestaña.

1. Escriba las credenciales de su cuenta de [!DNL Amazon Seller Central] y haga clic en **[!UICONTROL Sign in]**.

   Para completar esta conexión, debes iniciar sesión en tu cuenta de [!DNL Amazon Seller Central] con las credenciales de inicio de sesión del usuario principal (el correo electrónico o el teléfono usado para crear la cuenta de vendedor).

1. Si se le solicita, complete la Autorización de dos factores de Amazon (2FA) introduciendo el código que recibe de Amazon y haga clic en **[!UICONTROL Sign in]**.

1. En la página de confirmación _[!UICONTROL Amazon Marketplace Web Service]_, seleccione la casilla &quot;[!UICONTROL I understand...]&quot; y haga clic en **[!UICONTROL Next]**.

1. En el mensaje _[!UICONTROL You are almost done]_, haga clic en **[!UICONTROL Continue]**.

   Ha concedido permiso al canal de ventas de Amazon para acceder a sus datos de [!DNL Amazon Seller Central] y compartirlos con ella. La página de Amazon se cierra y aparece un mensaje de confirmación.

   Se abre la página de inicio del canal de ventas [Amazon](./amazon-sales-channel-home.md) con las tarjetas de la tienda Amazon.

   Para ver el panel de la tienda, haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

![canal de ventas Amazon con tarjeta de la tienda nueva](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

El nuevo almacén del canal de ventas de Amazon ahora está conectado a su cuenta de [!DNL Amazon Seller Central].

![Siguiente icono](assets/btn-next.png) [**Sigue creando una regla de anuncio**](./ob-create-listing-rule.md)
