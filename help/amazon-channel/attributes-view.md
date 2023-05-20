---
title: Atributos
description: La Sales Channel de Amazon proporciona el [!UICONTROL Attributes] para monitorizar la lista de atributos de Amazon y Commerce y cómo se asignan para la coincidencia de productos.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Atributos

El _[!UICONTROL Attributes]_La vista muestra su lista de Amazon y [!DNL Commerce] atributos. La lista también indica los atributos que se han asignado para la coincidencia de productos. Para obtener más información, consulte [Administrar atributos](./managing-attributes.md).

![Vista Atributos](assets/amazon-attributes-view.png)

Desde el _[!UICONTROL Attributes]_vea, y revise la configuración de atributos en la tabla y [crear o editar](./creating-attributes.md) un atributo.

## Ver la lista de atributos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Clic **[!UICONTROL Attributes]** en el menú de la izquierda, busque un atributo de Amazon y revise la lista de atributos.

1. Cree o edite un atributo según sea necesario:

   - Hasta [crear](./creating-attributes.md#create-an-attribute) y defina Valores de atributo coincidentes para el atributo, haga clic en **[!UICONTROL Create]**.

   - Para desactivar o [editar la configuración](./creating-attributes.md#edit-an-attribute) o Valores de atributo coincidentes para el atributo, haga clic en **[!UICONTROL Edit]**.

      La edición de un atributo incluye el cambio de la asignación de atributos para la coincidencia de productos.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Country] | El país para la actividad de ventas definida en  **[!DNL Amazon Marketplace]País** durante [integración de tienda](./store-integration.md). |
| [!UICONTROL ID] | Valor de atributo genérico generado por [!DNL Commerce] cuando se crea el atributo. |
| [!UICONTROL Amazon Attribute Name] | Nombre del atributo importado de Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Si está asignado, la variable [!DNL Commerce] atributo asignado a asignar a _[!UICONTROL Amazon Attribute Name]_para productos de catálogo y listado coincidentes. |
| [!UICONTROL Overwrite Magento Values] | Si el atributo está establecido en `Overwrite Existing Magento Values` en la Configuración de atributos, la tabla muestra `Enabled`. Habilitado significa que cuando se recibe información de producto actualizada para el atributo desde Amazon, la nueva información actualiza (sobrescribe) la información correspondiente para el producto en su [!DNL Commerce] catálogo. También puede afectar a los productos enumerados en su [!DNL Commerce] tiendas. |
| Estado | Indica si los valores de atributo se han importado en [!DNL Commerce] y asignado a un [!DNL Commerce] atributo. Opciones: `Enabled` / `Disabled` |
| Acción | Indica las opciones de tarea disponibles para el atributo. Opciones: `Create` / `Edit` |
