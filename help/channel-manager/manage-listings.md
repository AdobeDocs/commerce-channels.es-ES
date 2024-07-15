---
title: Administrar anuncios
description: '"Administre los listados de canales de ventas de una tienda  [!DNL Commerce] con el Administrador de canales para Adobe Commerce y el Magento Open Source".'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Administrar anuncios

Administrar listados de productos para el canal de ventas [!DNL Walmart Marketplace] desde la interfaz de usuario de Channel Manager.

El estado de un listado individual indica dónde se encuentra el producto en el flujo de trabajo [!DNL Channel Manager] para que pueda determinar los pasos siguientes y resolver los errores.

![Página de anuncios para un canal de ventas conectado](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

Puede completar las tareas siguientes desde la vista Listado.

* Ver anuncios actuales
* Ordenar y filtrar los anuncios
* Añadir productos
* Hacer coincidir productos
* Seguimiento del estado del anuncio
* Revisar la descripción del error de los anuncios con estado de error

## Ver listados de productos

1. Desde el administrador, vaya a [!UICONTROL **Marketing** > **Administrador de canales**].

1. En la lista Tienda, seleccione el icono en forma de ojo de una fila de entrada de tienda para abrir la vista de la tienda.

1. Seleccionar [!UICONTROL **anuncios**].

1. Ordene la vista *Listing* seleccionando cualquier encabezado de columna en la tabla *Listing*.

1. Filtra la vista *Listing* seleccionando una de las tarjetas de recuento de estados.

1. Restablezca el criterio de ordenación y quite filtros seleccionando **Actualizar productos**.

## Agregar productos de [!DNL Commerce] al Administrador de canales

Cree el surtido de productos para el canal [!DNL Walmart Marketplace] realizando las siguientes tareas:

* [Agregar productos de su  [!DNL Commerce] catálogo de productos a [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Asignar atributos de catálogo](map-catalog-attributes.md#configure-product-attribute-settings)

## Hacer coincidir productos en [!DNL Walmart]

Puede crear ofertas de productos en [!DNL Walmart Marketplace] mediante la coincidencia de productos o cargando manualmente listados de productos para nuevos productos.

* **[Igualar productos en Walmart](connect-listings-to-marketplace.md)**: conecta anuncios de productos de tu canal a [!DNL Walmart Marketplace] actualizando los anuncios existentes que venden el mismo producto. Los criterios de coincidencia están determinados por la [configuración de asignación de atributos](map-catalog-attributes.md) para su canal.

* **[Cargar manualmente nuevos listados](connect-listings-to-marketplace.md#upload-new-product-listings)**: para los productos que no coinciden con un listado existente en [!DNL Walmart Marketplace], use una plantilla de Excel de categoría de producto [!DNL Walmart] para cargar listados de productos en lotes.

## Controles de lista y descripciones de columna

Las tablas siguientes describen los controles y las columnas disponibles para [!UICONTROL Listings].

**Controles para[!UICONTROL Listings]**

| **Control** | **Descripción** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Abre la página [!UICONTROL Admin Product Catalog] para seleccionar productos que se agregarán a su selección de [!DNL Walmart Marketplace], o para actualizar los atributos de los productos a fin de que cumplan los requisitos de las listas de Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Después de seleccionar uno o más productos en estado [!UICONTROL Draft], seleccione [!UICONTROL Match products on Walmart] para buscar ofertas de productos que se puedan agregar a un listado de [!DNL Walmart Marketplace] existente. |
| [!UICONTROL Refresh products] | Actualice la pantalla con el anuncio y el estado más actuales. Este control también restablece la vista de listado al orden predeterminado y elimina los filtros. |
| [!UICONTROL Filter by *Estado*] | Mostrar sólo anuncios con un estado específico seleccionando una de las tarjetas de estado encima de la tabla Listado. Elimine el filtro seleccionando **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | Cambie el criterio de ordenación de los listados seleccionando cualquier encabezado de columna. |


**Descripciones de columna**

| **Campo** | **Descripción** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nombre del producto del catálogo de tienda [!DNL Commerce]. |
| [!UICONTROL SKU (Unique ID)] | El SKU asignado al producto en el catálogo [!DNL Commerce]. |
| [!UICONTROL  Quantity] | Cantidad de inventario disponible en Adobe Commerce o Magento Open Source. |
| [!UICONTROL Price] | El precio del producto del catálogo de la tienda [!DNL Commerce]. Las actualizaciones de precios de catálogo se sincronizan con el Administrador de canales y luego se envían a [!DNL Walmart Marketplace] para que los artículos enumerados muestren el precio actual. |
| [!UICONTROL Status] | Indica el estado de pedido actual en el flujo de trabajo de pedido [!DNL Commerce]. El estado se actualiza cuando se agregan correctamente productos a [!DNL Channel Manager] y cuando coinciden los productos en el mercado. Si falla una operación, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |
| [!UICONTROL Error Description] | Proporciona información de error adicional para productos con un estado `[!DNL Error]`. |

### Acerca del estado del anuncio

En el área de trabajo Lista, la etiqueta Estado muestra dónde se encuentra un producto en el flujo de trabajo [!DNL Channel Manager] para que pueda determinar los pasos siguientes y resolver errores. Los anuncios pueden tener las siguientes etiquetas de estado:

* **[!UICONTROL Draft]**: identifica los productos que no se han [enviado a [!DNL Walmart] para que coincidan](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**: identifica los productos enviados para su coincidencia en [!DNL Walmart Marketplace]. Los productos permanecen en estado *Procesando* hasta que [!DNL Walmart] devuelve un mensaje de estado HTTP que indica si la coincidencia se realizó correctamente o si hubo un error. La operación de coincidencia puede tardar hasta 30 minutos en completarse el [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**: identifica los productos que se encontraron correctamente en [!DNL Walmart].

  Se produce una coincidencia cuando el valor de atributo del producto (código UPC por ejemplo) coincide con el valor UPC de un listado de [!DNL Walmart Marketplace] existente. Cuando un producto coincide, la oferta de productos de Commerce se agrega al listado existente.

  Consulte el panel [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) para revisar la lista de productos actualizada y verificar los detalles del producto, el precio y la cantidad de inventario.

* **[!UICONTROL Match - Match in Stage]**: identifica los productos coincidentes en [!DNL Walmart] que no pueden conectarse hasta que el almacén de [!DNL Walmart Marketplace] esté activo. Los productos con este estado se conectan automáticamente cuando se activa la tienda [!DNL Walmart Marketplace].

* **[!UICONTROL Error]**: identifica los productos que no coinciden con un listado de [!DNL Walmart Marketplace] existente.

* **[!UICONTROL Error description]**: proporciona información detallada sobre el error de listado.

  Una vez resuelto el error, vuelva a enviar el producto para que coincida. Ver [Solucionar errores de coincidencia de productos](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
