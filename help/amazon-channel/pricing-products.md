---
title: Administrar los precios de Amazon
description: Puede establecer que los precios de sus anuncios de Amazon difieran de los de su tienda de comercio electrónico mediante las reglas de precios.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Administrar los precios de Amazon

El canal de ventas de Amazon le permite establecer reglas de precios que le permiten establecer un precio de anuncio de Amazon diferente del **[!UICONTROL Magento Price Source]** definido en su [precio de anuncio](./listing-price.md). También puede apilar varias reglas e incluso utilizar los precios inteligentes para ajustar el precio de listado de Amazon en función del precio [[!DNL Buy Box]](./buy-box-competitor-pricing.md) de los competidores o del [precio más bajo del competidor](./lowest-competitor-pricing.md).

Existen dos tipos de reglas de precios:

- [Regla de precios estándar](./standard-price-rules.md)
- [Regla de revalorización inteligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Las reglas inteligentes de reasignación de precios no funcionan correctamente si la región de Amazon está configurada en el estado `Inactive`, como sucede durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en estado `Active` para que las tasas de envío se sincronicen con Amazon.
   >
   >Para actualizar el estado de su región en su cuenta de Amazon, vaya a Configuración > Información de la cuenta > Configuración de las vacaciones. Consulte [Amazon: Estado de listado de Vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){:target=&quot;_blank&quot;} (se requiere el inicio de sesión de Seller Central).

Esta función le permite manipular los precios de Amazon de una manera similar a las [!DNL Commerce] [reglas de precios de catálogo](https://docs.magento.com/user-guide/catalog/pricing.html){:target=&quot;_blank&quot;}. Puede crear reglas complejas que le permitan cambiar los precios de productos específicos, productos dentro de categorías específicas o incluso con atributos específicos.

Puede agregar reglas de precios para sus anuncios de Amazon. Las reglas de precios se pueden usar para ajustar automáticamente los precios de los anuncios, en función de un conjunto de condiciones definidas. Las reglas de precios se activan y calculan el precio ajustado antes de que el producto aparezca en Amazon.

>[!NOTE]
>
>La fuente de precios de sus anuncios de Amazon se define para **[!UICONTROL Magento Price Source]** en su configuración [precio de venta](./listing-price.md). Cualquier cálculo de ajuste definido en la regla de precios utiliza el origen de precios como valor inicial.

Las reglas de precios le permiten establecer un precio de listado de Amazon diferente al **[!UICONTROL Magento Price Source]** en su configuración [precio de listado](./listing-price.md). También puede apilar varias reglas que trabajen juntas para ajustar el precio.

Una regla de precios/reprecios requiere tres conjuntos de información durante su configuración:

- [Configuración](./pricing-rule-general-settings.md) general: Define el nombre, la descripción, las fechas activas y la prioridad de una regla y establece el comportamiento de las reglas posteriores en función de su configuración de prioridad.
- [Condiciones](./pricing-rule-conditions.md): Determine qué productos cumplen los requisitos para la regla de precio.
- [Acciones](./pricing-rule-actions.md): Defina los cálculos de ajuste que se aplican al origen de precios para determinar el precio del anuncio.

Puede crear [reglas de precios estándar](./standard-price-rules.md) que ajusten automáticamente el precio de listado de Amazon en relación con el **[!UICONTROL Magento Price Source]** seleccionado en la configuración [precio de listado](./listing-price.md). Esta función le permite manipular los precios de Amazon de una manera similar a las [!DNL Commerce] [reglas de precios de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}. Puede crear reglas complejas que cambien automáticamente los precios de productos específicos, productos dentro de categorías específicas o productos con atributos específicos. Puede completar la configuración tradicional y revaluar sus productos para aumentar o disminuir en función de una cantidad fija o un porcentaje.

Otra herramienta potente es la función [Intelligent Reprice](./intelligent-repricing-rules.md) que ajusta el precio de listado de Amazon en función del precio [[!DNL Buy Box]](./buy-box-competitor-pricing.md) del competidor o [el precio más bajo del competidor](./lowest-competitor-pricing.md). Al igual que las [!DNL Commerce] [reglas de precio de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}, esta característica avanzada le permite manipular los precios de Amazon creando reglas complejas. Las reglas pueden definir el ámbito para un cambio de precio para productos específicos, productos dentro de categorías específicas o incluso con atributos de producto específicos.

Utilizar el reajuste inteligente de precios para ajustar los precios de las listas de Amazon, en función de los precios de los competidores. El canal de ventas de Amazon ha incorporado salvaguardas para que usted pueda configurar a fin de proteger los márgenes o evitar que los precios de un comerciante coincidan con los bajos comentarios. Si utiliza [reglas de reasignación de precios inteligentes](./intelligent-repricing-rules.md), los precios de las listas de Amazon se pueden manipular automáticamente como una cantidad fija o porcentual (arriba o abajo) o incluso sincronizarse con el precio [[!DNL Buy Box]](./buy-box-competitor-pricing.md) o [Precio del competidor más bajo](./lowest-competitor-pricing.md) por artículo. Incluso se pueden apilar reglas para proporcionar flexibilidad ilimitada.

Puede controlar aspectos importantes de las reglas, como el estado activo/inactivo, la idoneidad del sitio web, los intervalos de fechas opcionales y los niveles de prioridad opcionales (utilizados para el apilamiento de reglas).

Por ejemplo, puede definir y establecer las condiciones de una regla de precio que, cuando se cumplan las condiciones, ajuste automáticamente el precio del anuncio antes de enviarlo a Amazon.

Otra opción de precio es [price override](./overrides.md), que se establece en el nivel de listado individual. Se puede establecer una [anulación de precio](./overrides.md) y una anulación ignora/tiene prioridad sobre todos los demás valores predeterminados, configuraciones y reglas. Se puede configurar una [anulación](./overrides.md) para precio, tiempo de administración, condición y notas del vendedor (con algunas excepciones).

![Reglas de precios](assets/amazon-pricing-rules.png)

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Name] | Nombre de la regla de precios, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | El tipo de regla, tal como se establece en [Acciones de regla de precios](./pricing-rule-actions.md) (regla de precio estándar o regla de reprecio inteligente) |
| [!UICONTROL Is Active] | Indica si la regla está activa, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La prioridad sobre otras condiciones de precios, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica si se procesan más reglas de precios en productos aptos para esta regla, tal como se establece en [configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Inicio del período de tiempo en el que la regla está activa |
| [!UICONTROL To Date] | El final del período de tiempo en el que la regla está activa |
| [!UICONTROL Action] | Enumera todas las acciones que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en la columna _[!UICONTROL Action]_. Opciones: `Edit Price Rule` / `Delete Price Rule` |
