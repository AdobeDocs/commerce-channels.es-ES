---
title: Integración de tiendas
description: Antes de iniciar el proceso de incorporación, debe crear (añadir) un almacén de Sales Channel de Amazon y conectarlo a su cuenta de vendedor de Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Integración de tiendas

Para comenzar con el canal de ventas de Amazon, debe crear (agregar) un almacén de canales de ventas de Amazon y conectarlo a su cuenta de vendedor de Amazon. Estos dos pasos integran el [!DNL Commerce] y cuentas de Amazon para compartir datos, sincronizar productos y mucho más.

_Necesita las credenciales de inicio de sesión principales para su [!DNL Amazon Seller Central] cuenta (el correo electrónico o teléfono que se utilizó para crear la cuenta de vendedor) para conectar la tienda._

>[!NOTE]
>
>Después de la primera integración de almacén, se le pedirá anualmente que renueve su conexión de canal de ventas de Amazon a Amazon, otorgándole de nuevo acceso. Puede renovar o revocar esta autorización en la _Autorizaciones actuales_ en el _Permisos del desarrollador de Amazon MWS_ de la sección **Configuración** > **Permisos de usuario** de su cuenta de Seller Central.

## Agregar una tienda de Amazon

1. En el _Administrador_ barra lateral, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

   Al añadir su primer almacén de canales de ventas de Amazon, la variable _Tareas previas a la configuración_ modal. Una vez añadida la primera tienda, se puede acceder a las tareas previas a la configuración en la [Inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página debajo de _Aprendizaje y preparación_ en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Add Amazon Store]**.

   La variable _[!UICONTROL Add Amazon sales channel]_se abre.

   ![Añadir el almacén de canales de ventas de Amazon](assets/amazon-store-integration.png)

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, elija cuál de sus [!DNL Commerce] sitios web a los que conectarse para este almacén de canales de ventas de Amazon.

   Esta configuración también define el valor predeterminado [!DNL Commerce] almacenar para [importación de pedidos de Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, introduzca su dirección de correo electrónico de contacto preferida.

1. Para **[!UICONTROL New Store Name]**, escriba un nombre descriptivo para el nuevo almacén de canales de ventas de Amazon.

   >[!NOTE]
   >
   >Este nombre se usa como [!DNL Commerce] solo referencia e identifica el almacén en la variable [Inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) página. Desea que sea algo que su equipo pueda identificar fácilmente. Por ejemplo, es posible que el nombre de la tienda de Amazon que vende en la región de Estados Unidos sea `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, elija la región o el país en el que el almacén del canal de ventas de Amazon vende productos. Opciones:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. En el _[!UICONTROL Map your Magento attributes to Amazon]_, haga lo siguiente:

   - Para **[!UICONTROL Product ID on the Amazon market]**, elija el atributo Amazon para asignarlo a la variable [!DNL Commerce] a continuación.

      Este ID le ayuda a hacer coincidir correctamente los productos correspondientes de su [!DNL Commerce] catálogo.

   - Para **[!UICONTROL Map a Magento attribute]**, elija el [!DNL Commerce] atributo de producto para asignarlo al atributo de Amazon seleccionado anteriormente.

      [Asignación de atributos](./ob-creating-magento-attributes.md) ayuda a garantizar que el listado de Amazon coincide correctamente con el producto correspondiente de su [!DNL Commerce] catálogo.

1. Haga clic en **[!UICONTROL Connect]**.

   El cuadro de diálogo se cierra y el nuevo almacén aparece en el [Inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) con un mensaje de confirmación.

## Conectar una tienda a [!DNL Amazon Seller Central]

1. En el panel de la tienda, haga clic en **[!UICONTROL Connect store]** en la tarjeta de la tienda que se va a iniciar [!DNL Amazon Seller Central] en una pestaña nueva.

1. Escriba la [!DNL Amazon Seller Central] credenciales de cuenta y haga clic en **[!UICONTROL Sign in]**.

   Para completar esta conexión, debe iniciar sesión en su [!DNL Amazon Seller Central] cuenta que utiliza las credenciales de inicio de sesión del usuario principal (el correo electrónico o el teléfono utilizados para crear la cuenta de vendedor).

1. Si se le solicita, rellene la Autorización de dos factores (2FA) de Amazon introduciendo el código que recibe de Amazon y haga clic en **[!UICONTROL Sign in]**.

1. En el _[!UICONTROL Amazon Marketplace Web Service]_página de confirmación, seleccione la opción[!UICONTROL I understand...]&quot; casilla de verificación y haga clic en **[!UICONTROL Next]**.

1. En el _[!UICONTROL You are almost done]_mensaje, haga clic en **[!UICONTROL Continue]**.

   Ha concedido permiso al canal de ventas de Amazon para acceder y compartir datos con su [!DNL Amazon Seller Central] cuenta. La página de Amazon se cierra y aparece un mensaje de confirmación.

   La variable [Inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) se abre la página mostrando las tarjetas de la tienda Amazon.

   Para ver el tablero de la tienda, haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

![Página principal del canal de ventas de Amazon con la nueva tarjeta de tienda](assets/asc-dashboard-after-2fa.png)

El nuevo almacén de canales de ventas de Amazon ahora está conectado a su [!DNL Amazon Seller Central] cuenta.

![Icono Siguiente](assets/btn-next.png) [**Continuar creando una regla de lista**](./ob-create-listing-rule.md)
