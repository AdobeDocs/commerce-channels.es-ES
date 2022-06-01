---
title: Asignación de transportistas
description: Asignar atributos para la coincidencia [DNL! Productos de Commerce] para [!DNL Walmart Marketplace] anuncios y sincronización de datos entre [!DNL Channel Manager] y [!DNL Walmart].
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Asignación de transportistas

Antes de [procesar envíos de pedidos](process-orders.md#ship-an-order) para [!DNL Walmart Marketplace] pedidos, asigne los transportistas preferidos de Walmart a los transportistas correspondientes en [!DNL Commerce] para que los datos de envío se puedan sincronizar entre [!DNL Walmart] y [!DNL Commerce].

Los operadores de comercio que no se asignan a un operador preferido están etiquetados como *[!UICONTROL Other Carrier]* en [!DNL Walmart].

**Requisitos previos**

Antes de asignar transportistas, complete las siguientes tareas:

1. Consulte la [Métodos de operador de telefonía móvil y prácticas recomendadas de envío para entregas a tiempo](https://sellerhelp.walmart.com/s/guide?article=000009473) para [!DNL Walmart Marketplace].

1. Compruebe el [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) y [[!UICONTROL Shipping Settings]](https://docs.magento.com/user-guide/configuration/sales/shipping-settings.html) configuración de [!DNL Commerce] almacenar para asegurarse de que ha optimizado la configuración para [!DNL Walmart Marketplace sales].

## Asignación de transportistas

1. En el [!UICONTROL Listings] para el almacén de canales de ventas, seleccione **[!UICONTROL Settings]**.

1. De **[!UICONTROL Map Attributes]**, seleccione **[!UICONTROL Shipping Carriers]**.

   ![Asignación de transportistas](assets/map-shipping-carriers.png)

1. Para cada [!DNL Walmart] operador preferido enumerado, seleccione [!DNL Commerce] nombre del operador de la lista desplegable si el operador está disponible.

1. Select **[!UICONTROL Save]** para aplicar la configuración.
