---
title: Incorporado [!DNL Channel Manager]
description: Conecte la instancia a la variable [!DNL Channel Manager] completando algunos pasos de integración.
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: e0b7f971f8eb4bc0827a7792ef94d88766adf82e
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---


# Incorporado [!DNL Channel Manager]

Administrador de canales integrado instalando la extensión del Administrador de canales en su [!DNL Commerce] y configurar conexiones de API. Estas conexiones permiten la comunicación y la sincronización de datos entre la instancia de Commerce y la [!DNL Walmart Marketplace].

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

      Para [!DNL Adobe Commerce] en proyectos de infraestructura en la nube, los instaladores de software deben tener el siguiente acceso a la variable [!DNL Commerce] instancia:

      - Acceso de superusuario al proyecto de Cloud
      - Acceso de administrador a un entorno específico
      - an [!DNL Adobe Commerce] o [!DNL Magento Open Source] cuenta con permisos para acceder al repositorio del Compositor

      Consulte [Administrar el acceso de los usuarios](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Autorización para descargar el paquete del Compositor de administrador de canales**-Proporcione al coordinador de Beta para el Canal de Adobe el ID MAGE del [!DNL Commerce] cuenta utilizada para administrar el servicio para su organización.
- **Experiencia con el Compositor y el[!DNL Commerce CLI]** -Consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obtener información sobre el uso de estas herramientas para instalar y administrar extensiones en [!DNL Adobe Commerce] o [!DNL Magento Open Source] plataformas.
- [[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)- Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene instalada la versión 4.42 antes de instalar [!DNL Channel Manager].
- [!DNL Inventory Management] extensión para Adobe Commerce y Magento Open Source

   Si planea utilizar el Administrador de canales para la gestión de inventario y pedidos, debe tener instalada y habilitada la extensión de Inventory management en la instancia de Adobe Commerce y Magento Open Source. Normalmente, esta extensión está instalada y habilitada de forma predeterminada en Adobe Commerce y Magento Open Source 2.3.x y posteriores. Para obtener más información, consulte [Instalación de Inventory management](https://devdocs.magento.com/extensions/inventory-management/) en la documentación para desarrolladores de Adobe Commerce.

### Requisitos

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Compositor 1.x o posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)- Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene instalada la versión 4.42 antes de instalar [!DNL Channel Manager].
- [!DNL Inventory Management]

### Plataformas compatibles

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce local (EE) : 2.4.x
- Magento Open Source 2.4.x
