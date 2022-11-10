---
title: Incorporado [!DNL Channel Manager]
description: '"Conecte la instancia a la variable [!DNL Channel Manager] completando algunos pasos de integración".'
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 738c48b8b8075e7c8bbf883c58cc8de39bca355c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# Incorporado [!DNL Channel Manager]

Una vez completado el proceso de incorporación de Channel Manager, puede acceder, configurar y administrar las operaciones de ventas de canal de Walmart Marketplace desde Adobe Commerce. El Administrador de canales está disponible en el [!UICONTROL Channel Manager] en la [!UICONTROL Commerce Admin Marketing] para abrir el Navegador.

![[!DNL Channel Manager] en la vista Administración](assets/channel-manager-admin-view.png)

## Requisitos

Revise los requisitos para utilizar el administrador de canales y recopile la información de cuenta y las credenciales necesarias para descargar, instalar y configurar la extensión.

- **[Requisitos de Walmart Marketplace](walmart-requirements.md)**-Compruebe que cumple los requisitos para la integración con el Administrador de canales, incluido [configuración de la cuenta de vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) y generación de la clave de API para habilitar la integración.

- **Información de la cuenta de comercio**-Descarga e instalación [!DNL Channel Manager] requiere un [Cuenta de comercio](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Necesita un ID de cuenta y credenciales con acceso de propietario o administrador a la variable [!DNL Adobe Commerce] o [!DNL Magento Open Source] instancia.

   - **ID DE MAGE**-[Iniciar sesión](https://account.magento.com/customer/account/login/) a [!DNL Commerce] cuenta para obtener el ID de **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] en [!DNL Commerce] configuración de la cuenta](assets/mageid-my-commerce-account.png)

   - **Teclas de acceso -** Obtener claves de autenticación para descargar [!DNL Commerce] las extensiones de [!DNL Commerce] Repositorio de compositores `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      En proyectos de Adobe Commerce y Magento Open Source, el propietario puede configurar [Acceso compartido](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que los empleados y proveedores de servicios de confianza descarguen extensiones utilizando credenciales de la cuenta de propietario o titular de licencia.

      Para [!DNL Adobe Commerce] en proyectos de infraestructura en la nube, los instaladores de software deben tener el siguiente acceso a la variable [!DNL Commerce] instancia:

      - Acceso de superusuario al proyecto de Cloud
      - Acceso de administrador a un entorno específico
      - an [!DNL Adobe Commerce] cuenta con permisos para acceder al repositorio del Compositor

      Consulte [Administrar el acceso de los usuarios](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Experiencia con el Compositor y el[!DNL Commerce CLI]**-Consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} para obtener información sobre el uso de estas herramientas para instalar y administrar extensiones en [!DNL Adobe Commerce] o [!DNL Magento Open Source] plataformas.

- **[[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**- Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene instalada la versión 4.4.2 o posterior antes de instalar [!DNL Channel Manager].

- **[!DNL Inventory Management]extensión para Adobe Commerce y Magento Open Source**

   Si planea utilizar el Administrador de canales para la gestión de inventario y pedidos, debe tener instalada y habilitada la extensión de Inventory management en la instancia de Adobe Commerce y Magento Open Source. Normalmente, esta extensión está instalada y habilitada de forma predeterminada en Adobe Commerce y [!DNL Magento Open Source] 2.3.x y posteriores.

   Si ha actualizado Commerce desde 2.2.x, o si ha deshabilitado Inventory management, actualice la instalación para incluir los módulos necesarios. Consulte [Instalación de Inventory management](https://devdocs.magento.com/extensions/inventory-management/) en la documentación para desarrolladores de Adobe Commerce.

### Requisitos del sistema

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Compositor 1.x o posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)- Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene la versión 4.4.2 instalada antes de instalar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### Plataformas compatibles

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce local (EE) : 2.4.x
- Magento Open Source 2.4.x

## Pasos de incorporación

1. [Configure su cuenta de vendedor de Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Instale el [!DNL Channel Manager] Extensión](install.md).

1. [Conectarse a Commerce Services](connect.md) para integrar Channel Manager con la instancia de Commerce y otros servicios de soporte.

1. [Conecte su [!DNL Commerce] almacenar en [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Configuración completa de la tienda](complete-sales-channel-store-setup.md).
