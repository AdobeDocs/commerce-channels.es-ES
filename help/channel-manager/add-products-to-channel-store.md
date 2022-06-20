---
title: Agregar productos al almacén de canales de ventas
description: Cree una variedad de productos para [!DNL Walmart Marketplace] ventas añadiendo productos del catálogo al canal de ventas
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: d9b39984fc7401c42fc431f35cf5649f86f4f2f9
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---


# Añadir productos a [!DNL Channel Manager]

Para agregar productos a [!DNL Walmart Marketplace] canal de ventas, selecciónelos en la lista [!DNL Commerce] catálogo de productos e impórtelos en [!DNL Channel Manager].
El proceso de importación puede tardar hasta 30 minutos o más en función de la cantidad de productos que seleccione.

## Requisito previo

**[Asignar atributos de catálogo](map-catalog-attributes.md)**—En el [!DNL Channel Settings] configuración, asigne al menos un atributo de [!DNL Commerce] catálogo de productos a uno de los identificadores de producto Walmart requeridos—-GTIN, ISBN, ISSN, UPC, EAN.

## Requisitos de listado

[!DNL Commerce] las listas de productos deben tener la siguiente configuración de atributos requerida:

- **[!UICONTROL Connect to Channel Manager]** el atributo está habilitado

- Proporcione valores válidos para los atributos Walmart requeridos.

   - Al menos un atributo de producto que coincida con uno de los requisitos [!DNL Walmart Marketplace] identificadores de producto: GTIN, ISBN, ISSN, UPC, EAN.

   - El precio del producto especificado es de un máximo de dos decimales, por ejemplo `9.99`

   - Peso del producto especificado como máximo en dos decimales, por ejemplo `1.25`

>[!TIP]
>
>Para obtener información adicional sobre la optimización de anuncios para su canal de ventas, consulte la [Guía de optimización de la calidad de la lista de Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Agregar productos

1. En un almacén de canales de ventas conectado, seleccione **Agregar productos** para abrir el catálogo de productos.

   ![Agregar productos al almacén de canales de ventas](assets/add-initial-products-to-connected-channel.png)

   El catálogo se abre en una nueva pestaña.

1. En la cuadrícula de producto del catálogo, seleccione los productos que desea vender [!DNL Walmart Marketplace].

   ![Enviar productos al almacén de canales de ventas](assets/select-products-from-catalog.png)

1. Active la variable **[!UICONTROL Connect to Channel Manager]** para los elementos seleccionados.

   - De **[!UICONTROL Actions]**, seleccione **[!UICONTROL Update attributes]**.

   - Desplácese hasta el **[!UICONTROL Connect to Channel Manager]** y actívelo.

   - Compruebe que los atributos de producto incluyen al menos uno de los requisitos [!DNL Walmart Product IDs].

   - Select **[!UICONTROL Save]**.

      Aparece un mensaje de confirmación.

      ![Importación de productos del catálogo al mensaje de confirmación de canal de ventas](assets/product-import-from-catalog-confirmation.png)

      Si el mensaje indica que la actualización está programada, utilice la variable [cola:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] para procesar la actualización inmediatamente.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. Una vez finalizada la operación de importación, compruebe los productos que ha agregado volviendo a [!DNL Channel Manager] y seleccionar **[!UICONTROL Listings]**.

   ![Productos importados al canal de ventas conectado](assets/products-in-marketplace-sales-channel.png)

   Inicialmente, los productos están en *Borrador* estado. Select **[!UICONTROL Refresh products]** para actualizar la tabla.

