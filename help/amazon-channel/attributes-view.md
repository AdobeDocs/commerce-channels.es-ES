---
title: Atributos
description: La Sales Channel de Amazon proporciona la pestaña [!UICONTROL Attributes] para supervisar la lista de atributos de Amazon y comercio y cómo se asignan para la coincidencia de productos.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Atributos

La vista _[!UICONTROL Attributes]_muestra la lista de atributos de Amazon y [!DNL Commerce]. La lista también indica los atributos que se han asignado para la coincidencia de productos. Para obtener más información, consulte [Administrar atributos](./managing-attributes.md).

![Vista Atributos](assets/amazon-attributes-view.png)

Desde la vista _[!UICONTROL Attributes]_, revise la configuración de atributos en la tabla y [cree o edite](./creating-attributes.md) un atributo.

## Ver la lista de atributos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Haga clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y revise la lista de atributos.

1. Cree o edite un atributo según sea necesario:

   - Para [crear](./creating-attributes.md#create-an-attribute) y definir los valores de atributo coincidentes para el atributo, haga clic en **[!UICONTROL Create]**.

   - Para desactivar o [editar la configuración](./creating-attributes.md#edit-an-attribute) o los valores de atributo coincidentes para el atributo, haga clic en **[!UICONTROL Edit]**.

      La edición de un atributo incluye el cambio de la asignación de atributos para la coincidencia de productos.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Country] | El país para la actividad de ventas definido en **[!DNL Amazon Marketplace]País** durante la [integración del almacén](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico generado por [!DNL Commerce] cuando se crea el atributo. |
| [!UICONTROL Amazon Attribute Name] | Nombre del atributo importado de Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Si está asignado, el atributo [!DNL Commerce] asignado al _[!UICONTROL Amazon Attribute Name]_para asignar al catálogo y listar productos coincidentes. |
| [!UICONTROL Overwrite Magento Values] | Si el atributo se establece en `Overwrite Existing Magento Values` en Configuración de atributos, la tabla muestra `Enabled`. Enabled significa que cuando se recibe información actualizada del producto para el atributo de Amazon, la nueva información actualiza (sobrescribe) la información correspondiente del producto en su catálogo [!DNL Commerce]. También puede afectar a sus productos enumerados en sus [!DNL Commerce] tiendas. |
| Estado | Indica si los valores de atributo se han importado en [!DNL Commerce] y se han asignado a un atributo [!DNL Commerce]. Opciones: `Enabled` / `Disabled` |
| Acción | Indica las opciones de tarea disponibles para el atributo. Opciones: `Create` / `Edit` |
