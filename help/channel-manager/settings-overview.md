---
title: Información general sobre la configuración
description: '"Obtenga información sobre [!DNL Channel Manager settings] para configurar la autenticación y asignar los atributos del catálogo de productos y los transportistas necesarios para coordinar las operaciones de venta entre [!DNL Commerce] y [!DNL Walmart Marketplace]"'
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 638ba8c595652e66aa5f15f5207855c6d2b872d7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Información general sobre la configuración

La configuración del canal de ventas permite la comunicación y la sincronización de datos entre [!DNL Commerce] y [!DNL Walmart Marketplace] para que pueda administrar [!DNL Walmart Marketplace] operaciones de venta de [!DNL Commerce] Administrador.

En [!DNL Channel Manager], se configuran algunos canales de ventas durante el proceso de incorporación. Después de la incorporación, puede ver y administrar la configuración seleccionando **[!UICONTROL Channel Settings]** de la variable [!UICONTROL Listings] y [!UICONTROL Orders] tableros.

* **[Conexión Walmart](manage-wmt-connection.md)**-Durante el [!DNL Channel Manager] proceso de incorporación, proporcione [Credenciales de API](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de su [!DNL Walmart Marketplace] Cuenta de vendedor para conectar [!DNL Commerce] a [!DNL Walmart Marketplace] para la comunicación y la sincronización de datos. Si es necesario, puede actualizar estas credenciales desde el *Configuración de canal* página.

* **[Asignar identificadores únicos](map-catalog-attributes.md)**-Antes de conectar anuncios desde [!DNL Commerce] a [!DNL Walmart Marketplace], asigne al menos un identificador único de su [!DNL Commerce] catálogo con el identificador correspondiente de Walmart. Este paso es necesario para que coincida con [!DNL Commerce] productos a [!DNL Walmart] anuncios y para sincronizar datos de productos entre [!DNL Commerce] y [!DNL Walmart].

* **[Asignar transportistas de envío](map-shipping-carriers.md)**-Antes de procesar [!DNL Walmart Marketplace] pedidos de [!DNL Commerce], asegúrese de asignar los transportistas desde su [!DNL Commerce] a los operadores correspondientes en [!DNL Walmart Marketplace].
