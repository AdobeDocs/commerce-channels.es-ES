---
title: Asignar transportistas de envío
description: 'Asignar atributos para la coincidencia [DNL! Productos de [Commerce] a productos existentes [!DNL Walmart Marketplace] listados y sincronización de datos entre [!DNL Channel Manager] y [!DNL Walmart].'
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Asignar transportistas de envío

Antes de [procesar envíos de pedidos](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] pedidos, asigne a Walmart los transportistas preferidos al transportista correspondiente en [!DNL Commerce] para que los datos de envío se puedan sincronizar entre [!DNL Walmart] y [!DNL Commerce].

Los operadores de comercio que no se asignan a un operador preferido se etiquetan como *[!UICONTROL Other Carrier]* el [!DNL Walmart].

**Requisitos previos**

Antes de asignar transportistas de envío, complete las siguientes tareas:

1. Revise la [Métodos de transportista y prácticas recomendadas de envío para la entrega a tiempo](https://sellerhelp.walmart.com/s/guide?article=000009473) para [!DNL Walmart Marketplace].

1. Compruebe el [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) y [[!UICONTROL Shipping Settings]](https://docs.magento.com/user-guide/configuration/sales/shipping-settings.html) configuración en su [!DNL Commerce] almacene para asegurarse de que ha optimizado la configuración de para [!DNL Walmart Marketplace sales].

## Mapa de transportistas

1. Desde el **[!UICONTROL Listings]** o **[!UICONTROL Orders]** página, seleccione **[!UICONTROL Channel Settings]**.

1. Activado **[!UICONTROL Channel Settings]**, seleccione **[!UICONTROL Shipping Carriers]**.

   ![Mapa de transportistas](assets/map-shipping-carriers.png)

1. Para cada [!DNL Walmart] operador preferido de la lista, seleccione el [!DNL Commerce] nombre del operador en la lista desplegable si el operador está disponible.

1. Seleccionar **[!UICONTROL Save]** para aplicar la configuración.

