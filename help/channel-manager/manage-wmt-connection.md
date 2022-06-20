---
title: Administrar la conexión de Walmart
description: Actualice las credenciales de la API para autorizar la conexión entre [DNL! Commerce] vista de tienda y [!DNL Walmart Marketplace]. La conexión es necesaria para conectar las listas de productos de Commerce y sincronizar los datos de inventario, precio, pedido y envío entre Commerce y Walmart.
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Asignación de transportistas

Antes de [procesar envíos de pedidos](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] pedidos, asigne los transportistas preferidos de Walmart a los transportistas correspondientes en [!DNL Commerce] para que los datos de envío se puedan sincronizar entre [!DNL Walmart] y [!DNL Commerce].

Los operadores de comercio que no se asignan a un operador preferido están etiquetados como *[!UICONTROL Other Carrier]* en [!DNL Walmart].

**Requisitos previos**

Consulte [Requisitos de Walmart](walmart-requirements.md) para el [!DNL Marketplace Seller account].

## Actualizar credenciales de conexión

1. En el [!UICONTROL Listings] para el almacén de canales de ventas, seleccione **[!UICONTROL Channel Settings]**.

1. Activado **[!UICONTROL Channel Settings]**, seleccione **[!UICONTROL Walmart Connection]**.

1. Para modificar las credenciales, seleccione **[!UICONTROL Change Credentials]**

   ![Actualizar las credenciales de la API Walmart para autorizar la conexión](assets/update-connection-credentials.png)

1. Introduzca la variable **[!UICONTROL Walmart Client ID]** y **[!UICONTROL Walmart Client Secret]**.

1. Select **[!UICONTROL Save]** para aplicar la configuración.
