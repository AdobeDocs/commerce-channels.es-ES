---
title: Configuración general de la regla de precios
description: Utilice la configuración general de la regla de precio para definir las características principales de una regla de precio de anuncio.
redirect_from: /sales-channels/asc/ob-pricing-rules-general-settings.html: 
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 0%

---

# Configuración general de la regla de precios

Defina el nombre, la descripción, las fechas activas y la prioridad de la regla.

## Completar la sección Configuración general de la regla de precio

1. Para **[!UICONTROL Rule Name]** (obligatorio), introduzca el nombre de la regla.

   Este nombre es solo para fines de identificación interna. Cuanto más descriptivo sea el nombre de la regla, mejor.

1. Para **[!UICONTROL Description]**, introduzca una descripción detallada de la regla.

   Esta descripción podría incluir información sobre los productos que cumplen los requisitos, las fechas activas, la fórmula para calcular el precio ajustado o cualquier otra información que considere útil si desea modificar la regla.

1. Para **[!UICONTROL Status]**, elija una opción:

   - `Active` - Seleccione esta opción cuando desee que la regla de precios se aplique a sus productos aptos y ajuste los precios de los anuncios antes de publicarlos en Amazon.

   - `Inactive` - Seleccione esta opción cuando no desee que la regla de precios se aplique a sus productos aptos. Es muy probable que esta opción se utilice al modificar una regla de precios o desactivarla después de una promoción limitada.

1. Para **[!UICONTROL From]** y **[!UICONTROL To]**, introduzca una fecha de inicio y finalización para la regla de precios.

   También puede hacer clic en el icono de calendario para seleccionar una fecha del calendario dinámico. Esta opción de inicio y parada automática es útil cuando se configuran promociones de tiempo limitado o de temporada con fechas de inicio y finalización definidas.

1. Para **[!UICONTROL Priority]**, introduzca un valor numérico para la prioridad de regla.

   El valor de prioridad igual a `1` es la prioridad más alta. Cuando tiene varias reglas de precios activas, puede utilizar este valor de prioridad para determinar qué regla se aplica primero. Este campo es necesario para utilizar la función _[!UICONTROL Discard Subsequent Rules]_.

1. Para **[!UICONTROL Discard Subsequent Rules]**, elija una opción:

   - `Yes` - Seleccione esta opción cuando no desee que se apliquen otras reglas de precios que puedan aplicarse a un producto. Descartar reglas posteriores significa que, si se aplican varias reglas de precios al mismo producto, solo se aplica al producto la regla de precios con el valor de prioridad definido más alto. Esta opción evita que se apilen varias reglas de precios y proporciona descuentos adicionales no deseados.

   - `No` - Seleccione esta opción cuando desee permitir que se apliquen varias reglas de precios al mismo producto. Esta opción podría resultar en apilar y proporcionar varios descuentos a aplicar.

>[!NOTE]
>
>Para descartar reglas posteriores, una regla de precios debe tener un valor definido de **Priority**.

![Configuración general de la regla de precios](assets/amazon-pricing-rule-general.png)

| Campo | Descripción |
|---|---|
| [!UICONTROL Rule Name] | (Obligatorio) Introduzca un nombre para la regla, que se utiliza con fines de identificación interna. Cuanto más descriptivo sea el nombre de la regla, mejor. Por ejemplo, &quot;25% de descuento en la venta de libros de fin de año&quot;. |
| [!UICONTROL Description] | Introduzca una descripción detallada que explique la regla (también utilizada con fines internos). Por ejemplo, &quot;Venta al final del año, 25 % de descuento en todos los artículos de la categoría Libros&quot;. |
| [!UICONTROL Status] | Opciones:<ul><li>**[!UICONTROL Inactive]** - La regla de precios no se aplica a sus anuncios. Esta opción se puede utilizar al modificar una regla de precios o desactivarla después de una promoción limitada.</li><li>**[!UICONTROL Active]** - La regla de precios se aplica a sus anuncios y ajusta los precios de los anuncios antes de publicarlos en Amazon.</li></ul> |
| [!UICONTROL From] | Introduzca la fecha de inicio en la que comienza la regla de precios. Por ejemplo, para tener una venta durante el último mes del año, establecería la fecha `From` en 1 de diciembre para que la regla de precios se aplicara automáticamente a sus anuncios de Amazon a partir del 1 de diciembre. |
| [!UICONTROL To] | Introduzca la fecha de finalización cuando finalice la regla de precios. Continuando con el ejemplo anterior, para limitar la venta al último mes del año, establecería la fecha `To` como 31 de diciembre, por lo que la regla de precios caduca el 31 de diciembre. |
| [!UICONTROL Priority] | Introduzca un valor para la prioridad de regla de precios. Un valor de prioridad igual a `1` es la prioridad más alta. Cuando tiene varias reglas de precios, puede utilizar el valor de prioridad para determinar qué regla se aplica primero. Este campo es necesario para utilizar la función **Descartar reglas posteriores**. |
| [!UICONTROL Discard Subsequent Rules] | Se utiliza para permitir o evitar que se apilen varias reglas de precios y para proporcionar descuentos adicionales. Para descartar reglas posteriores, una regla de precios debe tener un valor definido para **[!UICONTROL Priority]**. Opciones:<ul><li>**[!UICONTROL Yes]** - Elija cuándo no desea que se apliquen otras reglas de precios que puedan aplicarse a un producto. Descartar reglas posteriores significa que, cuando se aplican varias reglas de precios al mismo producto, solo se aplica la regla de precios con el valor de prioridad definido más alto.</li><li>**[!UICONTROL No]** - Elija cuándo desea permitir que se apliquen varias reglas de precios al mismo producto. Esta opción podría resultar en apilamiento y en varios descuentos aplicados al precio de su anuncio.</li></ul> |
