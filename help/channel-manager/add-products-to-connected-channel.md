---
title: Añadir productos a la tienda de canales
description: Cree una gama de productos para las ventas de Marketplace agregando productos del catálogo al canal de ventas
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# Añadir productos a la tienda de canales

En el Administrador de canales, seleccione los productos de [!DNL Commerce] catálogo de ventas de Walmart Marketplace.

Para sincronizar productos con el canal de ventas, los productos seleccionados deben tener la siguiente configuración de atributos:

- **[!UICONTROL Publish to Channel Manager]** el atributo está habilitado

- Al menos un atributo de producto debe coincidir con uno de los [atributos requeridos de Walmart Marketplace](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

Después de guardar las selecciones, el Administrador de canales importa los datos del producto en el canal. Este proceso puede tardar hasta 30 minutos.

## Agregar productos al canal de ventas

1. Abra el catálogo de productos asociado con su tienda de Channel Manager.

   En un almacén de canales de ventas conectado, seleccione **Agregar productos**.

   ![Añadir productos a un canal conectado](assets/add-initial-products-to-connected-channel.png)

   El catálogo se abre en una nueva pestaña.

1. En la cuadrícula de productos del catálogo, seleccione los productos que desea vender en Walmart Marketplace.

   ![Enviar productos al canal conectado](assets/select-products-from-catalog.png)

1. Active la variable **[!UICONTROL Publish to Channel Manager]** para los elementos seleccionados.

   - De **[!UICONTROL Actions]**, seleccione **[!UICONTROL Update attributes]**.

   - Desplácese hasta el **[!UICONTROL Publish to Channel Manager]** y actívelo.

   - Compruebe que los atributos de producto incluyen al menos uno de los ID de producto Walmart necesarios.

   - Select **[!UICONTROL Save]**.

   Aparece un mensaje de confirmación.

   ![Importación de productos del catálogo al mensaje de confirmación de canal de ventas](assets/product-import-from-catalog-confirmation.png)

   Si el mensaje indica que la actualización está programada, utilice la variable [cola:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] para procesar la actualización inmediatamente.

   ```bash
   $ bin/magento queue:consumers:start product_action_attribute.update
   ```

1. Vuelva al canal de ventas conectado en [!DNL Channel Manager].

   Una vez finalizada la operación de importación, consulte los productos desde **[!UICONTROL Listings]**. Inicialmente, los productos están en *Borrador* estado. Select [!UICONTROL Refresh products]** para actualizar la tabla.

   ![Productos importados al canal de ventas conectado](assets/products-in-marketplace-sales-channel.png)
