---
title: Administrar conexión de Walmart Marketplace
description: 'Actualice las credenciales de la API para autorizar la conexión entre un [DNL! Commerce] almacena la vista y los  [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] listados de productos y sincroniza los datos de inventario, precio, pedido y envío entre [!DNL Commerce] y Walmart.'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Asignar transportistas de envío

Antes de [procesar envíos de pedidos](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] pedidos, asigne los transportistas preferidos de Walmart al transportista correspondiente en [!DNL Commerce] para que los datos de envío se puedan sincronizar entre [!DNL Walmart] y [!DNL Commerce].

Los operadores de Commerce que no se asignan a un operador preferido se etiquetan como *[!UICONTROL Other Carrier]* en [!DNL Walmart].

**Requisitos previos**

Revise [Requisitos de Walmart](walmart-requirements.md) para [!DNL Marketplace Seller account].

## Actualizar credenciales de conexión

1. En la página [!UICONTROL Listings] del almacén de canales de ventas, seleccione **[!UICONTROL Channel Settings]**.

1. El **[!UICONTROL Channel Settings]**, seleccione **[!UICONTROL Walmart Connection]**.

1. Para modificar las credenciales, seleccione **[!UICONTROL Change Credentials]**

   ![Actualizar credenciales de la API de Walmart para autorizar la conexión](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. Escriba **[!UICONTROL Walmart Client ID]** y **[!UICONTROL Walmart Client Secret]**.

1. Seleccione **[!UICONTROL Save]** para aplicar la configuración.
