---
title: 'Conectar a [!DNL Commerce] Servicios'
description: '''Conectar el Administrador de canales a [!DNL Commerce] servicios para permitir la sincronización de datos y la comunicación entre los [!DNL Commerce] instancia de, Channel Manager y otros servicios de asistencia".'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Conectar a [!DNL Commerce] Servicios

El [!DNL Commerce Services Connector] integra el servicio Channel Manager con las instancias de Adobe Commerce y Magento Open Source. El conector permite la sincronización de datos y la comunicación entre los [!DNL Commerce] ejemplo, [!DNL Channel Manager]y otros servicios de soporte.

[!DNL Commerce Services Connector] la configuración es un proceso único necesario para utilizar [Servicios SaaS de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) como [!DNL Channel Manager], [!DNL Live Search], y [!DNL Product Recommendations]. Si ya ha configurado el conector para otro servicio, omita este paso.

## Requisitos

- **Cuenta de Commerce**-Para instalar software en [!DNL Commerce] instancias, debe tener una cuenta con acceso de Propietario o Administrador a [!DNL Commerce] plataforma.

  Los propietarios de cuenta y los superusuarios pueden crear cuentas de administrador desde el [!DNL Commerce] o desde la línea de comandos utilizando la variable [!DNL Commerce] comando CLI `admin:user:create`.

- **Clave de API de producción de Adobe Commerce**-Esto [key](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) habilita el acceso de API a los servicios requeridos por Channel Manager. Necesita las credenciales públicas y privadas para esta clave.

>[!TIP]
>
>Para proporcionar las credenciales, [!DNL Commerce] el titular de la licencia o el titular de la cuenta tienen opciones para [acceso compartido](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html), o asigne el [Clave de API](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) credenciales a un desarrollador de confianza.

## Configure las variables [!DNL Commerce Services Connector]

1. Abra la Configuración de servicios de tienda.

   - En Admin, seleccione **[!UICONTROL Stores]**.

   - En *[!UICONTROL Settings]*, seleccione **[!UICONTROL Configuration]**.

   - Expandir **[!UICONTROL Services]** y seleccione **[!UICONTROL Commerce Services Connector]**.

1. Agregue las credenciales de la clave API de producción de su cuenta de Adobe Commerce.

   ![[!DNL Commerce Services Connector] servicio en la [!DNL Admin] vista](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Si su [!DNL Commerce] la instancia tiene otros [!DNL Adobe Commerce] servicios como [!DNL Live Search] o [!DNL Product Recommendations] instalado, la información de credenciales se muestra en la interfaz y no se requiere ninguna otra configuración.

1. Configure el proyecto SaaS y el espacio de datos para que Commerce Services pueda enviar datos al servicio Channel Manager.

   ![[!DNL Commerce Services Connector] Configuración del identificador SaaS en [!DNL Admin] vista](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

