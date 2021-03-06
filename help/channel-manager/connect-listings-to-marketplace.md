---
title: Conectar anuncios a Walmart
description: '''Conectar listados para [!DNL Commerce] productos a [!DNL Walmart Marketplace]para empezar a vender".'
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: bc2e14714e9b532263c480395da28b31b4c3797c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Conectar anuncios a Walmart

Como otros mercados, [!DNL Walmart] permite a los vendedores de terceros enumerar los artículos que venden otros.

- [!DNL Walmart Marketplace] utiliza identificadores de producto como UPC y GTIN para hacer coincidir productos con productos existentes [!DNL Walmart Marketplace] anuncios.

- Para los productos coincidentes, Walmart Marketplace enumera las actualizaciones para incluir la variable [!DNL Commerce] oferta de producto cuando conecta un producto desde [!DNL Channel Manager].

- Normalmente, las ofertas de productos con los precios más bajos aparecen primero en la [!DNL Walmart Marketplace] , pero otros factores como las revisiones también afectan a la ubicación.

## Hacer coincidir productos

Cuando coincide con productos, el Administrador de canales envía los datos del producto a [!DNL Walmart Marketplace] para buscar anuncios existentes con valores de atributo que coincidan con el [!DNL Commerce] atributo de producto. Los criterios de coincidencia están determinados por la variable [configuración de asignación de atributos](map-catalog-attributes.md) para el canal de la tienda.

Si se encuentra una coincidencia, la lista de productos existente se actualiza para añadir la oferta.

### Requisitos previos

Antes de hacer coincidir productos, compruebe que los valores de atributos del catálogo de productos cumplen los requisitos de Walmart y configure los atributos del producto. Consulte [Asignar atributos de catálogo](map-catalog-attributes.md).

#### Seleccionar y buscar coincidencias en los productos

1. Abra un canal de ventas conectado.

1. De **[!UICONTROL Listings]**, seleccione los productos para las coincidencias que se encuentran en *[!UICONTROL Draft]* estado.

   ![Seleccione productos de los anuncios y envíe para que coincidan](assets/products-in-marketplace-sales-channel.png)

1. Select **[!UICONTROL Match Products]**.

   Un mensaje indica el número de productos enviados para la coincidencia.

   ![Enviar productos al canal de ventas conectado](assets/products-submitted-for-matching.png)

   El estado de los productos seleccionados cambia a [!UICONTROL *Procesamiento*] hasta que se complete la operación de coincidencia. Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

### Comprobar estado de coincidencia

Una vez finalizada la coincidencia, seleccione la opción **[!UICONTROL Refresh products]** para ver el estado actual del producto. *Coincidencia* o *Error*.

- **[!UICONTROL Match]** indica que el producto se encontró correctamente. Su oferta de producto estaba conectada a una lista de Walmart Marketplace existente. Si la variable [El almacén de Marketplace no está activo](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* se muestra en la variable *[!UICONTROL Status detail]* para abrir el Navegador. Los productos por etapas se conectan automáticamente cuando la variable [!DNL Walmart Marketplace] el almacén está activado.

- **[!UICONTROL Error]** indica que la operación de coincidencia falló debido a uno de los siguientes problemas:

   - [!DNL Channel Manager] no se pudo enviar para la coincidencia debido a un problema de conexión.

   - No se encontró ninguna coincidencia.

   - Se ha encontrado una coincidencia, pero la lista no se puede conectar porque [!DNL Walmart Marketplace] devuelve un código de error. Consulte la **[!UICONTROL Error Description]** para obtener información sobre el problema.

### Comprobación de listado en Walmart

Después de hacer coincidir los productos, revise la lista de productos actualizada y verifique los detalles del producto, el precio y la cantidad de inventario de la variable [[!UICONTROL Walmart Marketplace Seller Account Items] tablero](https://seller.walmart.com/items-and-inventory/manage-items) para revisar el producto actualizado.

### Solución de problemas de errores de coincidencia de productos

Si la operación de coincidencia del producto falla con un error, el mensaje de error se muestra en la *[!UICONTROL Status detail]* en la columna [!UICONTROL Channel Manager] lista de productos.

Los errores comunes devueltos tienen un formato incorrecto de los valores de ID de producto o carecen de los atributos necesarios.

#### Corrección de los valores de ID de producto

| Tipo | Descripción | Ejemplo |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, el número de 12 dígitos incluyendo el dígito de comprobación. </br></br>Si su UPC tiene menos de 12 dígitos, como UPC-E, que es de 8 dígitos, agregue ceros finales para satisfacer los requisitos. | Cambiar desde `45678912345` a `045678912345` |
| GTIN | GTIN-14, el número de 14 dígitos incluyendo el dígito de comprobación. </br></br>Si su GTIN tiene menos de 14 dígitos, agregue ceros a la izquierda </br>para satisfacer los requisitos. | Cambiar `456789123456` a `0045678912345` |
| EAN | GTIN-13, el número de 13 dígitos incluyendo el dígito de comprobación. </br></br>Si el EAN tiene menos de 13 dígitos, agregue al principio </br>ceros para satisfacer los requisitos. | Cambiar desde `4567891234` a `0004567891234` |

Para obtener más información sobre los códigos de error de Walmart Marketplace, consulte la [Ayuda para vendedores de Walmart](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Cargar nuevas listas de productos

Para los productos que no coinciden con Walmart Marketplace, utilice una plantilla de Excel de categoría de producto Walmart para cargar listas de productos de forma masiva. La plantilla de Walmart se rellena con datos del catálogo de productos exportados desde su [!DNL Commerce] instancia.

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

- Compruebe que cumple los requisitos de [Requisitos de Walmart](walmart-requirements.md).

- En [!DNL Commerce] catálogo de productos, compruebe que la configuración del catálogo de los productos que se incluyen en Walmart Marketplace tiene todos los atributos necesarios y cumple las directrices de contenido de Walmart Marketplace.

- Compruebe que el trabajo cron se esté ejecutando para completar la operación de exportación.

   - Para las instancias locales, consulte [Configuración y ejecución de cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   - Para obtener información sobre la infraestructura de nube de Adobe, consulte [Configurar trabajos cron](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### Cree el archivo de datos del producto para cargar

1. Desde su [Cuenta de vendedor Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller), descargue una plantilla de listado de productos desde el Centro de vendedores de Walmart.

   - En la página Artículos del catálogo de productos , seleccione **[!UICONTROL Add Items]**. A continuación, seleccione **[!UICONTROL Add items in bulk]**.

      ![Agregar elementos en la opción de forma masiva en la configuración de elementos de Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png)

   - En la página de descarga, seleccione **[!UICONTROL Full Setup]**. A continuación, seleccione una categoría de elemento y descargue la plantilla de categoría.

      ![Opción Descargar plantilla de categoría en la configuración de artículos de Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png)

   - Compruebe que la plantilla incluye los atributos requeridos y recomendados para la lista de productos.

1. En el [!DNL Commerce] Administrador, seleccione los datos del producto para exportar desde el Adobe [!DNL Commerce] sitio.

   - En Administración, seleccione [!UICONTROL **Sistema** > Transferencia de datos > **Exportar**].

   - En el [!UICONTROL Export] en el [!UICONTROL Entity Type] campo, seleccione [!UICONTROL **Productos**].

   - En el [!UICONTROL Entity Attributes] , configure los criterios de selección para la exportación de datos del producto.
   ![Exportar la página de datos del producto en el [!UICONTROL [!DNL Commerce] Admin]](assets/walmart-seller-account-full-setup-download.png)

   Utilice filtros para seleccionar y configurar los valores de atributo que se aplican a las categorías de productos que vende. Asegúrese de incluir los atributos requeridos y recomendados de Walmart (consulte [Exportar datos](https://docs.magento.com/user-guide/system/data-export.html) en el Adobe [!DNL Commerce] Guía del usuario para obtener instrucciones detalladas).

   Para omitir un atributo de la exportación, seleccione la opción [!UICONTROL **Excluir**] al principio de la fila.

1. Desplácese hasta el final de la tabla de atributos y seleccione [!UICONTROL **Continuar**] para iniciar la exportación de datos.

   El archivo de exportación CSV se procesa a través de una cola de mensajes utilizando trabajos cron y se guarda en la `var/export/folder`. (Consulte [Administrar colas de mensajes](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) en el *Guía para desarrolladores de Commerce*.)

1. Abra la plantilla de Excel para la categoría de producto de Walmart Marketplace y utilice las capacidades de macros de Excel para combinar los datos del producto exportados con la plantilla de Excel.

1. Cargue el archivo de Excel con los datos del producto exportados.

   - Vuelva a la página Artículos del catálogo de productos en el [Centro de vendedores Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Select [!UICONTROL **Agregar elementos** > **Agregar elementos de forma masiva**].
   - Arrastre la hoja de cálculo completa a la sección Cargar .
   - Select [!UICONTROL **Submit**].
   - Seleccione el [!UICONTROL  **Fuente de actividades**] para ver el progreso.

Para obtener instrucciones completas, consulte [Agregar artículos de forma masiva mediante la especificación de artículos completos](https://sellerhelp.walmart.com/s/guide?article=000007680) en el [!DNL *Ayuda para vendedores de Walmart*].
