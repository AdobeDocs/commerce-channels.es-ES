---
title: Canal de ventas de Amazon - [!UICONTROL Listing Rules]
description: Utilice reglas de listado para determinar los productos del catálogo de Commerce que se publican como listados de Amazon Marketplace.
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

Puede acceder a las reglas de listado para almacenar en la [tablero de tienda](./amazon-store-dashboard.md).

Las reglas de listado definen las reglas para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas ofrecen muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como listados. Cada regla consta de condiciones que establecen los requisitos para la elegibilidad de la lista de productos.

Las reglas de anuncios se sincronizan continuamente con tu [!DNL Commerce] catálogo. Cuando se añade un nuevo [!DNL Commerce] productos que cumplen los requisitos de idoneidad establecidos por las reglas de listado, los productos se procesan automáticamente para su listado en Amazon.

- Si desea que todos sus productos se publiquen en un anuncio de Amazon, no defina ninguna condición para las reglas del anuncio.

- Si desea limitar cuáles de los productos del catálogo se publican en Amazon, defina las condiciones de la regla de listado. La definición de las condiciones para las reglas de listado de Amazon sigue la misma lógica y proceso que la definición de las condiciones para [Reglas de precio de carrito](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- Si las reglas de la lista excluyen un producto, el estado de idoneidad de ese producto cambia a `Ineligible`. Los productos no aptos no se publican en Amazon.

- Si un producto no apto ya figura en Amazon y usted relaciona el anuncio de Amazon con su [!DNL Commerce] producto del catálogo, la cantidad del listado de Amazon cambia a `0` para evitar la venta del producto. Los anuncios de Amazon pueden ser [eliminado manualmente](./end-listings-manually.md).

Los cambios en la cantidad y en el estado de idoneidad afectan a todos los anuncios que comparten el SKU del vendedor de Amazon en los mercados que existen para tiendas que venden en la misma región (tal y como se define en _[!UICONTROL Amazon Marketplace Country]_durante [integración de tienda](./store-integration.md)). Sin embargo, un cambio en un recurso compartido [!DNL Amazon Seller SKU] en una región no afecta a los anuncios de Amazon del producto en un país diferente.

![Reglas de listado](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## Configurar las reglas de listado

1. Clic **[!UICONTROL Listing Rules]** en el tablero de la tienda.

1. Defina las condiciones deseadas para la idoneidad de los productos que se enumerarán en Amazon.

Consulte [Ejemplo: Definición de una condición](./ob-define-condition-example.md).

| Campo | Descripción |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | Las opciones disponibles dependen de la variable [sitios web](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) que ha configurado en su [!DNL Commerce] configuración. Seleccione el sitio web de los productos aptos que aparecen en Amazon. Solo se puede seleccionar un sitio web, ya que cada sitio web requiere una tienda Amazon única creada en el canal de ventas de Amazon. |
| [!UICONTROL Conditions] | Se utiliza para definir la variable [!DNL Commerce] atributos para la idoneidad del producto dentro de su región de Amazon. Consulte [Ejemplo: Definición de una condición](./ob-define-condition-example.md). |

## Espacio de trabajo Condiciones

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

- No agregue condiciones si todos los productos de los sitios web seleccionados cumplen los requisitos.
- Existe un complejo conjunto de procesos back-end para comunicarse directamente con los sistemas de Amazon. En función del número de artículos que intentas poner en venta y de la ocupación que puedan tener los sistemas de Amazon (por ejemplo, Black Friday), puede que tus artículos tarden un tiempo en aparecer en Amazon.

Para obtener más información sobre las condiciones, consulte [Describir las condiciones](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## Previsualización de regla de anuncio

Cuando modifique las definiciones de condición para las reglas de listado, puede hacer clic en **[!UICONTROL Preview Changes]** para aplicar los cambios de las reglas y ver cómo se ven afectados los anuncios. Comprueba tus anuncios en esta función de vista previa antes de guardar los cambios de las reglas de anuncios.

Los anuncios de Amazon se comparan con las reglas y las condiciones definidas. A continuación, puede revisar:

- Qué productos pasan a un estado no apto en función de su [!DNL Amazon Seller Central] account
- Qué productos pasan de un estado no apto a un estado apto
- ¿Qué productos son nuevos anuncios de Amazon y se añaden a tu anuncio de Amazon desde el anuncio apto? [!DNL Commerce] products

Vista previa de anuncios permite obtener una vista previa de los anuncios de Amazon y realizar los ajustes necesarios en las reglas de anuncios.

Los posibles anuncios de Amazon se rellenan en _[!UICONTROL Listing Preview]_en una de las tres pestañas:

- **[!UICONTROL Ineligible Listings]** - Los productos que aparecen en la lista no cumplen los requisitos para aparecer en la lista de Amazon según las reglas y condiciones actuales.

  Los productos no aptos no se publican en Amazon. Si un producto no apto ya figura en Amazon y usted relaciona el anuncio de Amazon con su [!DNL Commerce] producto del catálogo, la cantidad del listado de Amazon cambia a `0` para evitar la venta del producto. Para quitar manualmente un listado, consulte [Finalizar un anuncio de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no aparecen aquí. Estos productos se enumeran en la [Pestaña Anuncios inactivos](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Los productos que aparecen en la lista cumplen los requisitos para aparecer en la lista de Amazon según las reglas y condiciones actuales del anuncio, y también cumplen los requisitos de Amazon. Esta lista incluye los anuncios existentes de Amazon que se importan (si tiene **Importar anuncios de terceros** establezca en `Import Listing` in [Configuración de anuncio](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Los productos enumerados incluyen su [!DNL Commerce] catalogar productos que acaban de ser aptos para la creación de anuncios de Amazon en función de las reglas y condiciones actuales, y crear y publicar nuevos anuncios de Amazon.

### Ver la vista previa del anuncio

1. Clic **[!UICONTROL Listing Rules]** en el tablero de la tienda.

1. Ver o agregar su [enumerar reglas](./listing-rules.md).

1. Modifique su [Condiciones de reglas de listado](./ob-define-condition-example.md).

1. Haga clic **[!UICONTROL Preview Changes]**.

1. Revisa y confirma tus anuncios en la _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_, y _[!UICONTROL New Listings]_pestañas.

1. Si tus anuncios cumplen tus expectativas, pulsa **[!UICONTROL Save and close]**.

   Si los anuncios no se muestran según lo esperado, pulsa **[!UICONTROL Back]** y modifica las reglas y condiciones hasta que los anuncios cumplan tus expectativas.

![Previsualización de regla de anuncio](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### Listado de registros de vista previa

| Campo | Descripción |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | El número único y secuencial que se asigna a un [!DNL Commerce] el producto del catálogo cuando se añada. |
| [!UICONTROL Thumbnail] | Muestra una miniatura de la imagen principal del producto. |
| [!UICONTROL Name] | El nombre del producto, administrado en la variable [!DNL Commerce] [cuadrícula de productos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | El tipo de producto, administrado en la variable [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL Attribute Set] | El nombre del conjunto de atributos utilizado como plantilla para el producto, administrado en la variable [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL SKU] | La única unidad de mantenimiento de stock asignada al producto, gestionada en el [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL Visibility] | Indica dónde está visible el producto, administrado en el [!DNL Commerce] cuadrícula de productos. Opciones:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Estado | Indica el estado del producto, gestionado en el [!DNL Commerce] cuadrícula de productos. Opciones: `Enabled` / `Disabled` |

![Flujo de trabajo de vista previa](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
