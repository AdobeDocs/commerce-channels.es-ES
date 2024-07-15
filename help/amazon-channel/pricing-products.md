---
title: Administrar precios de Amazon
description: Puedes definir unos precios diferentes para los anuncios de Amazon de tu tienda Commerce mediante las reglas de precios.
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Administrar precios de Amazon

El canal de ventas de Amazon te permite establecer reglas de precios, lo que te permite establecer un precio de anuncio de Amazon distinto del **[!UICONTROL Magento Price Source]** definido en el [precio de anuncio](./listing-price.md). También puede apilar múltiples reglas e incluso usar los precios inteligentes para ajustar el precio de su anuncio de Amazon en función del precio de [[!DNL Buy Box]](./buy-box-competitor-pricing.md) de la competencia o el [precio más bajo de la competencia](./lowest-competitor-pricing.md).

Existen dos tipos de reglas de precios:

- [Regla de precios estándar](./standard-price-rules.md)
- [Regla de reasignación inteligente](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >Las reglas de reasignación de precios inteligentes no funcionan correctamente si la región de Amazon está configurada con el estado `Inactive`, tal como sucede durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en estado `Active` para que las tarifas de envío se sincronicen desde Amazon.
  >
  >Para actualizar el estado de tu región en la cuenta de Amazon, ve a Configuración > Información de la cuenta > Configuración de vacaciones. Consulte [Amazon: estado del anuncio para las vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) (se requiere el inicio de sesión en la Central de vendedores).

Esta característica le permite manipular los precios de Amazon de forma similar a las [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). Puede crear reglas complejas que le permitan cambiar los precios de productos específicos, productos dentro de categorías específicas o incluso con atributos específicos.

Puedes agregar reglas de precios para tus anuncios de Amazon. Las reglas de precios se pueden utilizar para ajustar automáticamente los precios de los anuncios, según un conjunto de condiciones definidas. Las reglas de precios se activan y calculan el precio ajustado antes de que el producto aparezca en Amazon.

>[!NOTE]
>
>La fuente de precios para tus anuncios de Amazon está definida para **[!UICONTROL Magento Price Source]** en la configuración de [precio de anuncio](./listing-price.md). Cualquier cálculo de ajuste definido en la regla de asignación de precios utiliza el origen de precio como valor inicial.

Las reglas de precios te permiten establecer un precio de anuncio de Amazon diferente de **[!UICONTROL Magento Price Source]** en la configuración de [precio de anuncio](./listing-price.md). También puede apilar varias reglas que funcionen juntas para ajustar el precio.

Una regla de asignación de precios/reasignación de precios requiere tres conjuntos de información durante su configuración:

- [Configuración general](./pricing-rule-general-settings.md): define el nombre, la descripción, las fechas de actividad y la prioridad de una regla, y establece el comportamiento de las reglas subsiguientes en función de su configuración de prioridad.
- [Condiciones](./pricing-rule-conditions.md): Determine qué productos cumplen los requisitos para la regla de precios.
- [Acciones](./pricing-rule-actions.md): defina los cálculos de ajuste que se aplican al origen de precios para determinar el precio del listado.

Puede crear [reglas de precios estándar](./standard-price-rules.md) que ajusten automáticamente el precio del anuncio de Amazon en relación con el **[!UICONTROL Magento Price Source]** seleccionado en la configuración de [precio del anuncio](./listing-price.md). Esta característica le permite manipular los precios de Amazon de forma similar a las [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). Puede crear reglas complejas que cambien automáticamente los precios de productos específicos, productos dentro de categorías específicas o productos con atributos específicos. Puede completar la configuración tradicional y reasignar el precio de los productos para aumentar o disminuir según una cantidad fija o un porcentaje.

Otra herramienta poderosa es la función [Reasignación Inteligente de Precios](./intelligent-repricing-rules.md) que ajusta el precio de tu anuncio de Amazon en función del precio de la competencia [[!DNL Buy Box]](./buy-box-competitor-pricing.md) o el [Precio Más Bajo de la Competencia](./lowest-competitor-pricing.md). Similar a las [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html), esta característica avanzada le permite manipular los precios de Amazon creando reglas complejas. Las reglas pueden definir el ámbito de un cambio de precio para productos específicos, productos dentro de categorías específicas o incluso con atributos de producto específicos.

Utilizar la reasignación inteligente de precios para ajustar los precios de listado de Amazon, según los precios de la competencia. El canal de ventas de Amazon ha incorporado protecciones para que pueda proteger los márgenes o evitar que los precios de un comerciante coincidan con los bajos comentarios. Con [reglas inteligentes de reasignación de precios](./intelligent-repricing-rules.md), los precios de listado de Amazon se pueden manipular automáticamente como una cantidad fija o porcentual (arriba o abajo) o incluso sincronizarse con el precio [[!DNL Buy Box]](./buy-box-competitor-pricing.md) o con el [Precio más bajo de la competencia](./lowest-competitor-pricing.md) por artículo. Las reglas incluso se pueden apilar para proporcionar una flexibilidad ilimitada.

Puede controlar aspectos importantes de las reglas, como el estado activo/inactivo, la idoneidad del sitio web, los intervalos de fechas opcionales y los niveles de prioridad opcionales (utilizados para el apilamiento de reglas).

Por ejemplo, puedes definir y establecer las condiciones de una regla de precios que, cuando se cumplan las condiciones, ajuste automáticamente el precio del anuncio antes de enviarlo a Amazon.

Otra opción de precios es [anulación de precios](./overrides.md), que se establece en el nivel de anuncio individual. Se puede establecer un [reemplazo de precio](./overrides.md), y un reemplazo ignora/tiene prioridad sobre todos los demás valores predeterminados, configuraciones y reglas. Se puede establecer un [reemplazo](./overrides.md) para el precio, el tiempo de manipulación, la condición y las notas del vendedor (con algunas excepciones).

![Reglas de precios](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## Columnas predeterminadas

| Columna | Descripción |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | Nombre de la regla de precios, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | El tipo de regla, tal como se establece en [Acciones de regla de asignación de precios](./pricing-rule-actions.md) (ya sea regla de precio estándar o regla de reasignación de precios inteligente) |
| [!UICONTROL Is Active] | Si la regla está activa, como se establece en [Configuración general de regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La prioridad sobre otras condiciones de precios, tal como se establece en [Configuración general de regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica si se procesan otras reglas de precios en productos que cumplen los requisitos para esta regla, según se establece en [configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Inicio del período de tiempo en el que la regla está activa |
| [!UICONTROL To Date] | El final del período de tiempo en el que la regla está activa |
| [!UICONTROL Action] | Enumera todas las acciones que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_. Opciones: `Edit Price Rule` / `Delete Price Rule` |
