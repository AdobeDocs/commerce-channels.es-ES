---
title: Asignar atributos de catálogo
description: 'Asignar atributos para la coincidencia [DNL! Productos de [Commerce] a productos existentes [!DNL Walmart Marketplace] listados y sincronización de datos entre [!DNL Channel Manager] y [!DNL Walmart].'
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Asignar atributos de catálogo

Antes de conectar anuncios de [!DNL Commerce] hasta [!DNL Walmart Marketplace], debe asignar al menos un identificador único de su [!DNL Commerce] al identificador correspondiente de Walmart.

Este paso es necesario para hacer coincidir [!DNL Commerce] productos a existentes [!DNL Walmart] listados y para sincronizar datos de producto entre [!DNL Commerce] y [!DNL Walmart]. El [!DNL Commerce] El producto debe tener al menos un atributo de producto que coincida con uno de los siguientes identificadores de producto (ID de producto) requeridos por [!DNL Walmart].

**Requerido [!DNL Walmart] ID de producto**

| **Tipo aceptado** | **Nombre** | **Finalidad** | **Dígitos aceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Elemento comercial global | Uso general, utilizado en todo el mundo | 14 dígitos |
| ISBN | Número de libro estándar internacional | Libros en rústica, tapa dura y electrónicos | 10 o 13 dígitos |
| ISSN | Número de serie estándar internacional | Número de serie de 8 dígitos utilizado para identificar revistas, diarios, periódicos y publicaciones periódicas de todo tipo entregadas en todos los medios impresos y electrónicos | 8 dígitos |
| UPC | Código de producto universal | Código de seguimiento comercial estándar | 12 dígitos |

Si el catálogo no tiene un atributo que coincida, [añadir o convertir un atributo de catálogo existente](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Asignar identificadores únicos

1. Desde el **[!UICONTROL Listings]** o **[!UICONTROL Orders]** para la tienda de canales de ventas, seleccione **[!UICONTROL Channel Settings]**.

1. Activado **[!UICONTROL Channel Settings]**, seleccione **[!UICONTROL Map Attributes]**.

   - Busque el [!DNL Walmart Marketplace] atributo para asignar.

   - Seleccione el atributo correspondiente de la [!DNL Commerce] catálogo de la tienda.

      El siguiente ejemplo asigna el [!UICONTROL Walmart Marketplace UPC] al atributo UPC del catálogo de productos.

      ![Asignar atributos para criterios de coincidencia de productos](assets/products-map-attributes-for-match.png)

   - Seleccionar **[!UICONTROL Save]**.
