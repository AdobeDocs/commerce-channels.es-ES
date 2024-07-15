---
title: Atributos para listados de Amazon
description: La Sales Channel de Amazon proporciona la ficha [!UICONTROL Attributes] para supervisar la lista de atributos de Amazon y Commerce y cómo se asignan para la coincidencia de productos.
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Atributos para listados de Amazon

La vista _[!UICONTROL Attributes]_muestra su lista de atributos Amazon y [!DNL Commerce]. La lista también indica los atributos que se han asignado para la coincidencia de productos. Para obtener más información, consulte [Administrar atributos](./managing-attributes.md).

![Vista de atributos](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

Desde la vista _[!UICONTROL Attributes]_, revise la configuración de atributos en la tabla y [cree o edite](./creating-attributes.md) un atributo.

## Ver la lista de atributos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic en **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y revise la lista de atributos.

1. Cree o edite un atributo según sea necesario:

   - Para [crear](./creating-attributes.md#create-an-attribute) y definir los valores de atributo coincidentes para el atributo, haga clic en **[!UICONTROL Create]**.

   - Para desactivar o [editar la configuración](./creating-attributes.md#edit-an-attribute) o los valores de atributo coincidentes del atributo, haga clic en **[!UICONTROL Edit]**.

     La edición de un atributo incluye el cambio de la asignación de atributos para la coincidencia de productos.

| Campo | Descripción |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | El país para la actividad de ventas definida en **[!DNL Amazon Marketplace]País** durante la [integración de tiendas](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico generado por [!DNL Commerce] cuando se crea el atributo. |
| [!UICONTROL Amazon Attribute Name] | Nombre del atributo importado de Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Si se asigna, el atributo [!DNL Commerce] se asigna al _[!UICONTROL Amazon Attribute Name]_para que coincida con el catálogo y los productos de listado. |
| [!UICONTROL Overwrite Magento Values] | Si el atributo se establece en `Overwrite Existing Magento Values` en la configuración de atributos, la tabla muestra `Enabled`. Habilitado significa que cuando se recibe información de producto actualizada para el atributo desde Amazon, la nueva información actualiza (sobrescribe) la información correspondiente para el producto en el catálogo [!DNL Commerce]. También puede afectar a los productos que aparecen en las tiendas [!DNL Commerce]. |
| Estado | Indica si los valores de atributo se importaron en [!DNL Commerce] y se asignaron a un atributo [!DNL Commerce]. Opciones: `Enabled` / `Disabled` |
| Acción | Indica las opciones de tarea disponibles para el atributo. Opciones: `Create` / `Edit` |
