---
title: Conectarse a Commerce Services
description: Conecte la instancia del Administrador de canales a [!DNL Commerce services] para habilitar la sincronización de datos y la comunicación entre la instancia de Commerce, Channel Manager y otros servicios de soporte.
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Conectarse a Commerce Services

Commerce Services Connector integra el servicio Channel Manager con instancias de Adobe Commerce y Magento Open Source. El conector permite la sincronización de datos y la comunicación entre los [!DNL Commerce] instancia, [!DNL Channel Manager]y otros servicios de soporte.

La configuración de Commerce Services Connector es un proceso único necesario para utilizar Adobe [Servicios de Commerce SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} like [!DNL Channel Manager], [!DNL Live Search]y [!DNL Product Recommendations]. Si ya ha configurado el conector para otro servicio, puede omitir este paso.

## Requisitos previos

- **Cuenta de comercio con [Acceso de administrador](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** a su instancia de Commerce** Los propietarios de cuentas y los usuarios administradores pueden configurar cuentas de usuario desde la instancia de Commerce o desde la línea de comandos utilizando la variable [!DNL Commerce] Comando CLI `admin:user:create`.

- **Adobe Commerce [Claves de API de producción](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}**-Habilitar el acceso a la API a los servicios requeridos por el Administrador de canales

   Para proporcionar las credenciales, el titular de una licencia de comercio o el propietario de la cuenta tiene la opción de
   [acceso compartido](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} o asigne la variable [Clave de API](https://docs.magento.com/user-guide/system/saas.html#apikey)Credenciales de {target=&quot;_blank&quot;} para un desarrollador de confianza.

## Configuración del conector de Commerce Services

1. Abra la configuración de Servicios de almacenamiento .

   - En Administración, seleccione [!UICONTROL Stores].

   - En *Configuración*, seleccione [!UICONTROL Configuration].

   - En el [!UICONTROL Configuration] página, expandir [!UICONTROL Services] y seleccione [!UICONTROL Commerce Services Connector].

1. Agregue las claves de la API de producción de su cuenta de Adobe Commerce.

   ![[!DNL Commerce Service Connector] en el [!DNL Admin] ver](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Si su [!DNL Commerce] la instancia tiene otro [!DNL Adobe Commerce] servicios como [!DNL Live Search] o [!DNL Product Recommendations] instalado, la información de las credenciales se muestra en la interfaz y no se requiere ninguna configuración adicional.

1. Configure el proyecto SaaS y el espacio de datos para que Commerce Services pueda enviar datos al servicio Channel Manager.

   ![[!DNL Commerce Service Connector] Configuración del identificador SaaS en la variable [!DNL Admin] ver](assets/commerce-services-connector-saas-config.png)

