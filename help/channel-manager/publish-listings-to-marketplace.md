---
title: Publicar anuncios en Walmart
description: Publique anuncios de productos de Commerce en Walmart Marketplace para comenzar a vender.
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---

# Publicar anuncios en Walmart

Como otros mercados, [!DNL Walmart] permite a los vendedores de terceros enumerar los artículos que venden otros.

La plataforma utiliza identificadores de producto como UPC y GTIN para coincidir con los existentes [!DNL Walmart Marketplace] anuncios.
Para los productos coincidentes, el anuncio de Walmart Marketplace se actualiza para incluir la oferta de productos Commerce al publicar un producto de [!DNL Channel Manager].

Normalmente, las ofertas de productos con los precios más bajos aparecen primero en la [!DNL Walmart Marketplace] , pero otros factores como las revisiones también afectan a la ubicación.

## Hacer coincidir productos

Cuando coincide con productos, el Administrador de canales envía los datos del producto a [!DNL Walmart Marketplace] para buscar anuncios existentes con valores de atributo que coincidan con el atributo de producto de Commerce asignado. Los criterios de coincidencia están determinados por la variable [configuración de asignación de atributos](map-product-attributes-for-matching.md) para el canal de la tienda.

Si se encuentra una coincidencia, la lista de productos existente se actualiza para añadir la oferta.

### Requisitos previos

Antes de hacer coincidir productos, compruebe que los valores de atributos del catálogo de productos cumplen los requisitos de Walmart y configure los atributos. Consulte [Configurar la coincidencia de productos](map-product-attributes-for-matching.md)

#### Seleccionar y buscar coincidencias en los productos

1. Abra un canal de ventas conectado.

1. De **[!UICONTROL Listings]**, seleccione los productos para las coincidencias que se encuentran en *[!UICONTROL Draft]* estado.

   ![Seleccione productos de los anuncios y envíe para que coincidan](assets/products-in-marketplace-sales-channel.png)

1. Select **[!UICONTROL Match Products]**.

   Un mensaje indica el número de productos enviados para la coincidencia.

   ![Enviar productos al canal de ventas conectado](assets/products-submit-for-matching.png)

   El estado de los productos seleccionados cambia a [!UICONTROL *Procesamiento*] hasta que se complete la operación de coincidencia. Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

### Comprobar estado de coincidencia

1. Select **Actualizar productos** para actualizar el estado del producto más actual.

1. Compruebe el estado del producto.

   Una vez finalizada la coincidencia, el estado puede ser *Coincidencia* o *Error*.

   * **[!UICONTROL Match]** indica que el producto se encontró correctamente. Su oferta de producto se publicó en una lista de Walmart Marketplace existente.

   * **[!UICONTROL Error]** indica una de las siguientes opciones:

      * Se produjo un error y la operación de coincidencia falló.

      * No se encontró ninguna coincidencia.

      * Coincidencia encontrada, pero producto publicado como ensayo porque la variable [El almacén de Marketplace no está activo](walmart-prerequisites.md#walmart-marketplace-store-status).

### Comprobación de listado en Walmart

Después de hacer coincidir los productos, revise la lista de productos actualizada y verifique los detalles del producto, el precio y la cantidad de inventario de la variable [[!UICONTROL Walmart Marketplace Seller Account Items] tablero](https://seller.walmart.com/items-and-inventory/manage-items) para revisar el producto actualizado.

### Solución de problemas de errores de coincidencia de productos

Si la operación de coincidencia del producto falla, Walmart Marketplace devuelve un código de error y Channel Manager muestra el estado de error en la información de la lista del producto.

Vea los detalles de los mensajes de error pasando el ratón sobre el **Error** etiqueta de estado. Los errores comunes devueltos tienen un formato incorrecto de los valores de ID de producto o carecen de los atributos necesarios.

#### Corrección de los valores de ID de producto

| Tipo | Descripción | Ejemplo |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, el número de 12 dígitos incluyendo el dígito de comprobación. </br></br>Si su UPC tiene menos de 12 dígitos, como UPC-E, que es de 8 dígitos, agregue ceros finales para satisfacer los requisitos. | Cambiar desde `45678912345` a `045678912345` |
| GTIN | GTIN-14, el número de 14 dígitos incluyendo el dígito de comprobación. </br></br>Si su GTIN tiene menos de 14 dígitos, agregue ceros a la izquierda </br>para satisfacer los requisitos. | Cambiar `456789123456` a `0045678912345` |
| EAN | GTIN-13, el número de 13 dígitos incluyendo el dígito de comprobación. </br></br>Si el EAN tiene menos de 13 dígitos, agregue al principio </br>ceros para satisfacer los requisitos. | Cambiar desde `4567891234` a `0004567891234` |

Para obtener más información sobre los códigos de error de Walmart Marketplace, consulte la [Ayuda para vendedores de Walmart](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Cargar nuevas listas de productos

Para los productos que no coinciden con Walmart Marketplace, utilice una plantilla de Excel de categoría de producto Walmart para cargar listas de productos de forma masiva. La plantilla de Walmart se rellena con datos del catálogo de productos exportados desde la instancia de Commerce.

Para obtener nuevos listados de productos, consulte su catálogo de productos para asegurarse de que los productos que planea vender en Walmart Marketplace tengan los atributos requeridos para las listas de productos de Walmart.

**Anuncios de Walmart Marketplace: requisitos de atributos**

| **Atributo** | **Nivel de requisito** |
|--------------------------|-----------------------|
| SKU | Requerido |
| Nombre del producto | Requerido |
| Tipo de ID de producto | Requerido |
| ID del producto | Requerido |
| Marca | Requerido |
| Descripción breve | Requerido |
| Precio de venta | Requerido |
| Descripción del sitio | Requerido |
| URL de imagen principal | Requerido |
| Peso del envío | Requerido |
| Funciones principales | Recomendado |
| Número de modelo | Recomendado |
| Nombre del fabricante | Recomendado |
| Número de pieza del fabricante | Recomendado |
| Tamaño | Recomendado |
| Color | Recomendado |
| URL de imagen principal | Opcional |
| URL de imagen adicional | Opcional |
| Fabricante | Opcional |

### Requisitos previos

* Compruebe que cumple los requisitos de [Requisitos previos de Walmart](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.k2lo9voad1gx).

* En su catálogo de productos de Comercio, compruebe que la configuración del catálogo de los productos que desea incluir en Walmart Marketplace tenga todos los atributos necesarios y cumpla las directrices de contenido de Walmart Marketplace.

* Compruebe que el trabajo cron se esté ejecutando para completar la operación de exportación.

   * Para las instancias locales, consulte [Configuración y ejecución de cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   * Para obtener información sobre la infraestructura de nube de Adobe, consulte [Configurar trabajos cron](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### Cree el archivo de datos del producto para cargar

1. Desde su [Cuenta de vendedor Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller), descargue una plantilla de listado de productos desde el Centro de vendedores de Walmart.

   * En la página Artículos del catálogo de productos , seleccione **[!UICONTROL Add Items]**. A continuación, seleccione **[!UICONTROL Add items in bulk]**.

      ![Agregar elementos en la opción de forma masiva en la configuración de elementos de Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png)

   * En la página de descarga, seleccione **[!UICONTROL Full Setup]**. A continuación, seleccione una categoría de elemento y descargue la plantilla de categoría.

      ![Opción Descargar plantilla de categoría en la configuración de artículos de Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png)

   * Compruebe que la plantilla incluye los atributos requeridos y recomendados para la lista de productos.

1. En el [!DNL Commerce] Administrador, seleccione los datos de producto que desea exportar desde el sitio de Adobe Commerce.

   * En Administración, seleccione [!UICONTROL **Sistema** > Transferencia de datos > **Exportar**].

   * En el [!UICONTROL Export] en el [!UICONTROL Entity Type] campo, seleccione [!UICONTROL **Productos**].

   * En el [!UICONTROL Entity Attributes] , configure los criterios de selección para la exportación de datos del producto.
   ![Exportar la página de datos del producto en el [!UICONTROL Commerce Admin]](assets/walmart-seller-account-full-setup-download.png)

   Utilice filtros para seleccionar y configurar los valores de atributo que se aplican a las categorías de productos que vende. Asegúrese de incluir los atributos requeridos y recomendados de Walmart (consulte [Exportar datos](https://docs.magento.com/user-guide/system/data-export.html) en la Guía del usuario de Adobe Commerce para obtener instrucciones detalladas).

   Para omitir un atributo de la exportación, seleccione la opción [!UICONTROL **Excluir**] al principio de la fila.

1. Desplácese hasta el final de la tabla de atributos y seleccione [!UICONTROL **Continuar**] para iniciar la exportación de datos.

   El archivo de exportación CSV se procesa a través de una cola de mensajes utilizando trabajos cron y se guarda en la `var/export/folder`. (Consulte [Administrar colas de mensajes](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) en el *Guía para desarrolladores de Commerce*.)

1. Abra la plantilla de Excel para la categoría de producto de Walmart Marketplace y utilice las capacidades de macros de Excel para combinar los datos del producto exportados con la plantilla de Excel.

1. Cargue el archivo de Excel con los datos del producto exportados.

   * Vuelva a la página Artículos del catálogo de productos en el [Centro de vendedores Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   * Select [!UICONTROL **Agregar elementos** > **Agregar elementos de forma masiva**].
   * Arrastre la hoja de cálculo completa a la sección Cargar .
   * Select [!UICONTROL **Submit**].
   * Seleccione el [!UICONTROL  **Fuente de actividades**] para ver el progreso.

Para obtener instrucciones completas, consulte [Agregar artículos de forma masiva mediante la especificación de artículos completos](https://sellerhelp.walmart.com/s/guide?article=000007680) en el [!DNL *Ayuda para vendedores de Walmart*].
