---
title: 'Canal de ventas de Amazon: [!UICONTROL Listing Rules]'
description: Utilice reglas de listado para determinar los productos del catálogo Commerce que se publican como listados de Amazon Marketplace.
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

Puede obtener acceso a las reglas de listado para almacenar en el [tablero de almacén](./amazon-store-dashboard.md).

Las reglas de listado definen las reglas para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas ofrecen muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como listados. Cada regla consta de condiciones que establecen los requisitos para la elegibilidad de la lista de productos.

Las reglas de listado se sincronizan continuamente con el catálogo [!DNL Commerce]. Al agregar nuevos [!DNL Commerce] productos que cumplen con los requisitos de elegibilidad establecidos por las reglas de listado, los productos se procesan automáticamente para listarse en Amazon.

- Si desea que todos sus productos se publiquen en un anuncio de Amazon, no defina ninguna condición para las reglas del anuncio.

- Si desea limitar cuáles de los productos del catálogo se publican en Amazon, defina las condiciones de la regla de listado. La definición de las condiciones de las reglas de anuncios de Amazon sigue la misma lógica y proceso que la definición de las condiciones de [Reglas de precios del carro de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- Si las reglas de la lista excluyen un producto, el estado de idoneidad para ese producto cambia a `Ineligible`. Los productos no aptos no se publican en Amazon.

- Si un producto no apto ya figura en Amazon y el listado de Amazon coincide con el producto del catálogo [!DNL Commerce], la cantidad del listado de Amazon cambia a `0` para evitar las ventas del producto. Los anuncios de Amazon se pueden [eliminar manualmente](./end-listings-manually.md).

Los cambios en la cantidad y el estado de idoneidad afectan a todos los anuncios que comparten la SKU de Amazon Seller en mercados que existen para tiendas que venden en la misma región (tal y como se define en _[!UICONTROL Amazon Marketplace Country]_durante [integración de tiendas](./store-integration.md)). Sin embargo, un cambio en un(a) [!DNL Amazon Seller SKU] compartido(a) en una región no afecta los anuncios de Amazon del producto en un país diferente.

![Reglas de anuncio](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## Configurar las reglas de listado

1. Haga clic en **[!UICONTROL Listing Rules]** en el tablero del almacén.

1. Defina las condiciones deseadas para la idoneidad de los productos que se enumerarán en Amazon.

Ver [Ejemplo: Definir una condición](./ob-define-condition-example.md).

| Campo | Descripción |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | Las opciones disponibles dependen de los [sitios web](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) que haya configurado en la configuración de [!DNL Commerce]. Seleccione el sitio web de los productos aptos que aparecen en Amazon. Solo se puede seleccionar un sitio web, ya que cada sitio web requiere una tienda Amazon única creada en el canal de ventas de Amazon. |
| [!UICONTROL Conditions] | Se usa para definir los atributos [!DNL Commerce] de idoneidad del producto dentro de su región de Amazon. Ver [Ejemplo: Definir una condición](./ob-define-condition-example.md). |

## Espacio de trabajo Condiciones

Se puede hacer clic en cualquier área de las condiciones que esté en negrita para ver las distintas opciones.

- No agregue condiciones si todos los productos de los sitios web seleccionados cumplen los requisitos.
- Existe un complejo conjunto de procesos back-end para comunicarse directamente con los sistemas de Amazon. En función del número de artículos que intentas poner en venta y de la ocupación que puedan tener los sistemas de Amazon (por ejemplo, Black Friday), puede que tus artículos tarden un tiempo en aparecer en Amazon.

Para obtener más información acerca de las condiciones, vea [Describir las condiciones](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## Previsualización de regla de anuncio

Cuando esté modificando las definiciones de condición para las reglas de listado, puede hacer clic en **[!UICONTROL Preview Changes]** para aplicar los cambios de reglas y ver cómo se ven afectados los listados. Comprueba tus anuncios en esta función de vista previa antes de guardar los cambios de las reglas de anuncios.

Los anuncios de Amazon se comparan con las reglas y las condiciones definidas. A continuación, puede revisar:

- Qué productos pasan a un estado no apto según su cuenta actual de [!DNL Amazon Seller Central]
- Qué productos pasan de un estado no apto a un estado apto
- Qué productos son Nuevos anuncios de Amazon y se agregaron a tu anuncio de Amazon a partir de tus [!DNL Commerce] productos aptos

Vista previa de anuncios permite obtener una vista previa de los anuncios de Amazon y realizar los ajustes necesarios en las reglas de anuncios.

Los posibles listados de Amazon se rellenan en la página _[!UICONTROL Listing Preview]_en una de las tres fichas:

- **[!UICONTROL Ineligible Listings]**: los productos enumerados no cumplen los requisitos para el anuncio de Amazon según las reglas y condiciones actuales del anuncio.

  Los productos no aptos no se publican en Amazon. Si un producto no apto ya figura en Amazon y el listado de Amazon coincide con el producto del catálogo [!DNL Commerce], la cantidad del listado de Amazon cambia a `0` para evitar las ventas del producto. Para quitar manualmente un listado, vea [Finalizar un listado de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no aparecen aquí. Estos productos se muestran en la ficha [Anuncios inactivos](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]**: los productos enumerados cumplen los requisitos para el anuncio de Amazon en función de las reglas y condiciones actuales del anuncio, y también cumplen los requisitos de Amazon. Esta lista incluye los anuncios existentes de Amazon que importan (si tiene **Importar anuncios de terceros** establecidos en `Import Listing` en [Configuración de anuncios](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]**: los productos enumerados incluyen los productos del catálogo [!DNL Commerce] que cumplen los requisitos para aparecer en el listado de Amazon según las reglas y condiciones actuales, y crean y publican nuevos listados de Amazon.

### Ver la vista previa del anuncio

1. Haga clic en **[!UICONTROL Listing Rules]** en el tablero del almacén.

1. Ver o agregar [reglas de anuncio](./listing-rules.md).

1. Modifica tus [condiciones de regla de anuncio](./ob-define-condition-example.md).

1. Haga clic en **[!UICONTROL Preview Changes]**.

1. Revise y confirme sus anuncios en las fichas _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ y _[!UICONTROL New Listings]_.

1. Si tus anuncios cumplen tus expectativas, haz clic en **[!UICONTROL Save and close]**.

   Si tus anuncios no se muestran según lo esperado, pulsa **[!UICONTROL Back]** y modifica las reglas y condiciones hasta que se ajusten a tus expectativas.

![Vista previa de regla de anuncio](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### Listado de registros de vista previa

| Campo | Descripción |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | Número único secuencial que se asigna a un producto de catálogo [!DNL Commerce] cuando se agrega. |
| [!UICONTROL Thumbnail] | Muestra una miniatura de la imagen principal del producto. |
| [!UICONTROL Name] | El nombre del producto, administrado en la [!DNL Commerce] [cuadrícula de productos](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | El tipo de producto, administrado en la cuadrícula de productos [!DNL Commerce]. |
| [!UICONTROL Attribute Set] | Nombre del conjunto de atributos utilizado como plantilla para el producto, administrado en la cuadrícula de productos [!DNL Commerce]. |
| [!UICONTROL SKU] | La única unidad de mantenimiento de existencias asignada al producto, administrada en la cuadrícula de productos [!DNL Commerce]. |
| [!UICONTROL Visibility] | Indica dónde está visible el producto, administrado en la cuadrícula de productos [!DNL Commerce]. Opciones:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Estado | Indica el estado del producto, administrado en la cuadrícula de productos [!DNL Commerce]. Opciones: `Enabled` / `Disabled` |

![Flujo de trabajo de vista previa del anuncio](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
