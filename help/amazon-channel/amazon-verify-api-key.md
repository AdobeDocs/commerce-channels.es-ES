---
title: Añadir o verificar la clave de API de Amazon
description: En la configuración de Commerce, la clave de API de Amazon validada le permite integrar sus tiendas con su cuenta de Amazon Seller.
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Añadir o verificar la clave de API de Amazon

Al acceder al canal de ventas de Amazon, [!DNL Commerce] comprueba y valida automáticamente la clave de API de Amazon que ha añadido en la configuración de la tienda. Si se valida, puede pasar al siguiente paso, [Integración de tiendas](./store-integration.md).

Si falta la clave de API de Amazon, no es válida o ha caducado, debe actualizarla. Aparece un mensaje que le solicita que obtenga una clave de API y que la añada a la configuración del canal de ventas de Amazon.

## Obtenga y agregue la clave de API de Amazon cuando se le solicite

La clave de API se valida cada vez que accede al canal de ventas de Amazon.

1. Inicie sesión en el [!DNL Commerce] Administrador.

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Si es la primera vez que accede al canal de ventas de Amazon o si la clave de API requiere actualización, el sistema le indicará que siga el proceso.

   ![Obtener y agregar el mensaje de clave de API de Amazon](assets/amazon-api-verification-prompt.png)

1. Haga clic en **[!UICONTROL Sign in]** para acceder a su [!DNL Commerce] cuenta web.

   La página Cuentas de comercio se abre en una nueva pestaña del explorador.

   - Si ha iniciado sesión en su [!DNL Commerce] cuenta, la variable _[!UICONTROL API Portal]_de la sección_[!UICONTROL My Account]_ aparece automáticamente.

   - Si no ha iniciado sesión, se le pedirá que introduzca su [!DNL Commerce] nombre de usuario y contraseña de la cuenta antes de _[!UICONTROL API Portal]_se abre.

   - Si no tiene una cuenta, visite [el [!DNL Commerce] página de cuenta](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;} y regístrese. Esta cuenta debe formar parte de su empresa o negocio.

1. Si es necesario, puede ver y generar claves de API en la variable _[!UICONTROL API Portal]_en la ficha [!DNL Commerce] cuenta.

   Para crear una clave de API, introduzca una descripción como `Amazon Sales Channel` y haga clic en **[!UICONTROL Add New]**. La nueva clave se genera y se muestra con el nombre introducido. Haga clic en **[!UICONTROL Copy]** para copiar la nueva clave.

   ![Generar o copiar una clave de API](assets/amazon-add-api-key.png)

1. Con la nueva clave generada y copiada, vuelva a la _[!UICONTROL Amazon Sales Channel]_en el navegador.

1. En el _[!UICONTROL Welcome to Amazon Sales Channel]_página, haga clic en **[!UICONTROL Add the key]**.

   El explorador sale del canal de ventas de Amazon y una página de configuración de tienda abre la variable _[!UICONTROL Api Keys]_en el [!DNL Commerce] Administrador. Puede abrir esta página manualmente cuando vaya a **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expandir **[!UICONTROL Services]** en el panel izquierdo y elija **[!UICONTROL Magento Services]**.

1. Pegar la clave copiada para **[!UICONTROL Production Api key]**.

1. Haga clic en **[!UICONTROL Save Config]**. Ahora puede volver al canal de ventas de Amazon.

   ![Añadir la clave de API en la configuración de la tienda](assets/config-magento-services-api-screen.png)

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Volver a acceder a los déclencheur de canal de ventas de Amazon [!DNL Commerce] compruebe y valide su clave de API y le permite continuar.

   Si se le solicita que vuelva a verificar la clave, repita esta _Agregar y verificar_ proceso.

![Icono Siguiente](assets/btn-next.png) [**Continuar con la integración del almacén**](./store-integration.md)
