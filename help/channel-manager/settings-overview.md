---
title: Información general de configuración
description: 'Obtenga información acerca de [!DNL Channel Manager settings] para configurar la autenticación y asignar los atributos del catálogo de productos y los transportistas necesarios para coordinar las operaciones de ventas entre [!DNL Commerce] y [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Información general de configuración

La configuración del canal de ventas habilita la comunicación y la sincronización de datos entre [!DNL Commerce] y [!DNL Walmart Marketplace] para que pueda administrar [!DNL Walmart Marketplace] operaciones de ventas desde el administrador de [!DNL Commerce].

En [!DNL Channel Manager], puede configurar algunos canales de ventas durante el proceso de incorporación. Después de la incorporación, puede ver y administrar la configuración seleccionando **[!UICONTROL Channel Settings]** en los paneles de [!UICONTROL Listings] y [!UICONTROL Orders].

* **[Conexión de Walmart](manage-wmt-connection.md)**: durante el proceso de incorporación de [!DNL Channel Manager], proporciona [credenciales de API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) desde su cuenta de vendedor de [!DNL Walmart Marketplace] para conectar [!DNL Commerce] a [!DNL Walmart Marketplace] para la comunicación y la sincronización de datos. Si es necesario, puede actualizar estas credenciales desde la página *Configuración de canal*.

* **[Asignar identificadores únicos](map-catalog-attributes.md)**-Antes de conectar listados de [!DNL Commerce] a [!DNL Walmart Marketplace], asigne al menos un identificador único de su catálogo [!DNL Commerce] al identificador correspondiente de Walmart. Este paso es necesario para hacer coincidir [!DNL Commerce] productos con los listados de [!DNL Walmart] existentes y para sincronizar los datos de productos entre [!DNL Commerce] y [!DNL Walmart].

* **[Asignar transportistas de envío](map-shipping-carriers.md)**-Antes de procesar [!DNL Walmart Marketplace] pedidos de [!DNL Commerce], asegúrese de asignar transportistas de envío de su instancia de [!DNL Commerce] a los transportistas correspondientes en [!DNL Walmart Marketplace].
