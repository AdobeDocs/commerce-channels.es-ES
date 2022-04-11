---
title: Configurar la coincidencia de productos
description: Asignar atributos para hacer coincidir productos de Commerce con anuncios de Walmart Marketplace existentes
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Configurar la coincidencia de productos

Antes de publicar la lista en Walmart Marketplace, asigne al menos un identificador único de sus atributos de catálogo de productos a uno de los identificadores de producto Walmart requeridos. Este paso es necesario para hacer coincidir productos en el mercado Walmart.

Para la coincidencia de productos, el producto Commerce debe tener al menos uno de los siguientes identificadores de producto (ID de producto) en los atributos del catálogo.

**ID de producto Walmart requeridos**

| **Tipo aceptado** | **Nombre** | **Objetivo** | **Dígitos aceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Artículo comercial global | Objetivo general, usado en todo el mundo | 14 dígitos |
| ISBN | Número de Libro Estándar Internacional | Libros de papel, tapa dura y electrónica | 10 o 13 dígitos |
| ISSN | Número de serie estándar internacional | Número de serie de 8 dígitos utilizado para identificar revistas, revistas, periódicos y periódicos de todo tipo entregados en todos los medios impresos y electrónicos | 8 dígitos |
| ISBN | Número de Libro Estándar Internacional | Papel, tapa dura y electrónico | 12 dígitos |

Si tiene un tipo diferente de atributo de ID de producto en el catálogo, conviértalo en uno de los tipos necesarios. A continuación, asígnelo al atributo correspondiente de Walmart Marketplace en la configuración de Listing para la tienda de Channel Manager.

## Configuración de atributos del producto

1. En el [!UICONTROL Listings] para el canal de ventas conectado, seleccione uno o varios productos en *Borrador* estado.

1. Select **[!UICONTROL Settings]**.

   - Busque el atributo de Walmart Marketplace para asignar.

   - Seleccione el atributo correspondiente del catálogo de tiendas.

      El siguiente ejemplo asigna el atributo UPC de Walmart Marketplace al atributo UPC del catálogo de productos.
   ![Asignar atributos para los criterios de coincidencia de producto](assets/products-map-attributes-for--match.png)

   - Select **[!UICONTROL Save]**.


## Actualizar la configuración de atributos asignados

Cambie el identificador de producto de Comercio para productos coincidentes actualizando la configuración de atributo asignada.

Por ejemplo, en lugar de buscar productos coincidentes basados en el código de atributo de producto UPC de comercio, puede hacer coincidir basándose en el SKU. O bien, asigne atributos adicionales para mejorar la coincidencia.

1. En el **[!UICONTROL Listings]**, seleccione **[!UICONTROL Settings]**.

1. En el formulario Asignar atributo , cambie la configuración de atributo asignada según sea necesario.
