---
title: Reglas de lista
description: Las reglas de uso de las listas determinan los productos del catálogo de comercio que se publican como anuncios de Amazon Marketplace.
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Reglas de lista

Puede acceder a las reglas de la lista para almacenarlas en la [tablero de almacenamiento](./amazon-store-dashboard.md).

Las reglas de lista definen las reglas para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas proporcionan muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como anuncios. Cada regla consta de condiciones que establecen los requisitos para la idoneidad para la lista de productos.

Las reglas del anuncio se sincronizan continuamente con su [!DNL Commerce] catálogo. Al agregar [!DNL Commerce] productos que cumplen los requisitos de elegibilidad establecidos por las reglas de cotización, los productos se procesan automáticamente para su inclusión en Amazon.

- Si desea que todos sus productos se publiquen en una lista de Amazon, no defina ninguna condición para las reglas de la lista.

- Si desea limitar qué producto del catálogo se publica en Amazon, debe definir las condiciones de las reglas de listado. La definición de las condiciones para las reglas de listado de Amazon sigue la misma lógica y proceso que la definición de las condiciones para [Reglas de precios del carro de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

- Si las reglas de la lista excluyen un producto, el estado de elegibilidad de ese producto cambia a `Ineligible`. Los productos no aptos no se publican en Amazon.

- Si un producto no apto ya aparece en la lista de Amazon y usted coincide con el listado de Amazon en su [!DNL Commerce] producto del catálogo, la cantidad de la lista de Amazon cambia a `0` para evitar ventas del producto. Los anuncios de Amazon se pueden [eliminado manualmente](./end-listings-manually.md).

Los cambios en la cantidad y el estado de elegibilidad afectan a todos los anuncios que comparten el SKU del vendedor de Amazon en mercados que existen para tiendas que venden en la misma región (tal y como se define en _[!UICONTROL Amazon Marketplace Country]_during [integración de tiendas](./store-integration.md)). Sin embargo, un cambio en un [!DNL Amazon Seller SKU] en una región no afecta a las listas de Amazon del producto en un país diferente.

![Reglas de lista](assets/ob-listing-rules.png)

## Configurar las reglas de listado

1. Haga clic en **[!UICONTROL Listing Rules]** en el panel de la tienda.

1. Defina las condiciones que desee para la idoneidad de los productos que se incluirán en Amazon.

Consulte [Ejemplo: Definir una condición](./ob-define-condition-example.md).

| Campo | Descripción |
|---|---|
| [!UICONTROL Websites] | Las opciones disponibles dependen de la variable [sitios web](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} que ha configurado en su [!DNL Commerce] configuración. Seleccione el sitio web de los productos aptos enumerados en Amazon. Solo se puede seleccionar un sitio web, ya que cada sitio web requiere una tienda Amazon única creada en el canal de ventas de Amazon. |
| [!UICONTROL Conditions] | Se utiliza para definir la variable [!DNL Commerce] atributos para la idoneidad del producto dentro de su región de Amazon. Consulte [Ejemplo: Definir una condición](./ob-define-condition-example.md). |

## Espacio de trabajo de condiciones

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

- No agregue condiciones si todos los productos dentro de los sitios web seleccionados son aptos.
- Existe un conjunto complejo de procesos back-end para comunicarse directamente con los sistemas de Amazon. En función del número de elementos que intente enumerar y de la cantidad de usuarios que estén en sistemas de Amazon (como Black Friday), puede que haya que esperar que los elementos aparezcan en Amazon.

Para obtener más información sobre las condiciones, consulte [Describir las condiciones](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

## Vista previa de regla de anuncio

Cuando modifique las definiciones de condiciones para las reglas de listado, puede hacer clic en **[!UICONTROL Preview Changes]** para aplicar los cambios de reglas y ver cómo se ven afectados sus anuncios. Compruebe sus anuncios en esta función de vista previa de anuncio antes de guardar los cambios en la regla de anuncio.

Los anuncios de Amazon se comparan con las reglas y condiciones definidas. A continuación, puede revisar:

- Qué productos pasan a ser inelegibles en función de su estado actual [!DNL Amazon Seller Central] account
- Qué productos pasan de un estado no elegible a un estado apto
- Qué productos son nuevos anuncios de Amazon y se han agregado a su lista de Amazon desde su lista de productos aptos [!DNL Commerce] products

Vista previa de anuncio le permite obtener una vista previa de los anuncios potenciales de Amazon y realizar los ajustes necesarios en las reglas de anuncio.

Los anuncios potenciales de Amazon se rellenan en la variable _[!UICONTROL Listing Preview]_en una de las tres pestañas:

- **[!UICONTROL Ineligible Listings]** - Los productos enumerados no son aptos para la lista de Amazon según las reglas y condiciones de la lista actual.

   Los productos no aptos no se publican en Amazon. Si un producto no apto ya aparece en la lista de Amazon y usted coincide con el listado de Amazon en su [!DNL Commerce] producto del catálogo, la cantidad de la lista de Amazon cambia a `0` para evitar ventas del producto. Para quitar manualmente un listado, consulte [Finalización de una lista de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no se enumeran aquí. Estos productos se incluyen en la lista [Pestaña Listados inactivos](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Los productos que figuran en la lista pueden incluirse en la lista de Amazon en función de las reglas y condiciones de la lista actual, y también pueden optar a los requisitos de Amazon. Esta lista incluye los listados de Amazon existentes que se importan (si tiene **Importar anuncios de terceros** configure como `Import Listing` en [Configuración de lista](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Los productos listados incluyen su [!DNL Commerce] catálogo de productos que recientemente cumplen los requisitos para la lista de Amazon según las reglas y condiciones de la lista actual, y cree y publique nuevos anuncios de Amazon.

### Ver la vista previa del anuncio

1. Haga clic en **[!UICONTROL Listing Rules]** en el panel de la tienda.

1. Vea o agregue su [listar reglas](./listing-rules.md).

1. Modifique su [Condiciones de reglas de lista](./ob-define-condition-example.md).

1. Haga clic en **[!UICONTROL Preview Changes]**.

1. Revise y confirme sus anuncios en la _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ y _[!UICONTROL New Listings]_pestañas.

1. Si sus anuncios coinciden con sus expectativas, haga clic en **[!UICONTROL Save and close]**.

   Si sus anuncios no aparecen como se esperaba, haga clic en **[!UICONTROL Back]** y modifique sus reglas y condiciones hasta que sus anuncios coincidan con sus expectativas.

![Vista previa de regla de anuncio](assets/amazon-listing-rule-preview.png)

### Listando registros de vista previa

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Product ID] | El número único y secuencial que se asigna a un [!DNL Commerce] producto de catálogo cuando se agregue. |
| [!UICONTROL Thumbnail] | Muestra una miniatura de la imagen principal del producto. |
| [!UICONTROL Name] | El nombre del producto, administrado en la variable [!DNL Commerce] [cuadrícula de productos](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Type] | El tipo de producto, administrado en la variable [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL Attribute Set] | El nombre del conjunto de atributos utilizado como plantilla para el producto, administrado en la variable [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL SKU] | La unidad única de mantenimiento de stock asignada al producto, administrada en la variable [!DNL Commerce] cuadrícula de productos. |
| [!UICONTROL Visibility] | Indica dónde está visible el producto, y se administra en la variable [!DNL Commerce] cuadrícula de productos. Opciones:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Estado | Indica el estado del producto, administrado en la variable [!DNL Commerce] cuadrícula de productos. Opciones: `Enabled` / `Disabled` |

![Flujo de trabajo de vista previa de anuncio](assets/listing-preview-flowchart.png)
