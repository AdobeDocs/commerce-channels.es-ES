---
title: A bordo [!DNL Channel Manager]
description: '''Conecte la instancia a [!DNL Channel Manager] al completar algunos pasos de incorporación."'
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# A bordo [!DNL Channel Manager]

Una vez completado el proceso de incorporación de Channel Manager, puede acceder, configurar y administrar las operaciones de ventas del canal de Walmart Marketplace desde Adobe Commerce. El Administrador de canales está disponible en [!UICONTROL Channel Manager] opción en la [!UICONTROL Commerce Admin Marketing] menú.

![[!DNL Channel Manager] opción en la vista de administración](assets/channel-manager-admin-view.png)

## Requisitos

Revise los requisitos para utilizar Channel Manager y recopile la información y las credenciales de cuenta necesarias para descargar, instalar y configurar la extensión de.

- **[Requisitos de Walmart Marketplace](walmart-requirements.md)**-Compruebe que cumple los requisitos para integrarse con Channel Manager, incluidos los siguientes [Configuración de tu cuenta de vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) y generando la clave de API para habilitar la integración.

- **Información de cuenta de Commerce**-Descarga e instalación [!DNL Channel Manager] requiere un [Cuenta de Commerce](https://docs.magento.com/user-guide/magento/magento-account.html){target="_blank"}. Necesita un ID de cuenta y credenciales con acceso de propietario o administrador a [!DNL Adobe Commerce] o [!DNL Magento Open Source] ejemplo.

   - **ID DE IMAGEN**-[Iniciar sesión](https://account.magento.com/customer/account/login/) a la [!DNL Commerce] cuenta de la que obtener el ID **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] el [!DNL Commerce] configuración de cuenta](assets/mageid-my-commerce-account.png)

   - **Claves de acceso-** Obtener claves de autenticación para descargar [!DNL Commerce] extensiones desde el [!DNL Commerce] Repositorio del compositor `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      En proyectos de Adobe Commerce y de Magento Open Source, el propietario puede configurar [Acceso compartido](https://docs.magento.com/user-guide/magento/magento-account-share.html) para permitir que los empleados de confianza y los proveedores de servicios descarguen extensiones mediante credenciales de la cuenta del propietario o titular de la licencia.

      Para [!DNL Adobe Commerce] en proyectos de infraestructura en la nube, los instaladores de software deben tener el siguiente acceso a la [!DNL Commerce] instancia:

      - Acceso de superusuario al proyecto de Cloud
      - Acceso de administrador a un entorno específico
      - un [!DNL Adobe Commerce] cuenta de con permisos de acceso al repositorio de Composer

      Consulte [Administrar el acceso de usuario](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Experiencia con Composer y el[!DNL Commerce CLI]**-Consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target="_blank"} para obtener información sobre el uso de estas herramientas para instalar y administrar extensiones en [!DNL Adobe Commerce] o [!DNL Magento Open Source] plataformas.

- **[[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene instalada la versión 4.4.2 o posterior antes de instalar [!DNL Channel Manager].

- **[!DNL Inventory Management]extensión para Adobe Commerce y Magento Open Source**

   Si tiene pensado utilizar Channel Manager para la gestión de inventario y pedidos, debe tener la extensión de Inventory management instalada y habilitada en la instancia de Adobe Commerce y de Magento Open Source. Normalmente, esta extensión se instala y habilita de forma predeterminada en Adobe Commerce y [!DNL Magento Open Source] 2.3.x y posterior.

   Si ha actualizado Commerce desde la versión 2.2.x o si ha desactivado Inventory management, actualice la instalación para incluir los módulos necesarios. Consulte [Instalación de Inventory management](https://devdocs.magento.com/extensions/inventory-management/) en la documentación para desarrolladores de Adobe Commerce.

### Requisitos del sistema

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x o posterior](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Si ha activado [!DNL Amazon Sales Channel] para su [!DNL Commerce] sitios, compruebe que su [!DNL Commerce] platform tiene instalada la versión 4.4.2 antes de instalar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### Plataformas compatibles

- Adobe Commerce en la nube (ECE) : 2.4.x
- Adobe Commerce local (EE) : 2.4.x
- Magento Open Source 2.4.x

## Pasos de incorporación

1. [Configurar tu cuenta de vendedor de Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Instale el [!DNL Channel Manager] extensión](install.md).

1. [Conectar con Commerce Services](connect.md) para integrar Channel Manager con la instancia de Commerce y otros servicios de soporte.

1. [Conecte su [!DNL Commerce] almacenar en [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Configuración completa de la tienda](complete-sales-channel-store-setup.md).
