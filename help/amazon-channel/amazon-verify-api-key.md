---
title: Añadir o verificar la clave de API de Amazon
description: En la configuración de Commerce, la clave de API de Amazon validada permite integrar las tiendas con la cuenta de vendedor de Amazon.
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Añadir o verificar la clave de API de Amazon

Al acceder al canal de ventas de Amazon, [!DNL Commerce] comprueba y valida automáticamente la clave de API de Amazon que añadió en la configuración de la tienda. Si se valida, puede pasar al siguiente paso, [Integración de tienda](./store-integration.md).

Si falta la clave de API de Amazon, si no es válida o si ha caducado, debe actualizarla. Aparece un mensaje que le solicita que obtenga una clave de API y que la añada a la configuración de su canal de ventas de Amazon.

## Obtenga y agregue la clave de API de Amazon cuando se le solicite

La clave de API se valida cada vez que accede al canal de ventas de Amazon.

1. Inicie sesión en [!DNL Commerce] Administrador.

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Si es la primera vez que accede al canal de ventas de Amazon o si la clave de API requiere una actualización, el sistema le guiará a través del proceso.

   ![Obtener y agregar el indicador de clave de API de Amazon](assets/amazon-api-verification-prompt.png){width="500"}

1. Clic **[!UICONTROL Sign in]** para acceder a su [!DNL Commerce] cuenta web.

   La página de cuentas de Commerce se abre en una nueva pestaña del explorador.

   - Si ha iniciado sesión en su [!DNL Commerce] cuenta, la _[!UICONTROL API Portal]_de la sección_[!UICONTROL My Account]_ página aparece automáticamente.

   - Si no ha iniciado sesión, se le pedirá que introduzca su [!DNL Commerce] nombre de usuario y contraseña de la cuenta antes de _[!UICONTROL API Portal]_aparece la pestaña.

   - Si no tiene una cuenta de, visite [el [!DNL Commerce] página de cuenta](https://account.magento.com/customer/account/login/){target="_blank"} y registrarse. Esta cuenta debe ser parte de su compañía o negocio.

1. Si es necesario, puede ver y generar claves API en la _[!UICONTROL API Portal]_pestaña en su [!DNL Commerce] cuenta.

   Para crear una clave de API, escriba una descripción como `Amazon Sales Channel` y haga clic en **[!UICONTROL Add New]**. La nueva clave se genera y se muestra con el nombre introducido. Clic **[!UICONTROL Copy]** para copiar la nueva clave.

   ![Generar o copiar una clave de API](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. Con la nueva clave generada y copiada, vuelva a la _[!UICONTROL Amazon Sales Channel]_en el explorador.

1. En el _[!UICONTROL Welcome to Amazon Sales Channel]_página, haga clic en **[!UICONTROL Add the key]**.

   El explorador sale del canal de ventas de Amazon y se abre una página de configuración de tienda de _[!UICONTROL Api Keys]_página en la [!DNL Commerce] Administrador. Puede abrir esta página manualmente cuando vaya a **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expanda **[!UICONTROL Services]** en el panel izquierdo y seleccione **[!UICONTROL Magento Services]**.

1. Pegue la clave copiada para **[!UICONTROL Production Api key]**.

1. Haga clic **[!UICONTROL Save Config]**. Ahora puede volver al canal de ventas de Amazon.

   ![Añadir la clave API en la configuración de la tienda](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. En el _[!UICONTROL Admin]_barra lateral, vaya a **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Reacceso a déclencheur de canal de ventas de Amazon [!DNL Commerce] compruebe y valide la clave de API y le permita continuar.

   Si se le pide que vuelva a comprobar la clave, repita esto _Agregar y verificar_ proceso.

![Icono Siguiente](assets/btn-next.png) [**Continuar con la integración de almacenamiento**](./store-integration.md)
