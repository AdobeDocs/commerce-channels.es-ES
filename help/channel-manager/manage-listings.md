---
title: Administrar anuncios
description: Administrar listados de canal de ventas para un [!DNL Commerce] almacenar con el administrador de canales para Adobe Commerce y Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 61d72e655a9f9eaefddd7561e0bc5fe36da69577
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---

# Administrar anuncios

Administrar listas de productos para [!DNL Walmart Marketplace] canal de ventas de [!UICONTROL Listings] en la vista tienda de canales. El estado de una lista individual indica dónde se encuentra el producto en la [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver los errores.

El estado de una lista individual indica dónde se encuentra el producto en la [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver los errores.

![Página Listados de un canal de ventas conectado](assets/product-listing-landing.png)

Puede completar las siguientes tareas desde la vista Listing .

* Ver anuncios actuales
* Ordenar y filtrar los anuncios
* Agregar productos
* Hacer coincidir productos
* Seguimiento del estado de la lista

## Ver listados de productos

1. Desde el administrador, vaya a [!UICONTROL **Marketing** > Canales > **Administrador de canales**].

1. En la lista Tienda de canales, seleccione el icono de lápiz en una fila de entrada de tienda para abrir la vista de tienda.

1. Select [!UICONTROL **Listados**].

1. Ordenar el *Listing* para ver, seleccione cualquier encabezado de columna en la *Listing* tabla.

1. Filtre el *Listing* seleccione una de las tarjetas de recuento de estado.

1. Restablecer el orden y quitar filtros seleccionando **Actualizar productos**.

## Agregar productos de comercio al Administrador de canales

Cree la gama de productos para el canal de Walmart Marketplace completando las siguientes tareas:

* [Añadir productos del catálogo de productos de Commerce al administrador de canales](add-products-to-connected-channel.md)

* [Configurar la coincidencia de productos](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## Publicar productos en Walmart

Puede crear ofertas de productos en Walmart Marketplace mediante la coincidencia de productos o cargando manualmente listas de productos para nuevos productos. Para obtener instrucciones, consulte [Publicar anuncios en Walmart Marketplace](publish-listings-to-marketplace.md) tal como se describe en los siguientes temas:

* **[Hacer coincidir productos en Walmart](publish-listings-to-marketplace.md)**-Publique listas de productos de su canal a [!DNL Walmart Marketplace] actualizando los listados existentes que venden el mismo producto. Los criterios de coincidencia están determinados por la variable [configuración de asignación de atributos](map-product-attributes-for-matching.md) para su canal.

* **[Cargar manualmente nuevos anuncios](publish-listings-to-marketplace.md#upload-new-product-listings)-**-Para los productos que no coinciden con un anuncio existente en Walmart Marketplace, utilice una plantilla Excel de categoría de producto Walmart para cargar listas de productos de forma masiva.

## Listing Controls y descripciones de columnas

Las tablas siguientes describen los controles y las columnas disponibles para [!UICONTROL Listings].

**Controles para[!UICONTROL Listings]**

| **Control** | **Descripción** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Abre el [!UICONTROL Admin Product Catalog] página para seleccionar los productos que desea agregar al [!DNL Walmart Marketplace] o actualizar los atributos del producto para cumplir los requisitos de listado de Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Después de seleccionar uno o varios productos en estado borrador, seleccione Coincidir productos en Walmart para buscar ofertas de productos que se puedan agregar a una existente [!DNL Walmart Marketplace] listado. |
| [!UICONTROL Refresh products] | Actualice la visualización con el listado y el estado más actuales. Este control también restablece la vista de listado al orden de clasificación predeterminado y elimina los filtros. |
| [!UICONTROL Filter by *Estado*] | Mostrar solo los listados con un estado específico seleccionando una de las tarjetas de recuento de estado encima de la tabla Listing. Utilice la variable *Actualizar productos* para quitar el filtro. |
| [!UICONTROL Sort products] | Cambie el orden de clasificación seleccionando cualquier encabezado de columna. |


**Descripciones de columnas**

| **Campo** | **Descripción** |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nombre del producto de la variable [!DNL Commerce] catálogo de tiendas. |
| [!UICONTROL SKU (Unique ID)] | El atributo asignado utilizado para hacer coincidir productos en el mercado. Este nombre de campo varía en función de la configuración de atributo asignada para [!DNL Channel Manager] anuncios. En este caso, la operación de coincidencia de productos utiliza el SKU de producto de la variable [!DNL Commerce] catálogo para encontrar un [!DNL Walmart Marketplace]  Listado con un valor de SKU que coincida con el valor de SKU del [!DNL Commerce] atributos del producto. |
| [!UICONTROL  Quantity] | Cantidad de inventario disponible en Adobe Commerce o Magento Open Source. |
| [!UICONTROL Price] | El precio del producto de la variable [!DNL Commerce] catálogo de tiendas. Las actualizaciones de precios del catálogo se sincronizan con el Administrador de canales y, a continuación, se envían a [!DNL Walmart Marketplace]  para que los artículos mostrados muestren el precio actual. |
| [!UICONTROL Status] | Indica el estado del pedido actual en la variable [!DNL Commerce] flujo de trabajo de pedido. El estado se actualiza cuando se agregan productos correctamente a [!DNL Channel Manager] y cuando empareja productos en el mercado. Si una operación falla, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |
| [!UICONTROL Status Detail] | Proporciona información adicional para los productos con *Error* o *Coincidencia* estado. |

### Acerca del estado de la lista

En el espacio de trabajo Listing , la etiqueta Status muestra dónde se encuentra un producto en la variable [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver errores. Los anuncios pueden tener las siguientes etiquetas de estado:

* **[!UICONTROL Draft]**-Identifica productos que no se han [enviado a [!DNL Walmart] para coincidencia](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**-Identifica los productos enviados para la coincidencia en la variable [!DNL Walmart Marketplace]. Los productos permanecen en *Procesamiento* hasta que [!DNL Walmart] devuelve un mensaje de estado HTTP que indica si la coincidencia se ha realizado correctamente o si se ha producido un error. La operación de coincidencia puede tardar hasta 30 minutos en completarse en el [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica los productos con los que se ha alcanzado una coincidencia satisfactoria en [!DNL Walmart].

   Se produce una coincidencia cuando el atributo de producto value-UPC code, por ejemplo, coincide con el valor UPC en una[!DNL Walmart Marketplace] listado. Cuando un producto coincide, la oferta de producto de Commerce se agrega a la lista de Walmart existente.

   Marque la [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) tablero para revisar la lista de productos actualizada y verificar los detalles del producto, el precio y la cantidad de inventario.

* **[!UICONTROL Match - Match in Stage]**-Identifica los productos coincidentes en [!DNL Walmart] que no se puede publicar hasta que el [!DNL Walmart Marketplace] la tienda está activa. Los productos con este estado se publican automáticamente cuando el [!DNL Walmart Marketplace] la tienda se pone en marcha.

* **[!UICONTROL Error]**-Identifica los productos que no coinciden con una [!DNL Walmart Marketplace] listado. Vea los detalles del error pasando el ratón sobre el *Error* etiqueta de estado.

   Después de resolver el error, vuelva a enviar el producto para que coincida. Consulte [Solución de problemas de errores de coincidencia de productos](publish-listings-to-marketplace.md#troubleshoot-product-match-errors).
