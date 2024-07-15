---
title: Añadir productos al Administrador de canales
description: '"Crea un surtido de productos para  [!DNL Walmart Marketplace] ventas agregando productos del catálogo al canal de ventas configurado en el Administrador de canales".'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Agregar productos a [!DNL Channel Manager]

Para agregar productos al canal de ventas [!DNL Walmart Marketplace], selecciónelos en el catálogo de productos [!DNL Commerce] e impórtelos a [!DNL Channel Manager].
El proceso de importación puede tardar hasta 30 minutos o más en función de la cantidad de productos que seleccione.

## Requisito previo

**[Asignar atributos de catálogo](map-catalog-attributes.md)**: en la configuración de [!DNL Channel Settings], asigne al menos un atributo del catálogo de productos [!DNL Commerce] a uno de los identificadores de producto de Walmart necesarios:-GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de anuncios

[!DNL Commerce] listados de productos deben tener la siguiente configuración de atributos requerida:

- El atributo **[!UICONTROL Connect to Channel Manager]** está habilitado

- Proporcione valores válidos para los atributos de Walmart necesarios.

   - Al menos un atributo de producto que coincida con uno de los identificadores de producto [!DNL Walmart Marketplace] necesarios: GTIN, ISBN, ISSN, UPC, EAN.

   - El precio del producto especificado no puede superar los dos decimales, por ejemplo `9.99`

   - Peso del producto especificado en un máximo de dos decimales; por ejemplo, `1.25`

>[!TIP]
>
>Para obtener información adicional acerca de cómo optimizar las listas para su canal de ventas, consulte la [Guía de optimización de calidad de listas de Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Añadir productos

1. En un almacén de canales de ventas conectado, seleccione **Agregar productos** para abrir el catálogo de productos.

   ![Agregar productos al almacén del canal de ventas](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   El catálogo se abre en una nueva pestaña.

1. En la cuadrícula de productos del catálogo, seleccione los productos que desea vender en [!DNL Walmart Marketplace].

   ![Enviar productos al almacén del canal de ventas](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Habilite el atributo **[!UICONTROL Connect to Channel Manager]** para los elementos seleccionados.

   - De **[!UICONTROL Actions]**, seleccione **[!UICONTROL Update attributes]**.

   - Desplácese hasta el atributo **[!UICONTROL Connect to Channel Manager]** y actívelo.

   - Compruebe que los atributos de producto incluyen al menos uno de los [!DNL Walmart Product IDs] necesarios.

   - Seleccione **[!UICONTROL Save]**.

     Aparece un mensaje de confirmación.

     ![Importación de producto del catálogo al mensaje de confirmación de canal de ventas](assets/product-import-from-catalog-confirmation.png){width="400"}

     Si el mensaje indica que la actualización está programada, use el comando [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] para procesar la actualización inmediatamente.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. Una vez finalizada la operación de importación, compruebe los productos que agregó volviendo a [!DNL Channel Manager] y seleccionando **[!UICONTROL Listings]**.

   Inicialmente, los productos están en estado *Borrador*. Seleccione **[!UICONTROL Refresh products]** para actualizar la tabla.

1. Actualice la vista para mostrar los nuevos productos agregados al Administrador de canales seleccionando la tarjeta de estado **[!UICONTROL Draft]**.

   ![Productos importados al canal de ventas conectado](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


