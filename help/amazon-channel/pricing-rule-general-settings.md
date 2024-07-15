---
title: 'Sales Channel de Amazon: configuración general de la regla de precios'
description: Utilice la configuración general de la regla de precios para definir las características principales de una regla de precios de listado.
feature: Sales Channels, Price Rules, Configuration
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Configuración general de reglas de precios

Defina el nombre, la descripción, las fechas activas y la prioridad de la regla.

## Rellene la sección Configuración general de la regla de precio

1. Para **[!UICONTROL Rule Name]** (obligatorio), escriba el nombre de la regla.

   Este nombre es solo para propósitos de identificación interna. Cuanto más descriptivo sea el nombre de la regla, mejor.

1. Para **[!UICONTROL Description]**, escriba una descripción detallada de la regla.

   Esta descripción puede incluir información sobre los productos aptos, las fechas de actividad, la fórmula para calcular el precio ajustado o cualquier otra información que le resulte útil si desea modificar la regla.

1. Para **[!UICONTROL Status]**, elija una opción:

   - `Active`: elige esta opción cuando quieras que la regla de precios se aplique a tus productos aptos y ajuste los precios del anuncio antes de publicarlo en Amazon.

   - `Inactive`: elige esta opción cuando no quieras que la regla de precios se aplique a tus productos aptos. Es muy probable que esta opción se utilice al modificar una regla de asignación de precios o al desactivarla después de una promoción limitada.

1. Para **[!UICONTROL From]** y **[!UICONTROL To]**, escriba una fecha de inicio y una de finalización para la regla de precios.

   También puede hacer clic en el icono de calendario para seleccionar una fecha del calendario dinámico. Esta opción de inicio y parada automática es beneficiosa cuando se configuran promociones de tiempo limitado o de temporada con fechas de inicio y finalización definidas.

1. Para **[!UICONTROL Priority]**, escriba un valor numérico para la prioridad de regla.

   El valor de prioridad igual a `1` es la prioridad más alta. Cuando tiene varias reglas de asignación de precios activas, puede utilizar este valor de prioridad para determinar qué regla se aplica primero. Este campo es necesario para utilizar la característica _[!UICONTROL Discard Subsequent Rules]_.

1. Para **[!UICONTROL Discard Subsequent Rules]**, elija una opción:

   - `Yes`: elija esta opción cuando no desee que se apliquen otras reglas de precios que se puedan aplicar a un producto. Descartar las reglas siguientes significa que, si se aplican varias reglas de asignación de precios al mismo producto, solo se aplica al producto la regla de asignación de precios con el valor de prioridad definido más alto. Esta opción evita que se apilen varias reglas de precios y proporciona descuentos adicionales no deseados.

   - `No`: elija esta opción cuando desee permitir que se apliquen varias reglas de precios al mismo producto. Esta opción podría provocar que se apilen y que se apliquen varios descuentos.

>[!NOTE]
>
>Para descartar las reglas siguientes, una regla de asignación de precios debe tener un valor definido de **Prioridad**.

![Configuración general de la regla de precios](assets/amazon-pricing-rule-general.png){width="600" zoomable="yes"}

| Campo | Descripción |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Name] | (Obligatorio) Introduzca un nombre para la regla, que se utilizará con fines de identificación interna. Cuanto más descriptivo sea el nombre de la regla, mejor. Por ejemplo, &quot;25% de descuento en la venta de libros al final del año&quot;. |
| [!UICONTROL Description] | Introduzca una descripción detallada que explique la regla (también utilizada con fines internos). Por ejemplo, &quot;Venta de fin de año, 25 % de descuento en todos los artículos de la categoría Libros&quot;. |
| [!UICONTROL Status] | Opciones:<ul><li>**[!UICONTROL Inactive]**: la regla de precios no se aplica a tus anuncios. Esta opción se puede utilizar cuando se modifica una regla de asignación de precios o se desactiva después de una promoción limitada.</li><li>**[!UICONTROL Active]**: la regla de precios se aplica a los anuncios y ajusta los precios del anuncio antes de publicarlo en Amazon.</li></ul> |
| [!UICONTROL From] | Introduzca la fecha de inicio en la que comienza la regla de asignación de precios. Por ejemplo, para realizar un descuento durante el último mes del año, establecerías la fecha de `From` en el 1 de diciembre para que la regla de precios se aplique automáticamente a tus anuncios de Amazon a partir del 1 de diciembre. |
| [!UICONTROL To] | Introduzca la fecha de finalización en la que finaliza la regla de asignación de precios. Siguiendo con el ejemplo anterior, para limitar la venta al último mes del año, establecería la fecha `To` como 31 de diciembre, de modo que la regla de asignación de precios caduca el 31 de diciembre. |
| [!UICONTROL Priority] | Introduzca un valor para la prioridad de la regla de asignación de precios. Un valor de prioridad igual a `1` es la prioridad más alta. Cuando tiene varias reglas de asignación de precios, puede utilizar el valor de prioridad para determinar qué regla se aplica primero. Este campo es necesario para usar la característica **Descartar reglas subsiguientes**. |
| [!UICONTROL Discard Subsequent Rules] | Se utiliza para permitir o evitar que se apilen varias reglas de precios y proporcionar descuentos adicionales. Para descartar las reglas siguientes, una regla de precios debe tener un valor definido para **[!UICONTROL Priority]**. Opciones:<ul><li>**[!UICONTROL Yes]**: elija cuándo no desea que se apliquen otras reglas de precios que puedan aplicarse a un producto. Descartar las reglas siguientes significa que, cuando se aplican varias reglas de asignación de precios al mismo producto, solo se aplica la regla de asignación de precios con el valor de prioridad definido más alto.</li><li>**[!UICONTROL No]**: elija cuándo desea permitir que se apliquen varias reglas de precios al mismo producto. Esta opción podría provocar la acumulación y la aplicación de varios descuentos al precio del anuncio.</li></ul> |
