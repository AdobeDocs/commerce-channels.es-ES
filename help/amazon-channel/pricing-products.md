---
title: Administrar precios de Amazon
description: Puedes establecer que los precios de los anuncios de Amazon difieran de los de tu tienda de comercio mediante las reglas de precios.
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Administrar precios de Amazon

El canal de ventas de Amazon le permite establecer reglas de precios, lo que le permite establecer un precio de anuncio de Amazon diferente del definido **[!UICONTROL Magento Price Source]** en su [precio de venta](./listing-price.md). También puede apilar varias reglas e incluso utilizar los precios inteligentes para ajustar el precio de su anuncio de Amazon en función de los precios de la competencia [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio o el [precio más bajo de competidor](./lowest-competitor-pricing.md).

Existen dos tipos de reglas de precios:

- [Regla de precios estándar](./standard-price-rules.md)
- [Regla de reasignación inteligente](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >Las reglas de reasignación de precios inteligentes no funcionan correctamente si la región de Amazon está configurada como `Inactive` estado, tal como aparece durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en `Active` estado de las tarifas de envío que se sincronizarán desde Amazon.
  >
  >Para actualizar el estado de tu región en la cuenta de Amazon, ve a Configuración > Información de la cuenta > Configuración de vacaciones. Consulte [Amazon: Estado del anuncio para vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) (Se requiere el inicio de sesión en Seller Central).

Esta función le permite manipular los precios de Amazon de una manera similar a la [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). Puede crear reglas complejas que le permitan cambiar los precios de productos específicos, productos dentro de categorías específicas o incluso con atributos específicos.

Puedes agregar reglas de precios para tus anuncios de Amazon. Las reglas de precios se pueden utilizar para ajustar automáticamente los precios de los anuncios, según un conjunto de condiciones definidas. Las reglas de precios se activan y calculan el precio ajustado antes de que el producto aparezca en Amazon.

>[!NOTE]
>
>La fuente de precios de los anuncios de Amazon está definida para **[!UICONTROL Magento Price Source]** en su [precio de venta](./listing-price.md) configuración. Cualquier cálculo de ajuste definido en la regla de asignación de precios utiliza el origen de precio como valor inicial.

Las reglas de precios permiten establecer el precio del anuncio de Amazon de forma diferente al de **[!UICONTROL Magento Price Source]** en su [precio de venta](./listing-price.md) configuración. También puede apilar varias reglas que funcionen juntas para ajustar el precio.

Una regla de asignación de precios/reasignación de precios requiere tres conjuntos de información durante su configuración:

- [Configuración general](./pricing-rule-general-settings.md): define el nombre, la descripción, las fechas de actividad y la prioridad de una regla y establece el comportamiento de las reglas siguientes en función de su configuración de prioridad.
- [Condiciones](./pricing-rule-conditions.md): Determine qué productos cumplen los requisitos para la regla de precio.
- [Acciones](./pricing-rule-actions.md): Defina los cálculos de ajuste que se aplican al origen de precios para determinar el precio de listado.

Puede crear [reglas de precios estándar](./standard-price-rules.md) que ajustan automáticamente el precio del anuncio de Amazon en relación con el seleccionado **[!UICONTROL Magento Price Source]** en su [precio de venta](./listing-price.md) configuración. Esta función le permite manipular los precios de Amazon de una manera similar a la [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). Puede crear reglas complejas que cambien automáticamente los precios de productos específicos, productos dentro de categorías específicas o productos con atributos específicos. Puede completar la configuración tradicional y reasignar el precio de los productos para aumentar o disminuir según una cantidad fija o un porcentaje.

Otra herramienta potente es la [Reasignación inteligente de precios](./intelligent-repricing-rules.md) función que ajusta el precio del anuncio de Amazon en función de la competencia [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio o [Precio de competidor más bajo](./lowest-competitor-pricing.md). Similar a la [!DNL Commerce] [reglas de precios de catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)Sin embargo, esta función avanzada le permite manipular los precios de Amazon creando reglas complejas. Las reglas pueden definir el ámbito de un cambio de precio para productos específicos, productos dentro de categorías específicas o incluso con atributos de producto específicos.

Utilizar la reasignación inteligente de precios para ajustar los precios de listado de Amazon, según los precios de la competencia. El canal de ventas de Amazon ha incorporado protecciones para que pueda proteger los márgenes o evitar que los precios de un comerciante coincidan con los bajos comentarios. Uso de [reglas inteligentes de reasignación de precios](./intelligent-repricing-rules.md), los precios de las listas de Amazon pueden manipularse automáticamente como una cantidad fija o porcentual (hacia arriba o hacia abajo) o incluso sincronizarse con el [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio o [Precio de competidor más bajo](./lowest-competitor-pricing.md) por artículo. Las reglas incluso se pueden apilar para proporcionar una flexibilidad ilimitada.

Puede controlar aspectos importantes de las reglas, como el estado activo/inactivo, la idoneidad del sitio web, los intervalos de fechas opcionales y los niveles de prioridad opcionales (utilizados para el apilamiento de reglas).

Por ejemplo, puedes definir y establecer las condiciones de una regla de precios que, cuando se cumplan las condiciones, ajuste automáticamente el precio del anuncio antes de enviarlo a Amazon.

Otra opción de precios es una [anulación de precios](./overrides.md), que se establece en el nivel de listado individual. A [anulación de precios](./overrides.md) se puede establecer, y una anulación ignora o tiene prioridad sobre el resto de valores predeterminados, configuraciones y reglas. Un [invalidar](./overrides.md) se puede configurar para el precio, el tiempo de manipulación, la condición y las notas del vendedor (con algunas excepciones).

![Reglas de precios](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## Columnas predeterminadas

| Columna | Descripción |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | El nombre de la regla de precios, tal como se establece en [Configuración general de reglas de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | El tipo de regla, tal como se establece en [Acciones de regla de precios](./pricing-rule-actions.md) (Regla de precio estándar o Regla de reasignación de precios inteligente) |
| [!UICONTROL Is Active] | Si la regla está activa, como se establece en [Configuración general de reglas de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La prioridad sobre otras condiciones de precios, tal como se establece en [Configuración general de reglas de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica si se procesan otras reglas de precios en productos aptos para esta regla, según se establece en [configuración general de reglas de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Inicio del período de tiempo en el que la regla está activa |
| [!UICONTROL To Date] | El final del período de tiempo en el que la regla está activa |
| [!UICONTROL Action] | Enumera todas las acciones que se pueden aplicar a un listado específico. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_columna. Opciones: `Edit Price Rule` / `Delete Price Rule` |
