---
title: 'Canal de ventas de Amazon: controles de Workspace'
description: La Sales Channel de Amazon proporciona controles de espacio de trabajo que ayudan a localizar listados, ver información y aplicar acciones de forma sencilla.
feature: Sales Channels
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Controles de Workspace

El canal de ventas de Amazon [página principal](./amazon-sales-channel-home.md) tiene algunos controles comunes del espacio de trabajo, como Filtros, Vista predeterminada, Columnas y Exportar. No todas las páginas tienen las mismas opciones de control.

![ejemplos de control del espacio de trabajo de Sales Channel Amazon](assets/amazon-workspace-controls.png){width="600" zoomable="yes"}

## Acciones

El selector _[!UICONTROL Actions]_proporciona una lista de acciones disponibles para un usuario en una página. Cuando se elige, la acción se aplica a todos los elementos seleccionados. Para aplicar una acción a un elemento específico, active la casilla de verificación de la primera columna de cada elemento y elija una opción en_[!UICONTROL Actions]_.

Por ejemplo, cuando el selector se muestra en la página _[!UICONTROL Attributes]_, incluye la acción_[!UICONTROL Re-import Product Attribute Values]_. Al elegir esta acción, se realiza un ping a la cuenta [!DNL Amazon Seller Central] correspondiente y se actualizan los datos de [!DNL Commerce] para cada uno de los elementos del almacén de Amazon marcados en la columna del lado izquierdo.

![Ejemplo de menú de acciones](assets/amazon-sales-channel-home-actions-option.png){width="500"}

## Filtros

El control _[!UICONTROL Filters]_muestra opciones para reducir los datos mostrados en la tabla. Las opciones de filtro se basan en las columnas seleccionadas en el control Columnas. Las opciones de filtro sólo se muestran para las columnas habilitadas en el control Columnas.

Los controles de filtros pueden incluir calendarios dinámicos para reducir los datos de fechas especificadas, menús desplegables para columnas con selecciones predefinidas y campos de texto libre que pueden contener datos personalizados.

El ejemplo siguiente muestra la configuración para filtrar la lista de pedidos de modo que se muestren únicamente los pedidos que cumplan los siguientes criterios:

- Pedidos realizados entre el 01/2/2019 y el 07/2/2019, y
- Pedidos con un comprador denominado `Smith`, y
- Pedidos con un estado de `Shipped`.

Cuando tenga establecidas las opciones de filtrado, haga clic en **[!UICONTROL Apply Filters]** para filtrar los datos enumerados. Haga clic en Cancelar para salir del control Filters sin aplicar.

![Ejemplo de control de filtros](assets/workspace-controls-filters.png){width="600" zoomable="yes"}

Después de aplicar filtros a los datos, aparecerá la información de **[!UICONTROL Active Filters]**. Puede hacer clic en el icono ![Borrar filtros](assets/x-icon-clear-filters.png) para borrar una opción de filtro específica, o bien hacer clic en **[!UICONTROL Clear All]** para borrar todos los filtros aplicados.

![Ejemplo de filtros activos](assets/applied-filters-line.png){width="700"}

## Ver

El control View se basa en las columnas predeterminadas de la página, por lo que recibe el nombre de Vista predeterminada. Puede agregar o quitar columnas disponibles mediante el control Columns. Al personalizar las columnas, puede guardar la vista como una vista personalizada en el control View.

Cuando tenga las columnas añadidas o eliminadas de la página, aparecerá lo siguiente:

1. Haga clic en **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. Introduzca un nombre para la vista.

1. Para guardar la vista personalizada, haga clic en el icono de flecha.

![Ver ejemplo de control](assets/workspace-controls-view.png)

En este ejemplo, la columna _Id. de pedido_ se agrega en el control Columna y se guarda como una vista personalizada. Observe que después de guardar el nombre de vista personalizada, el nombre de la vista cambió de _Vista predeterminada_ al nombre escrito.

Puede alternar entre las vistas seleccionando la vista deseada en el menú _[!UICONTROL View]_.

Si desea eliminar o cambiar el nombre de la vista personalizada, haga clic en el icono de lápiz. A continuación, puede introducir un nombre diferente o hacer clic en el icono de la papelera para eliminar la vista personalizada. No se puede eliminar la vista predeterminada.

## Columnas

El control Columns permite agregar o quitar columnas de datos de la presentación de la página. Cada página del canal de ventas de Amazon tiene una combinación preestablecida de columnas de datos, pero la mayoría de las páginas tienen columnas adicionales disponibles. Si no hay columnas adicionales disponibles, aún puede quitar las columnas predeterminadas de la visualización.

En el ejemplo siguiente se muestra un control Columns. Las opciones seleccionadas corresponden a los encabezados de columna que se muestran en la página.

- Para añadir una columna de datos a la página, marque la casilla de verificación.
- Para quitar una columna de datos de la página, no marque la casilla de verificación.

![Ejemplo de control de columnas](assets/workspace-controls-columns.png){width="400"}

Los cambios de casilla de verificación se muestran inmediatamente. Si realiza cambios y sale de la página, la página vuelve a la presentación de columna predeterminada. Para los cambios que realice con regularidad, puede guardar los cambios de las columnas como una vista personalizada en el control View. A continuación, puede alternar en el control View sin tener que agregar o quitar columnas manualmente.

Puede hacer clic en **[!UICONTROL Reset]** para volver a establecer las opciones en la configuración predeterminada, o bien puede hacer clic en **[!UICONTROL Cancel]** para salir sin realizar cambios.

## Exportar

La opción Exportar permite exportar los datos a un archivo de datos que se pueda importar a un software de terceros o a una base de datos independiente. Los datos exportados se limitan a los datos mostrados. Si es necesario, asegúrese de agregar o quitar columnas antes de utilizar el control Export.

Cuando esté listo para exportar los datos, elija una opción de formato de exportación y haga clic en **[!UICONTROL Export]**.

- CSV: archivo de valores separados por comas que contiene datos de texto sin formato
- XML de Excel: formato de datos de hoja de cálculo basado en XML (normalmente utilizado por los usuarios de Excel)

El archivo de datos generado se guarda automáticamente en la carpeta designada para las descargas.

![Control de exportación](assets/workspace-controls-export.png){width="250"}
