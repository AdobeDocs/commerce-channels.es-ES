---
title: Incorporado [!DNL Channel Manager]
description: Conecte la instancia a la variable [!DNL Channel Manager] completando algunos pasos de integración.
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: f57c6db4c0314272d10bb5483d2c8a0ae396a9fc
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Incorporado [!DNL Channel Manager]

Administrador de canales integrado instalando la extensión del Administrador de canales en su [!DNL Commerce] y configurar conexiones de API. Estas conexiones permiten la comunicación y la sincronización de datos entre su instancia de Commerce y Walmart Marketplace.

Después de completar la incorporación, configure y administre las operaciones de canal de ventas desde la [!UICONTROL Channel Manager] en la [!UICONTROL Commerce Admin Marketing] para abrir el Navegador.

![[!DNL Channel Manager] en la vista Administración](assets/channel-manager-admin-view.png)

## Información general sobre la incorporación

1. [Instale el [!DNL Channel Manager] Extensión](install.md).

1. [Configure las variables [!DNL Commerce Services Connector]](connect.md) para integrar Channel Manager con la instancia de Commerce y otros servicios de soporte.

1. [Conecte su [!DNL Commerce] almacenar en [!DNL Walmart Marketplace]](connect.md).

1. [Configuración completa de la tienda](complete-store-setup.md).

## Requisitos previos

- Compruebe que dispone del [Requisitos previos de Walmart Marketplace](walmart-prerequisites.md) para integrarlo con el administrador de canales.

- **Información de la cuenta de comercio**-Descarga e instalación [!DNL Channel Manager] requiere un [Cuenta de comercio](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Necesita un ID de cuenta y credenciales con acceso de propietario o administrador a la variable [!DNL Adobe Commerce] o [!DNL Magento Open Source] instancia.

   - **ID DE MAGE**-[Iniciar sesión](https://account.magento.com/customer/account/login/) a la cuenta de comercio para obtener el ID de **[!UICONTROL My Account - Magento settings]**. Necesita este ID para registrarse para la variable [!DNL Channel Manager] programa beta del servicio.

      ![[!DNL MAGEID] en la configuración de la cuenta de comercio](assets/mageid-my-commerce-account.png)

   - **Teclas de acceso -** Obtenga claves de autenticación para descargar extensiones de comercio desde el repositorio de Commerce Composer `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      En proyectos de Adobe Commerce y Magento Open Source, el propietario puede configurar [Acceso compartido](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que los empleados y proveedores de servicios de confianza descarguen extensiones utilizando credenciales de la cuenta de propietario o titular de licencia.

      Activado [!DNL Adobe Commerce] en proyectos de infraestructura en la nube, los instaladores de software deben tener el siguiente acceso a la variable [!DNL Commerce] instancia:

      - Acceso de superusuario al proyecto de Cloud
      - Acceso de administrador a un entorno específico
      - an [!DNL Adobe Commerce] o [!DNL Magento Open Source] cuenta con permisos para acceder al repositorio del Compositor.

      Consulte [Administrar el acceso de los usuarios](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Autorización para descargar el paquete del Compositor de administrador de canales**-Proporcione el ID de MAGE de la cuenta de comercio utilizada para administrar el servicio al representante de Adobe que coordina el programa Beta para su organización.
- **Experiencia con el Compositor y el[!DNL Commerce CLI]** -Consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obtener información sobre el uso de estas herramientas para instalar y administrar extensiones en [!DNL Adobe Commerce] o [!DNL Magento Open Source] plataformas.
- **[Sales Channel de Amazon versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Si ha activado la Sales Channel de Amazon para sus sitios de comercio, compruebe que su plataforma de comercio tenga la versión 4.42 instalada antes de instalar el Administrador de canales.


### Requisitos

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Compositor 1.x o posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plataformas compatibles

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce local (EE) : 2.4.x
- Magento Open Source 2.4.x
