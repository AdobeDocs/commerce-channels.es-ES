---
title: Administrar pedidos
description: Administrar listados de canal de ventas para un [!DNL Commerce] almacenar con el administrador de canales para Adobe Commerce y Magento Open Source.
source-git-commit: d1de3bb8873ea6bd141914c083b023def07999fd
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Administrar anuncios

Administrar listas de productos para un canal conectado desde[!UICONTROL Listings] en la vista tienda de canales.

El espacio de trabajo Listings incluye los productos para listarlos en Walmart Marketplace y proporciona las herramientas para administrar listados. El estado de un listado individual muestra dónde se encuentra el producto en la variable [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver errores.

![Página Listados de un canal de ventas conectado](assets/products-submit-for-matching.png)

## Ver anuncios

1. Desde el administrador, vaya a [!UICONTROL **Marketing** > Canales > **Administrador de canales**].

1. En la lista Tienda de canales, seleccione el icono de lápiz en una fila de entrada de tienda para abrir la vista de tienda.

1. Select [!UICONTROL **Listados**].


## Publicar productos en Walmart

Puede crear ofertas de productos en Walmart Marketplace mediante la coincidencia de productos o cargando manualmente listas de productos para nuevos productos. Para obtener instrucciones, consulte [Publicar anuncios en Walmart Marketplace](publish-listings-to-marketplace.md) tal como se describe en los siguientes temas:

* **[Hacer coincidir productos en Walmart](publish-listings-to-marketplace.md)**-Publique listas de productos de su canal a [!DNL Walmart Marketplace] actualizando los listados existentes que venden el mismo producto. Los criterios de coincidencia están determinados por la variable [configuración de asignación de atributos](map-product-attributes-for-matching.md) para su canal.

* **Cargar manualmente nuevos anuncios**-Para los productos que no coinciden con un anuncio existente en Walmart Marketplace, utilice una plantilla Excel de categoría de producto Walmart para cargar listas de productos de forma masiva.

## Acerca de los controles de lista y la información

**Controles para[!UICONTROL Listings]**

| **Atributo** | **Nivel de requisito** |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actualizar productos | Actualiza la visualización con los datos de listado y estado más actuales. |
| Agregar productos | Abre el [!UICONTROL  Admin Product Catalog] página para seleccionar los productos que desea agregar al [!DNL Walmart Marketplace] o actualizar los atributos del producto para cumplir los requisitos de listado de Walmart Marketplace. |
| Hacer coincidir productos en Walmart | Después de seleccionar uno o varios productos en estado borrador, seleccione Coincidir productos en Walmart para buscar ofertas de productos que se puedan agregar a una existente[!DNL Walmart Marketplace] listado. |


**Descripciones de columnas**

| **Campo** | **Descripción** |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre del producto | Nombre del producto de la variable [!DNL Commerce] catálogo de tiendas. |
| SKU (ID único) | El atributo asignado utilizado para hacer coincidir productos en el mercado. Este nombre de campo varía en función de la configuración de atributo asignada para [!DNL Channel Manager] anuncios. En este caso, la operación de coincidencia de productos utiliza el SKU de producto de la variable [!DNL Commerce] catálogo para encontrar un [!DNL Walmart Marketplace]  Listado con un valor de SKU que coincide con el valor de SKU de los atributos de producto de comercio. |
| Cantidad | Cantidad de inventario disponible en Adobe Commerce o Magento Open Source. |
| Precio | El precio del producto de la variable [!DNL Commerce] catálogo de tiendas. Las actualizaciones de precios del catálogo se sincronizan con el Administrador de canales y, a continuación, se envían a [!DNL Walmart Marketplace]  para que los artículos mostrados muestren el precio actual. |
| Estado | Indica el estado del pedido actual en la variable [!DNL Commerce] flujo de trabajo de pedido. El estado se actualiza cuando se agregan productos correctamente a [!DNL Channel Manager] y cuando empareja productos en el mercado. Si falla una operación, la lista muestra un estado de error. Después de corregir el error, [!DNL Channel Manager] reintenta la operación y actualiza el estado. |


### Acerca del estado de la lista

En el espacio de trabajo Listing , la etiqueta Status muestra dónde se encuentra un producto en la variable [!DNL Channel Manager] flujo de trabajo para que pueda determinar los pasos siguientes y resolver errores. Estado del producto*.

* **[!UICONTROL Draft]**-Identifica productos que no se han [enviado a [!DNL Walmart] para coincidencia](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**-Identifica los productos enviados para la coincidencia en la variable [!DNL Walmart Marketplace]. Los productos permanecen en *Procesamiento* hasta que [!DNL Walmart Marketplace] devuelve un mensaje de estado HTTP que indica si la coincidencia se ha realizado correctamente o si se ha producido un error. La operación de coincidencia puede tardar hasta 30 minutos en completarse en el [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifica los productos que se compararon correctamente con Walmart.

   Se produce una coincidencia cuando el atributo de producto value-UPC code, por ejemplo, coincide con el valor UPC en una[!DNL Walmart Marketplace] listado. Cuando un producto coincide, la oferta de producto de Commerce se agrega a la lista de Walmart existente.

   Marque la [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) tablero para revisar la lista de productos actualizada y verificar los detalles del producto, el precio y la cantidad de inventario.


* **[!UICONTROL Error]**-Identifica los productos que no coinciden con una [!DNL Walmart Marketplace] listado. Vea los detalles del error pasando el ratón sobre el *Error* etiqueta de estado.

   Después de resolver el error, vuelva a enviar el producto para que coincida. Consulte [Solución de problemas de errores de coincidencia de productos](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]**-Identifica los productos coincidentes en [!DNL Walmart] que no se puede publicar hasta que el [!DNL Walmart Marketplace] la tienda está activa. Los productos con este estado se publican automáticamente cuando el [!DNL Walmart Marketplace] la tienda se pone en marcha.



