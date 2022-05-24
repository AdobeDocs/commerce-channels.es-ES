---
title: Asignar atributos de catálogo
description: Asignar atributos para la coincidencia [DNL! Productos de Commerce] para [!DNL Walmart Marketplace] anuncios y sincronización de datos entre [!DNL Channel Manager] y [!DNL Walmart].
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: fac4bbd3985e07b919f986c877b8584da797e6fe
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Asignar atributos de catálogo

Antes de publicar anuncios de [!DNL Commerce] a [!DNL Walmart Marketplace], debe asignar al menos un identificador único del [!DNL Commerce] catálogo con el identificador correspondiente de Walmart.
Este paso es necesario para que coincida con [!DNL Commerce] productos a [!DNL Walmart] anuncios y para sincronizar datos de productos entre [!DNL Commerce] y [!DNL Walmart].

Para la coincidencia de productos, el producto Commerce debe tener al menos un atributo de producto que coincida con uno de los siguientes identificadores de producto (ID de producto) requeridos por [!DNL Walmart].

**ID de producto Walmart requeridos**

| **Tipo aceptado** | **Nombre** | **Objetivo** | **Dígitos aceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Artículo comercial global | Objetivo general, usado en todo el mundo | 14 dígitos |
| ISBN | Número de Libro Estándar Internacional | Libros de papel, tapa dura y electrónica | 10 o 13 dígitos |
| ISSN | Número de serie estándar internacional | Número de serie de 8 dígitos utilizado para identificar revistas, revistas, periódicos y periódicos de todo tipo entregados en todos los medios impresos y electrónicos | 8 dígitos |
| UPC | Código de producto universal | Código de seguimiento comercial estándar | 12 dígitos |

Si el catálogo no tiene un atributo coincidente, [agregar o convertir un atributo de catálogo existente](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Asignación de identificadores únicos

1. En el [!UICONTROL Listings] para el almacén de canales de ventas, seleccione **[!UICONTROL Settings]**.

   - Busque el atributo de Walmart Marketplace para asignar.

   - Seleccione el atributo correspondiente en la [!DNL Commerce] catálogo de tiendas.

      El siguiente ejemplo asigna el atributo UPC de Walmart Marketplace al atributo UPC del catálogo de productos.
   ![Asignar atributos para los criterios de coincidencia de producto](assets/products-map-attributes-for-match.png)
   - De forma opcional, puede asignar varios atributos para aumentar las coincidencias. Si asigna más de un atributo, seleccione uno como **Identificador principal**. Esta

   - Select **[!UICONTROL Save]**.


## Actualizar la configuración de atributos asignados

Cambie el identificador de producto de Comercio para productos coincidentes actualizando la configuración de atributo asignada.

Por ejemplo, en lugar de buscar productos coincidentes basados en el código de atributo de producto UPC de comercio, puede hacer coincidir basándose en el SKU. O bien, asigne atributos adicionales para mejorar la coincidencia.

1. En el **[!UICONTROL Listings]**, seleccione **[!UICONTROL Settings]**.

1. En el formulario Asignar atributo , cambie la configuración de atributo asignada según sea necesario.
