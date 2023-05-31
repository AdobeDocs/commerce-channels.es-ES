---
title: Administrar anuncios
description: '''Administrar listados de canales de ventas para un [!DNL Commerce] Almacenar con Channel Manager para Adobe Commerce y Magento Open Source."'
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Administrar anuncios

Administrar listados de productos para [!DNL Walmart Marketplace] canal de ventas desde la interfaz de usuario de Channel Manager.

El estado de una lista individual indica dónde se encuentra el producto en la [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver los errores.

![Página de listados de un canal de ventas conectado](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

Puede completar las tareas siguientes desde la vista Listado.

* Ver anuncios actuales
* Ordenar y filtrar los anuncios
* Añadir productos
* Hacer coincidir productos
* Seguimiento del estado del anuncio
* Revisar la descripción del error de los anuncios con estado de error

## Ver listados de productos

1. Desde Admin, vaya a [!UICONTROL **Marketing** > **Administrador de canales**].

1. En la lista Tienda, seleccione el icono en forma de ojo de una fila de entrada de tienda para abrir la vista de la tienda.

1. Seleccionar [!UICONTROL **Anuncios**].

1. Ordene los *Listado* ver seleccionando cualquier encabezado de columna en la *Listado* tabla.

1. Filtrar el *Listado* para ver, seleccione una de las tarjetas de recuento de estado.

1. Restablezca el criterio de ordenación y elimine los filtros seleccionando **Actualizar productos**.

## Añadir [!DNL Commerce] productos a Channel Manager

Cree el surtido de productos para [!DNL Walmart Marketplace] al completar las tareas siguientes:

* [Añadir productos de su [!DNL Commerce] catálogo de productos a [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Asignar atributos de catálogo](map-catalog-attributes.md#configure-product-attribute-settings)

## Hacer coincidir productos en [!DNL Walmart]

Puede crear ofertas de productos en [!DNL Walmart Marketplace] usando la coincidencia de productos o cargando manualmente listas de productos para nuevos productos.

* **[Igualar productos en Walmart](connect-listings-to-marketplace.md)**: permite conectar las listas de productos del canal a [!DNL Walmart Marketplace] actualizando los anuncios existentes que venden el mismo producto. Los criterios de coincidencia los determina la variable [configuración de asignación de atributos](map-catalog-attributes.md) para su canal.

* **[Cargar nuevos anuncios manualmente](connect-listings-to-marketplace.md#upload-new-product-listings)**: para productos que no coinciden con un anuncio existente en [!DNL Walmart Marketplace], utilice una [!DNL Walmart] categoría de producto Plantilla de Excel para cargar listados de productos por lotes.

## Controles de lista y descripciones de columna

En las tablas siguientes se describen los controles y las columnas disponibles para [!UICONTROL Listings].

**Controles para[!UICONTROL Listings]**

| **Control** | **Descripción** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Abre el [!UICONTROL Admin Product Catalog] página para seleccionar productos que añadir a su [!DNL Walmart Marketplace] o actualizar los atributos de los productos para cumplir con los requisitos de las listas de Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Después de seleccionar uno o más productos en [!UICONTROL Draft] estado, seleccione [!UICONTROL Match products on Walmart] para buscar ofertas de productos que se puedan agregar a una existente [!DNL Walmart Marketplace] listado. |
| [!UICONTROL Refresh products] | Actualice la pantalla con el anuncio y el estado más actuales. Este control también restablece la vista de listado al orden predeterminado y elimina los filtros. |
| [!UICONTROL Filter by *Estado*] | Mostrar sólo anuncios con un estado específico seleccionando una de las tarjetas de estado encima de la tabla Listado. Elimine el filtro seleccionando **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | Cambie el criterio de ordenación de los listados seleccionando cualquier encabezado de columna. |


**Descripciones de columna**

| **Campo** | **Descripción** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nombre del producto de la [!DNL Commerce] catálogo de la tienda. |
| [!UICONTROL SKU (Unique ID)] | El SKU asignado al producto en la variable [!DNL Commerce] catálogo. |
| [!UICONTROL  Quantity] | Cantidad de inventario disponible en Adobe Commerce o Magento Open Source. |
| [!UICONTROL Price] | El precio del producto de la [!DNL Commerce] catálogo de la tienda. Las actualizaciones de precios de catálogo se sincronizan con el Administrador de canales y se envían a [!DNL Walmart Marketplace]  para que los artículos en venta muestren el precio actual. |
| [!UICONTROL Status] | Indica el estado de pedido actual en el [!DNL Commerce] flujo de trabajo de pedidos. El estado se actualiza cuando se añaden correctamente productos a [!DNL Channel Manager] y cuando empareja productos en el mercado. Si falla una operación, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |
| [!UICONTROL Error Description] | Proporciona información de error adicional para productos con una `[!DNL Error]` estado. |

### Acerca del estado del anuncio

En el espacio de trabajo Lista, la etiqueta Estado muestra dónde se encuentra un producto en la [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver errores. Los anuncios pueden tener las siguientes etiquetas de estado:

* **[!UICONTROL Draft]**-Identifica productos que no se han [enviado a [!DNL Walmart] para la coincidencia](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**: identifica los productos enviados para su coincidencia en la [!DNL Walmart Marketplace]. Los productos permanecen en *Procesando* estado hasta que [!DNL Walmart] devuelve un mensaje de estado HTTP que indica si la coincidencia se realizó correctamente o si se produjo un error. La operación de coincidencia puede tardar hasta 30 minutos en completarse en el [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica los productos que se encontraron correctamente en [!DNL Walmart].

   Se produce una coincidencia cuando el valor del atributo del producto (código UPC por ejemplo) coincide con el valor UPC de un [!DNL Walmart Marketplace] listado. Cuando un producto coincide, la oferta de producto de Commerce se agrega al listado existente.

   Compruebe la [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) panel para revisar la lista de productos actualizada y verificar los detalles del producto, el precio y la cantidad de inventario.

* **[!UICONTROL Match - Match in Stage]**: identifica los productos coincidentes en [!DNL Walmart] que no se pueden conectar hasta que [!DNL Walmart Marketplace] la tienda está activa. Los productos con este estado se conectan automáticamente cuando la variable [!DNL Walmart Marketplace] La tienda se pone en marcha.

* **[!UICONTROL Error]**: identifica los productos que no coinciden con un existente [!DNL Walmart Marketplace] listado.

* **[!UICONTROL Error description]**: proporciona información detallada sobre el error de listado.

   Una vez resuelto el error, vuelva a enviar el producto para que coincida. Consulte [Solucionar errores de coincidencia de productos](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
