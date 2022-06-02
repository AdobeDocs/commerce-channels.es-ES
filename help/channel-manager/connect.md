---
title: Conectar a [!DNL Commerce] servicios
description: Conectar el Administrador de canales a [!DNL Commerce] para permitir la sincronización de datos y la comunicación entre los [!DNL Commerce] instancia, Channel Manager y otros servicios de soporte.
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: aaab7aa7feb05264c24386e62193564dc5ae8fe3
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# Conectar a [!DNL Commerce] servicios

Commerce Services Connector integra el servicio Channel Manager con instancias de Adobe Commerce y Magento Open Source. El conector permite la sincronización de datos y la comunicación entre los [!DNL Commerce] instancia, [!DNL Channel Manager]y otros servicios de soporte.

La configuración de Commerce Services Connector es un proceso único necesario para utilizar Adobe [Servicios de Commerce SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} like [!DNL Channel Manager], [!DNL Live Search]y [!DNL Product Recommendations]. Si ya ha configurado el conector para otro servicio, omita este paso.

## Requisitos

- **Cuenta de comercio**-Para instalar software en instancias de Commerce, debe tener una cuenta con acceso de Propietario o Administrador a la plataforma Commerce.

   Los propietarios de cuentas y los superusuarios pueden crear cuentas de administrador desde la instancia de Commerce o desde la línea de comandos utilizando la variable [!DNL Commerce] Comando CLI `admin:user:create`.

- **Clave de API de producción de Adobe Commerce**-Esto [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} habilita el acceso de API a los servicios requeridos por el Administrador de canales. Necesita las credenciales públicas y privadas para esta clave.

>[!TIP]
>
>Para proporcionar las credenciales, el titular de una licencia de comercio o el propietario de la cuenta tiene la opción de [acceso compartido](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} o asigne la variable [Clave de API](https://docs.magento.com/user-guide/system/saas.html#apikey)Credenciales de {target=&quot;_blank&quot;} para un desarrollador de confianza.

## Configuración del conector de Commerce Services

1. Abra la configuración de Servicios de almacenamiento .

   - En Administración, seleccione **[!UICONTROL Stores]**.

   - En *[!UICONTROL Settings]*, seleccione **[!UICONTROL Configuration]**.

   - Expandir **[!UICONTROL Services]** y seleccione **[!UICONTROL Commerce Services Connector]**.

1. Agregue las credenciales clave de la API de producción de su cuenta de Adobe Commerce.

   ![[!DNL Commerce Service Connector] en el [!DNL Admin] ver](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Si su [!DNL Commerce] la instancia tiene otro [!DNL Adobe Commerce] servicios como [!DNL Live Search] o [!DNL Product Recommendations] instalado, la información de las credenciales se muestra en la interfaz y no se requiere ninguna configuración adicional.

1. Configure el proyecto SaaS y el espacio de datos para que Commerce Services pueda enviar datos al servicio Channel Manager.

   ![[!DNL Commerce Service Connector] Configuración del identificador SaaS en la variable [!DNL Admin] ver](assets/commerce-services-connector-saas-config.png)

