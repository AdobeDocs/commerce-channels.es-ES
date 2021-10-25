---
title: Administrar los precios de Amazon
description: Puede establecer que los precios de sus anuncios de Amazon difieran de los de su tienda de comercio electrónico mediante las reglas de precios.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Administrar los precios de Amazon

El canal de ventas de Amazon le permite establecer reglas de precios que le permiten establecer un precio de anuncio de Amazon diferente del definido **[!UICONTROL Magento Price Source]** en su [precio de anuncio](./listing-price.md). También puede apilar varias reglas e incluso utilizar los precios inteligentes para ajustar el precio de anuncio de Amazon en función de los de los competidores [[!DNL Buy Box]](./buy-box-competitor-pricing.md) o [precio más bajo del competidor](./lowest-competitor-pricing.md).

Existen dos tipos de reglas de precios:

- [Regla de precios estándar](./standard-price-rules.md)
- [Regla de revalorización inteligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Las reglas inteligentes de revalorización no funcionan correctamente si la región de Amazon está configurada en `Inactive` , tal como está durante la incorporación. Los cálculos de precios dependen de las tarifas de envío y la región debe estar en `Active` para que las tarifas de envío se sincronicen con Amazon.
   >
   >Para actualizar el estado de su región en su cuenta de Amazon, vaya a Configuración > Información de la cuenta > Configuración de las vacaciones. Consulte [Amazon: Estado de anuncio de las vacaciones](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target=&quot;_blank&quot;} (se requiere inicio de sesión en Seller Central).

Esta función le permite manipular los precios de Amazon de forma similar a la [!DNL Commerce] [reglas de precios de catálogo](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}. Puede crear reglas complejas que le permitan cambiar los precios de productos específicos, productos dentro de categorías específicas o incluso con atributos específicos.

Puede agregar reglas de precios para sus anuncios de Amazon. Las reglas de precios se pueden usar para ajustar automáticamente los precios de los anuncios, en función de un conjunto de condiciones definidas. Las reglas de precios se activan y calculan el precio ajustado antes de que el producto aparezca en Amazon.

>[!NOTE]
>
>La fuente de precios para sus anuncios de Amazon está definida para **[!UICONTROL Magento Price Source]** en su [precio de anuncio](./listing-price.md) configuración. Cualquier cálculo de ajuste definido en la regla de precios utiliza el origen de precios como valor inicial.

Las reglas de precios le permiten establecer un precio de anuncio de Amazon diferente al de su **[!UICONTROL Magento Price Source]** en su [precio de anuncio](./listing-price.md) configuración. También puede apilar varias reglas que trabajen juntas para ajustar el precio.

Una regla de precios/reprecios requiere tres conjuntos de información durante su configuración:

- [Configuración general](./pricing-rule-general-settings.md): Define el nombre, la descripción, las fechas activas y la prioridad de una regla y establece el comportamiento de las reglas posteriores en función de su configuración de prioridad.
- [Condiciones](./pricing-rule-conditions.md): Determine qué productos cumplen los requisitos para la regla de precio.
- [Acciones](./pricing-rule-actions.md): Defina los cálculos de ajuste que se aplican al origen de precios para determinar el precio del anuncio.

Puede crear [reglas de precios estándar](./standard-price-rules.md) que ajusta automáticamente el precio de la oferta de Amazon en relación con el seleccionado **[!UICONTROL Magento Price Source]** en su [precio de anuncio](./listing-price.md) configuración. Esta función le permite manipular los precios de Amazon de forma similar a la [!DNL Commerce] [reglas de precios de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}. Puede crear reglas complejas que cambien automáticamente los precios de productos específicos, productos dentro de categorías específicas o productos con atributos específicos. Puede completar la configuración tradicional y revaluar sus productos para aumentar o disminuir en función de una cantidad fija o un porcentaje.

Otra herramienta poderosa es la [Revalorización inteligente](./intelligent-repricing-rules.md) función que ajusta el precio de su anuncio de Amazon en función de la competencia [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio o [Precio de la competencia más bajo](./lowest-competitor-pricing.md). Similar a la variable [!DNL Commerce] [reglas de precios de catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}, esta característica avanzada le permite manipular los precios de Amazon creando reglas complejas. Las reglas pueden definir el ámbito para un cambio de precio para productos específicos, productos dentro de categorías específicas o incluso con atributos de producto específicos.

Utilizar el reajuste inteligente de precios para ajustar los precios de las listas de Amazon, en función de los precios de los competidores. El canal de ventas de Amazon ha incorporado salvaguardas para que usted pueda configurar a fin de proteger los márgenes o evitar que los precios de un comerciante coincidan con los bajos comentarios. Uso [reglas de reasignación inteligentes](./intelligent-repricing-rules.md), los precios de los anuncios de Amazon se pueden manipular automáticamente como una cantidad fija o porcentual (hacia arriba o hacia abajo) o incluso sincronizarse con el [[!DNL Buy Box]](./buy-box-competitor-pricing.md) precio o [Precio de la competencia más bajo](./lowest-competitor-pricing.md) por partida. Incluso se pueden apilar reglas para proporcionar flexibilidad ilimitada.

Puede controlar aspectos importantes de las reglas, como el estado activo/inactivo, la idoneidad del sitio web, los intervalos de fechas opcionales y los niveles de prioridad opcionales (utilizados para el apilamiento de reglas).

Por ejemplo, puede definir y establecer las condiciones de una regla de precio que, cuando se cumplan las condiciones, ajuste automáticamente el precio del anuncio antes de enviarlo a Amazon.

Otra opción de precios es [anulación de precio](./overrides.md), que se establece en el nivel de anuncio individual. A [anulación de precio](./overrides.md) se puede establecer y una anulación ignora/tiene prioridad sobre todos los demás valores predeterminados, configuraciones y reglas. Un [override](./overrides.md) se puede configurar para precio, tiempo de manipulación, condición y notas del vendedor (con algunas excepciones).

![Reglas de precios](assets/amazon-pricing-rules.png)

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Name] | Nombre de la regla de precios, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | El tipo de regla definido en [Acciones de las reglas de precios](./pricing-rule-actions.md) (regla de precio estándar o regla de reprecio inteligente) |
| [!UICONTROL Is Active] | Si la regla está activa, tal como se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La prioridad sobre otras condiciones de precios, según se establece en [Configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indica si se procesan otras reglas de precios en productos aptos para esta regla, tal como se establece en [configuración general de la regla de precios](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Inicio del período de tiempo en el que la regla está activa |
| [!UICONTROL To Date] | El final del período de tiempo en el que la regla está activa |
| [!UICONTROL Action] | Enumera todas las acciones que se pueden aplicar a una lista específica. Para aplicar una acción, haga clic en **[!UICONTROL Select]** en el _[!UICONTROL Action]_para abrir el Navegador. Opciones: `Edit Price Rule` / `Delete Price Rule` |
