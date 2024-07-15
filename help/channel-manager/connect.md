---
title: 'Conectar con [!DNL Commerce] Servicios'
description: "Conecte el Administrador de canales a  [!DNL Commerce] servicios para habilitar la sincronización de datos y la comunicación entre la instancia  [!DNL Commerce] y el Administrador de canales, así como otros servicios de soporte."
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Conectar con servicios de [!DNL Commerce]

[!DNL Commerce Services Connector] integra el servicio Administrador de canales con las instancias de Adobe Commerce y Magento Open Source. El conector habilita la sincronización de datos y la comunicación entre la instancia [!DNL Commerce], [!DNL Channel Manager] y otros servicios auxiliares.

La configuración de [!DNL Commerce Services Connector] es un proceso único necesario para usar [servicios SaaS de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html), como [!DNL Channel Manager], [!DNL Live Search] y [!DNL Product Recommendations]. Si ya ha configurado el conector para otro servicio, omita este paso.

## Requisitos

- **cuenta de Commerce**-Para instalar software en [!DNL Commerce] instancias, debe tener una cuenta con acceso de propietario o administrador a la plataforma [!DNL Commerce].

  Los propietarios de cuenta y los superusuarios pueden crear cuentas de administrador desde la instancia [!DNL Commerce] o desde la línea de comandos utilizando el comando [!DNL Commerce] de CLI `admin:user:create`.

- **Clave de API de producción de Adobe Commerce**- Esta [clave](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) habilita el acceso de API a los servicios requeridos por Channel Manager. Necesita las credenciales públicas y privadas para esta clave.

>[!TIP]
>
>Para proporcionar las credenciales, el titular de una licencia de [!DNL Commerce] o el propietario de una cuenta tienen opciones para [compartir el acceso](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) o dar las credenciales de la [clave API](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) a un desarrollador de confianza.

## Configurar [!DNL Commerce Services Connector]

1. Abra la Configuración de servicios de tienda.

   - En el Administrador, seleccione **[!UICONTROL Stores]**.

   - En *[!UICONTROL Settings]*, seleccione **[!UICONTROL Configuration]**.

   - Expanda **[!UICONTROL Services]** y seleccione **[!UICONTROL Commerce Services Connector]**.

1. Agregue las credenciales de la clave API de producción de su cuenta de Adobe Commerce.

   ![[!DNL Commerce Services Connector] servicio en la vista [!DNL Admin]](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Si la instancia de [!DNL Commerce] tiene instalados otros servicios de [!DNL Adobe Commerce], como [!DNL Live Search] o [!DNL Product Recommendations], la información de credenciales se muestra en la interfaz y no se requiere ninguna configuración adicional.

1. Configure el proyecto SaaS y el espacio de datos para que los servicios de Commerce puedan enviar datos al servicio de Channel Manager.

   ![[!DNL Commerce Services Connector] Configuración del identificador SaaS en la vista [!DNL Admin]](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

