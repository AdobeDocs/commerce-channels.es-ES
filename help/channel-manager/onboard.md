---
title: Incorporado [!DNL Channel Manager]
description: 'Conecte la instancia al servicio  [!DNL Channel Manager] completando algunos pasos de incorporación.'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Incorporar [!DNL Channel Manager]

Una vez completado el proceso de incorporación de Channel Manager, puede acceder, configurar y administrar las operaciones de ventas del canal de Walmart Marketplace desde Adobe Commerce. Channel Manager está disponible en la opción [!UICONTROL Channel Manager] del menú [!UICONTROL Commerce Admin Marketing].

Opción ![[!DNL Channel Manager] en la vista de administración ](assets/channel-manager-admin-view.png){width="500"}

## Requisitos

Revise los requisitos para utilizar Channel Manager y recopile la información y las credenciales de cuenta necesarias para descargar, instalar y configurar la extensión de.

- **[Requisitos de Walmart Marketplace](walmart-requirements.md)**: compruebe que cumple los requisitos para integrarse con Channel Manager, incluido [configurar su cuenta de vendedor](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) y generar la clave de API para habilitar la integración.

- **La descarga e instalación de [!DNL Channel Manager] de información de cuenta de Commerce** requiere una [cuenta de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Necesita un identificador de cuenta y credenciales con acceso de propietario o administrador para la instancia [!DNL Adobe Commerce] o [!DNL Magento Open Source].

   - **ID de MAGE**-[Inicia sesión](https://account.magento.com/customer/account/login/) en la cuenta de [!DNL Commerce] para obtener el ID de **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] en [!DNL Commerce] configuración de cuenta](assets/mageid-my-commerce-account.png){width="250"}

   - **Claves de acceso-** Obtenga claves de autenticación para descargar las extensiones [!DNL Commerce] del repositorio del Compositor [!DNL Commerce] (repositorio `([!DNL repo.magento.com]`).

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     En proyectos de Adobe Commerce y Magento Open Source, el propietario puede configurar [Acceso compartido](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) para permitir que los empleados y proveedores de servicios de confianza descarguen extensiones con las credenciales de la cuenta Propietario o Titular de licencia.

     Para [!DNL Adobe Commerce] en proyectos de infraestructura en la nube, los instaladores de software deben tener el siguiente acceso a la instancia [!DNL Commerce]:

      - Acceso de superusuario al proyecto de Cloud
      - Acceso de administrador a un entorno específico
      - una cuenta de [!DNL Adobe Commerce] con permisos para acceder al repositorio de Composer

     Consulte [Administrar el acceso de los usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) en la *Guía de Commerce en la infraestructura de la nube*.

- **Experiencia con el Compositor y[!DNL Commerce CLI]**: vea [Instalar una extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) en la *Guía de instalación* para obtener información acerca del uso de estas herramientas para instalar y administrar extensiones en plataformas [!DNL Adobe Commerce] o [!DNL Magento Open Source].

- **[[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Si activó [!DNL Amazon Sales Channel] para sus sitios de [!DNL Commerce], compruebe que su plataforma de [!DNL Commerce] tenga instalada la versión 4.4.2 o posterior antes de instalar [!DNL Channel Manager].

- Extensión **[!DNL Inventory Management]para Adobe Commerce y Magento Open Source**

  Si tiene pensado utilizar Channel Manager para la gestión de inventario y pedidos, debe tener la extensión de Inventory management instalada y habilitada en la instancia de Adobe Commerce y de Magento Open Source. Normalmente, esta extensión se instala y habilita de forma predeterminada en Adobe Commerce y [!DNL Magento Open Source] 2.3.x y versiones posteriores.

  Si ha actualizado Commerce desde la versión 2.2.x o si ha desactivado Inventory management, actualice la instalación para incluir los módulos necesarios. Consulte [Instalar Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) en la *Guía de Inventory management*.

### Requisitos del sistema

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Compositor 1.x o posterior](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] versión 4.4.2 o posterior](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Si ha activado [!DNL Amazon Sales Channel] para sus sitios [!DNL Commerce], compruebe que su plataforma [!DNL Commerce] tenga instalada la versión 4.4.2 antes de instalar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plataformas compatibles

- Adobe Commerce en la nube (ECE) : 2.4.x
- Adobe Commerce local (EE) : 2.4.x
- Magento Open Source 2.4.x

## Pasos de incorporación

1. [Configura tu cuenta de vendedor de Walmart](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Instale la [!DNL Channel Manager] extensión](install.md).

1. [Conéctese a los servicios de Commerce](connect.md) para integrar Channel Manager con la instancia de Commerce y otros servicios de soporte.

1. [Conecta tu tienda [!DNL Commerce] a [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Configuración completa del almacén](complete-sales-channel-store-setup.md).
