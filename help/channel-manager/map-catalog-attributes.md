---
title: Asignar atributos de catálogo
description: 'Asignar atributos para la coincidencia [DNL! productos de Commerce] a listados existentes de  [!DNL Walmart Marketplace] y sincronizando datos entre [!DNL Channel Manager] y [!DNL Walmart].'
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Asignar atributos de catálogo

Antes de conectar listados de [!DNL Commerce] a [!DNL Walmart Marketplace], debe asignar al menos un identificador único del catálogo [!DNL Commerce] al identificador correspondiente de Walmart.

Este paso es necesario para hacer coincidir [!DNL Commerce] productos con los listados de [!DNL Walmart] existentes y para sincronizar los datos de productos entre [!DNL Commerce] y [!DNL Walmart]. El producto [!DNL Commerce] debe tener al menos un atributo de producto que coincida con uno de los siguientes identificadores de producto (Id. de producto) requeridos por [!DNL Walmart].

**Se requieren [!DNL Walmart] ID de producto**

| **Tipo aceptado** | **Nombre** | **Propósito** | **Dígitos Aceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Elemento comercial global | Uso general, utilizado en todo el mundo | 14 dígitos |
| ISBN | Número de libro estándar internacional | Libros en rústica, tapa dura y electrónicos | 10 o 13 dígitos |
| ISSN | Número de serie estándar internacional | Número de serie de 8 dígitos utilizado para identificar revistas, diarios, periódicos y publicaciones periódicas de todo tipo entregadas en todos los medios impresos y electrónicos | 8 dígitos |
| UPC | Código de producto universal | Código de seguimiento comercial estándar | 12 dígitos |

Si el catálogo no tiene un atributo que coincida, [agregue o convierta un atributo de catálogo existente](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

## Asignar identificadores únicos

1. En la página **[!UICONTROL Listings]** o **[!UICONTROL Orders]** del almacén de canales de ventas, seleccione **[!UICONTROL Channel Settings]**.

1. El **[!UICONTROL Channel Settings]**, seleccione **[!UICONTROL Map Attributes]**.

   - Busque el atributo [!DNL Walmart Marketplace] que desea asignar.

   - Seleccione el atributo correspondiente del catálogo de la tienda [!DNL Commerce].

     El ejemplo siguiente asigna el atributo [!UICONTROL Walmart Marketplace UPC] al atributo UPC del catálogo de productos.

     ![Asignar atributos para los criterios de coincidencia de productos](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - Seleccione **[!UICONTROL Save]**.
