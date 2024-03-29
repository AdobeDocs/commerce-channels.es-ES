---
title: Información general de configuración
description: 'Obtenga información acerca de [!DNL Channel Manager settings] para configurar la autenticación y asignar los atributos del catálogo de productos y los transportistas necesarios para coordinar las operaciones de ventas entre [!DNL Commerce] y el [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Información general de configuración

La configuración del canal de ventas permite la comunicación y la sincronización de datos entre [!DNL Commerce] y [!DNL Walmart Marketplace] para que pueda administrar [!DNL Walmart Marketplace] operaciones de ventas desde [!DNL Commerce] Administrador.

Entrada [!DNL Channel Manager], puede configurar algunos canales de ventas durante el proceso de incorporación. Después de la incorporación, puede ver y administrar la configuración seleccionando **[!UICONTROL Channel Settings]** desde el [!UICONTROL Listings] y [!UICONTROL Orders] paneles.

* **[Conexión de Walmart](manage-wmt-connection.md)**-Durante el [!DNL Channel Manager] proceso de incorporación, debe proporcionar [Credenciales de API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de su [!DNL Walmart Marketplace] Cuenta de vendedor para conectar [!DNL Commerce] hasta [!DNL Walmart Marketplace] para la comunicación y la sincronización de datos. Si es necesario, puede actualizar estas credenciales desde el *Configuración de canal* página.

* **[Asignar identificadores únicos](map-catalog-attributes.md)**- Antes de conectar anuncios de [!DNL Commerce] hasta [!DNL Walmart Marketplace], asigne al menos un identificador único de su [!DNL Commerce] al identificador correspondiente de Walmart. Este paso es necesario para hacer coincidir [!DNL Commerce] productos a existentes [!DNL Walmart] listados y para sincronizar datos de producto entre [!DNL Commerce] y [!DNL Walmart].

* **[Asignar transportistas de envío](map-shipping-carriers.md)**-Antes de procesar [!DNL Walmart Marketplace] pedidos de [!DNL Commerce], asegúrese de asignar los transportistas desde su [!DNL Commerce] a los operadores correspondientes en [!DNL Walmart Marketplace].
