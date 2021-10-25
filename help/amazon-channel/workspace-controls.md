---
title: Controles de Workspace
description: La Sales Channel de Amazon proporciona controles de espacio de trabajo que le ayudan a localizar listas, ver información y aplicar acciones fácilmente.
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# Controles de Workspace

El canal de ventas de Amazon [página principal](./amazon-sales-channel-home.md) tiene algunos controles comunes del espacio de trabajo, como Filtros, Vista predeterminada, Columnas y Exportar. No todas las páginas tienen las mismas opciones de control.

![Ejemplos de control de espacio de trabajo de Sales Channel de Amazon](assets/amazon-workspace-controls.png)

## Acciones

La variable _[!UICONTROL Actions]_El selector proporciona una lista de las acciones que están disponibles para un usuario en una página. Cuando se elige, la acción se aplica a todos los elementos seleccionados. Para aplicar una acción a un elemento específico, active la casilla de verificación de la primera columna de cada elemento y elija una opción en_[!UICONTROL Actions]_.

Por ejemplo, cuando el selector se muestra en la _[!UICONTROL Attributes]_, incluye el_[!UICONTROL Re-import Product Attribute Values]_ acción. Al seleccionar esta acción, se envía el ping correspondiente a [!DNL Amazon Seller Central] y actualiza el [!DNL Commerce] Los datos de cada uno de los elementos del almacén de Amazon marcados en la columna de la izquierda.

![Ejemplo de menú Acciones](assets/amazon-sales-channel-home-actions-option.png)

## Filtros

La variable _[!UICONTROL Filters]_control muestra las opciones para reducir los datos que se muestran en la tabla. Las opciones de filtro se basan en las columnas seleccionadas en el control Columns . Las opciones de filtro solo se muestran para las columnas habilitadas en el control Columnas .

Los controles Filtros pueden incluir calendarios dinámicos para reducir los datos de fechas especificadas, menús desplegables para columnas que tienen selecciones predefinidas y campos de texto libre que pueden contener datos personalizados.

El siguiente ejemplo muestra la configuración para filtrar la lista de pedidos para mostrar solo los pedidos que cumplen los siguientes criterios:

- Pedidos realizados entre el 01/02/2019 y el 07/2/2019, y
- Pedidos con un comprador llamado `Smith`y
- Pedidos con estado de `Shipped`.

Cuando haya configurado las opciones de filtrado, haga clic en **[!UICONTROL Apply Filters]** para filtrar los datos enumerados. Haga clic en Cancelar para salir del control Filtros sin aplicarlo.

![Ejemplo de control de filtros](assets/workspace-controls-filters.png)

Después de aplicar filtros a los datos, **[!UICONTROL Active Filters]** aparecerá la información. Puede hacer clic en el botón ![Icono Borrar filtros](assets/x-icon-clear-filters.png) icono para borrar una opción de filtro específica o haga clic en **[!UICONTROL Clear All]** para borrar todos los filtros aplicados.

![Ejemplo de filtros activos](assets/applied-filters-line.png)

## Ver

El control Ver se basa en las columnas predeterminadas de la página, por lo que se denomina Vista predeterminada. Puede agregar o quitar columnas disponibles mediante el control Columns . Al personalizar las columnas, puede guardar la vista como una vista personalizada en el control Ver.

Cuando se agregan o eliminan las columnas de la página, se muestra:

1. Haga clic en **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. Introduzca un nombre para la vista.

1. Para guardar la vista personalizada, haga clic en el icono de flecha.

![Ver ejemplo de control](assets/workspace-controls-view.png)

En este ejemplo, la variable _ID de pedido_ se añade en el control Column y se guarda como una vista personalizada. Observe que después de guardar el nombre de vista personalizado, el nombre de la vista cambió de _Vista predeterminada_ al nombre introducido.

Puede alternar entre las vistas seleccionando la vista deseada en la _[!UICONTROL View]_para abrir el Navegador.

Si desea eliminar o cambiar el nombre de la vista personalizada, haga clic en el icono de lápiz. A continuación, puede introducir un nombre diferente o hacer clic en el icono de la papelera para eliminar la vista personalizada. La vista predeterminada no se puede eliminar.

## Columnas

El control Columns permite agregar o quitar columnas de datos de la visualización de la página. Cada página de canal de ventas de Amazon tiene una combinación preestablecida de columnas de datos, pero la mayoría de las páginas tienen columnas adicionales disponibles. Si no hay columnas adicionales disponibles, puede quitar las columnas predeterminadas de la visualización.

El siguiente ejemplo muestra un control Columns . Las opciones seleccionadas corresponden a los encabezados de columna que se muestran en la página.

- Para agregar una columna de datos a la página, active la casilla de verificación.
- Para quitar una columna de datos de la página, no active la casilla de verificación.

![Ejemplo de control de columnas](assets/workspace-controls-columns.png)

Los cambios en la casilla de verificación se muestran inmediatamente. Si realiza cambios y sale de la página, la página vuelve a la visualización de la columna predeterminada. Para los cambios que realice con regularidad, puede guardar los cambios de las columnas como una vista personalizada en el control Ver. A continuación, puede alternar en el control Ver sin tener que agregar o quitar columnas manualmente.

Puede hacer clic en **[!UICONTROL Reset]** para volver a establecer las opciones en la configuración predeterminada, o puede hacer clic en **[!UICONTROL Cancel]** para salir sin los cambios.

## Exportar

La opción Exportar permite exportar los datos a un archivo de datos que se pueda importar a un software de terceros o a una base de datos independiente. Los datos exportados se limitan a los datos mostrados. Si es necesario, asegúrese de agregar o quitar columnas antes de utilizar el control Export .

Cuando esté listo para exportar los datos, elija una opción de formato de exportación y haga clic en **[!UICONTROL Export]**.

- CSV: archivo de valores separados por comas que contiene datos de texto sin formato
- Excel XML: formato de datos de hoja de cálculo basado en XML (normalmente se utiliza para usuarios de Excel)

El archivo de datos generado se guarda automáticamente en la carpeta designada para las descargas.

![Control de exportación](assets/workspace-controls-export.png)
