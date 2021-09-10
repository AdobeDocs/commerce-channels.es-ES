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

Para comenzar con el canal de ventas de Amazon, debe crear (agregar) un almacén de canales de ventas de Amazon y conectarlo a su cuenta de vendedor de Amazon. Estos dos pasos integran sus cuentas de [!DNL Commerce] y Amazon para compartir datos, sincronizar productos y mucho más.

_Necesita las credenciales de inicio de sesión principales de su  [!DNL Amazon Seller Central] cuenta (el correo electrónico o el teléfono utilizado para crear la cuenta de vendedor) para conectar su tienda._

>[!NOTE]
>
>Después de la primera integración de almacén, se le pedirá anualmente que renueve su conexión de canal de ventas de Amazon a Amazon, otorgándole de nuevo acceso. Puede renovar o revocar esta autorización en la tabla _Autorizaciones actuales_ de la sección _Permisos de desarrollador de Amazon MWS_ de la página **Configuración** > **Permisos de usuario** de la cuenta de Seller Central.

## Agregar una tienda de Amazon

1. En la barra lateral _Admin_, vaya a **Marketing** > _Canales_ > **Sales Channel de Amazon**.

   Al añadir el primer almacén de canales de ventas de Amazon, aparece el modal _Pre-Setup Tasks_. Una vez añadida la primera tienda, se puede acceder a las tareas previas a la configuración en la página principal del [canal de ventas de Amazon](./amazon-sales-channel-home.md) en _Aprendizaje y preparación_ en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Add Amazon Store]**.

   Se abre la página _[!UICONTROL Add Amazon sales channel]_.

   ![Añadir el almacén de canales de ventas de Amazon](assets/amazon-store-integration.png)

1. Para **[!UICONTROL Magento Website to use for Amazon Listing]**, elija cuál de sus [!DNL Commerce] sitios web se conectará para este almacén de canales de ventas de Amazon.

   Esta configuración también define el [!DNL Commerce] almacén predeterminado para [importar pedidos de Amazon](./order-settings.md).

1. Para **[!UICONTROL Email Address]**, introduzca su dirección de correo electrónico de contacto preferida.

1. Para **[!UICONTROL New Store Name]**, escriba un nombre descriptivo para el nuevo almacén de canales de ventas de Amazon.

   >[!NOTE]
   >
   >Este nombre se utiliza solo como referencia de [!DNL Commerce] e identifica el almacén en la página principal del [canal de ventas de Amazon](./amazon-sales-channel-home.md). Desea que sea algo que su equipo pueda identificar fácilmente. Por ejemplo, la tienda de Amazon que vende en la región de Estados Unidos puede tener el nombre `Amazon Store USA`.

1. Para **[!UICONTROL Amazon Marketplace Country]**, elija la región/país en la que vende productos este almacén de canales de ventas de Amazon. Opciones:

   - Estados Unidos
   - Canadá
   - México
   - Reino Unido

1. En la sección _[!UICONTROL Map your Magento attributes to Amazon]_, haga lo siguiente:

   - Para **[!UICONTROL Product ID on the Amazon market]**, elija el atributo Amazon que desea asignar al atributo [!DNL Commerce] seleccionado a continuación.

      Este ID ayuda a que coincida correctamente con los productos correspondientes de su catálogo [!DNL Commerce].

   - Para **[!UICONTROL Map a Magento attribute]**, elija el atributo del producto [!DNL Commerce] para asignarlo al atributo de Amazon seleccionado anteriormente.

      [Asignar ](./ob-creating-magento-attributes.md) atributos ayuda a garantizar que el listado de Amazon coincide correctamente con el producto correspondiente del  [!DNL Commerce] catálogo.

1. Haga clic en **[!UICONTROL Connect]**.

   El cuadro de diálogo se cierra y el nuevo almacén aparece en la página [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) con un mensaje de confirmación.

## Conectar un almacén a [!DNL Amazon Seller Central]

1. En el panel de la tienda, haga clic **[!UICONTROL Connect store]** en la tarjeta de la tienda para iniciar [!DNL Amazon Seller Central] en una nueva pestaña.

1. Introduzca sus credenciales de cuenta [!DNL Amazon Seller Central] y haga clic en **[!UICONTROL Sign in]**.

   Para completar esta conexión, debe iniciar sesión en su cuenta [!DNL Amazon Seller Central] utilizando las credenciales de inicio de sesión del usuario principal (el correo electrónico o el teléfono utilizados para crear la cuenta de vendedor).

1. Si se le solicita, rellene la Autorización de dos factores (2FA) de Amazon introduciendo el código que recibe de Amazon y haga clic en **[!UICONTROL Sign in]**.

1. En la página de confirmación _[!UICONTROL Amazon Marketplace Web Service]_, seleccione la casilla &quot;[!UICONTROL I understand...]&quot; y haga clic en **[!UICONTROL Next]**.

1. En el mensaje _[!UICONTROL You are almost done]_, haga clic en **[!UICONTROL Continue]**.

   Ha concedido permiso al canal de ventas de Amazon para acceder y compartir datos con su cuenta [!DNL Amazon Seller Central]. La página de Amazon se cierra y aparece un mensaje de confirmación.

   Se abre la página [inicio del canal de ventas de Amazon](./amazon-sales-channel-home.md) que muestra las tarjetas de la tienda Amazon.

   Para ver el tablero de la tienda, haga clic en **[!UICONTROL View Store]** en la tarjeta de la tienda.

![Página principal del canal de ventas de Amazon con la nueva tarjeta de tienda](assets/asc-dashboard-after-2fa.png)

El nuevo almacén de canales de ventas de Amazon ahora está conectado a su cuenta [!DNL Amazon Seller Central].

![Siguiente ](assets/btn-next.png) [**iconoContinuar creando una regla de lista**](./ob-create-listing-rule.md)
