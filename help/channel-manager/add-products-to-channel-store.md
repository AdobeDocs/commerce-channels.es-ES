---
title: Añadir productos al Administrador de canales
description: '''Crear surtido de productos para [!DNL Walmart Marketplace] ventas añadiendo productos del catálogo al canal de ventas configurado en Channel Manager."'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Añadir productos a [!DNL Channel Manager]

Para añadir productos a [!DNL Walmart Marketplace] canal de ventas, selecciónelos en [!DNL Commerce] catálogo de productos e importarlos en [!DNL Channel Manager].
El proceso de importación puede tardar hasta 30 minutos o más en función de la cantidad de productos que seleccione.

## Requisito previo

**[Asignar atributos de catálogo](map-catalog-attributes.md)**: en el [!DNL Channel Settings] , asigne al menos un atributo del [!DNL Commerce] Catálogo de productos a uno de los identificadores de producto de Walmart requeridos: GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de anuncios

[!DNL Commerce] los listados de productos deben tener la siguiente configuración de atributos requerida:

- **[!UICONTROL Connect to Channel Manager]** el atributo está habilitado

- Proporcione valores válidos para los atributos de Walmart necesarios.

   - Al menos un atributo de producto que coincida con uno de los necesarios [!DNL Walmart Marketplace] identificadores de producto: GTIN, ISBN, ISSN, UPC, EAN.

   - El precio del producto especificado en un máximo de dos decimales, por ejemplo `9.99`

   - Peso del producto especificado en un máximo de dos decimales, por ejemplo `1.25`

>[!TIP]
>
>Si desea obtener más información sobre cómo optimizar anuncios para su canal de ventas, consulte la [Guía de optimización de calidad de lista de Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Añadir productos

1. En un almacén de canales de ventas conectado, seleccione **Añadir productos** para abrir el catálogo de productos.

   ![Añadir productos a la tienda de canales de ventas](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   El catálogo se abre en una nueva pestaña.

1. En la cuadrícula de productos del catálogo, seleccione los productos que desea vender [!DNL Walmart Marketplace].

   ![Envíe productos a la tienda de canales de ventas](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Habilite la **[!UICONTROL Connect to Channel Manager]** para los elementos seleccionados.

   - Desde **[!UICONTROL Actions]**, seleccione **[!UICONTROL Update attributes]**.

   - Desplácese hasta **[!UICONTROL Connect to Channel Manager]** y habilitarlo.

   - Compruebe que los atributos del producto incluyen al menos uno de los necesarios [!DNL Walmart Product IDs].

   - Seleccionar **[!UICONTROL Save]**.

     Aparece un mensaje de confirmación.

     ![Importación de productos del catálogo al mensaje de confirmación de canal de ventas](assets/product-import-from-catalog-confirmation.png){width="400"}

     Si el mensaje indica que la actualización está programada, utilice el [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] para procesar la actualización inmediatamente.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. Una vez finalizada la operación de importación, compruebe los productos que ha agregado volviendo a [!DNL Channel Manager] y seleccionando **[!UICONTROL Listings]**.

   Inicialmente, los productos se encuentran en *Borrador* estado. Seleccionar **[!UICONTROL Refresh products]** para actualizar la tabla.

1. Actualice la vista para mostrar los nuevos productos añadidos al Administrador de canales seleccionando el **[!UICONTROL Draft]** tarjeta de estado.

   ![Productos importados al canal de ventas conectado](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


