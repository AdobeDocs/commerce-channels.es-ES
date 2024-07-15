---
title: Conectar anuncios a Walmart
description: 'Conecta anuncios de [!DNL Commerce] productos a [!DNL Walmart Marketplace]para empezar a vender.'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Conectar anuncios a Walmart

Al igual que otros mercados, [!DNL Walmart] permite a los vendedores externos poner en venta artículos vendidos por otros.

- [!DNL Walmart Marketplace] usa identificadores de producto como UPC y GTIN para hacer coincidir productos con listados de [!DNL Walmart Marketplace] existentes.

- Para los productos que coinciden, la lista de Walmart Marketplace se actualiza para incluir la oferta de producto [!DNL Commerce] al conectar un producto de [!DNL Channel Manager].

- Por lo general, las ofertas de productos con los precios más bajos aparecen primero en el listado de [!DNL Walmart Marketplace], pero otros factores como las revisiones también afectan la ubicación.

## Hacer coincidir productos

Cuando se comparan productos, Channel Manager enviará los datos del producto a [!DNL Walmart Marketplace] para buscar anuncios existentes con valores de atributo que coincidan con el atributo de producto [!DNL Commerce] asignado. Los criterios de coincidencia los determina la [configuración de asignación de atributos](map-catalog-attributes.md) para el canal de tienda.

Si se encuentra una coincidencia, la lista de productos existente se actualiza para agregar la oferta.

### Requisitos previos

Antes de hacer coincidir productos, verifique que los valores de atributos del catálogo de productos cumplan los requisitos de Walmart y configure las opciones de atributos de productos. Consulte [Asignar atributos de catálogo](map-catalog-attributes.md).

#### Seleccionar y hacer coincidir productos

1. Abra un canal de ventas conectado.

1. En **[!UICONTROL Listings]**, seleccione productos para buscar coincidencias que se encuentren en el estado *[!UICONTROL Draft]*.

   ![Seleccionar productos de los anuncios y enviarlos para que coincidan](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. Seleccione **[!UICONTROL Match Products]**.

   Un mensaje indica el número de productos enviados para su coincidencia.

   El estado de los productos seleccionados cambia a [!UICONTROL *Procesando*] hasta que finalice la operación de coincidencia. Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

### Comprobar estado de coincidencia

Una vez finalizada la coincidencia, seleccione **[!UICONTROL Refresh products]** para ver el estado actual del producto. *Coincidencia* o *Error*.

- **[!UICONTROL Match]** indica que el producto se encontró correctamente coincidente. Su oferta de productos estaba conectada a un anuncio existente de Walmart Marketplace. Si el almacén de [Marketplace no está activo](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* se muestra en la columna *[!UICONTROL Status detail]*. Los productos clasificados se conectan automáticamente cuando se activa el almacén [!DNL Walmart Marketplace].

- **[!UICONTROL Error]** indica que la operación de coincidencia falló debido a uno de los siguientes problemas:

   - [!DNL Channel Manager] no pudo enviar para buscar coincidencias debido a un problema de conexión.

   - No se ha encontrado ninguna coincidencia.

   - Se encontró una coincidencia, pero el listado no se puede conectar porque [!DNL Walmart Marketplace] devolvió un código de error. Consulte **[!UICONTROL Error Description]** para obtener información sobre el problema.

### Ver listado en Walmart

Después de hacer coincidir los productos, revise la lista de productos actualizada y verifique los detalles del producto, el precio y la cantidad de inventario en el [[!UICONTROL Walmart Marketplace Seller Account Items] panel](https://seller.walmart.com/items-and-inventory/manage-items) para revisar el producto actualizado.

### Solucionar errores de coincidencia de productos

Si la operación de coincidencia de productos falla con un error, el mensaje de error se muestra en la columna *[!UICONTROL Status detail]* de la lista de productos [!UICONTROL Channel Manager].

Los errores comunes devueltos son valores de ID de producto con formato incorrecto o faltan atributos necesarios.

#### Corregir valores de ID de producto

| Tipo | Descripción | Ejemplo |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, el número de 12 dígitos, incluido el dígito de control. </br></br>Si su UPC tiene menos de 12 dígitos, como UPC-E, que tiene 8 dígitos, agregue ceros finales para cumplir con el requisito. | Cambiar de `45678912345` a `045678912345` |
| GTIN | GTIN-14, el número de 14 dígitos, incluido el dígito de control. </br></br>Si el GTIN tiene menos de 14 dígitos, agregue ceros </br> a la izquierda para cumplir con los requisitos. | Cambiar `456789123456` a `0045678912345` |
| EAN | GTIN-13, el número de 13 dígitos, incluido el dígito de control. </br></br>Si su EAN tiene menos de 13 dígitos, agregue </br>ceros a la izquierda para cumplir con el requisito. | Cambiar de `4567891234` a `0004567891234` |

Para obtener más información sobre los códigos de error de Walmart Marketplace, consulte la [Ayuda para vendedores de Walmart](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Cargar nuevos listados de productos

Para los productos que no coinciden con Walmart Marketplace, utilice una plantilla de Excel de categoría de producto de Walmart para cargar listados de productos en lotes. La plantilla de Walmart se rellena usando datos del catálogo de productos exportados desde la instancia de [!DNL Commerce].

Para nuevas listas de productos, revisa tu catálogo de productos para asegurarte de que los productos que planeas vender en Walmart Marketplace tengan los atributos requeridos para las listas de productos de Walmart Marketplace.

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
| Peso de envío | Requerido |
| Características principales | Recomendado |
| Número de modelo | Recomendado |
| Nombre del fabricante | Recomendado |
| Número de pieza del fabricante | Recomendado |
| Tamaño | Recomendado |
| Color | Recomendado |
| URL de imagen principal | Opcional |
| URL de imagen adicional | Opcional |
| Fabricante | Opcional |

### Requisitos previos

- Compruebe que cumple con los [requisitos de Walmart](walmart-requirements.md).

- En su catálogo de productos [!DNL Commerce], verifique que la configuración del catálogo para los productos que se van a enumerar en Walmart Marketplace tenga todos los atributos requeridos y cumpla con las Directrices de contenido de Walmart Marketplace.

- Compruebe que el trabajo cron se está ejecutando para completar la operación de exportación.

   - Para instancias locales, consulte [Configurar y ejecutar cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html).

   - Para la infraestructura de nube de Adobe, consulte [Configuración de trabajos cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html).

### Cree el archivo de datos del producto que desea cargar

1. Desde tu [cuenta de vendedor de Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller), descarga una plantilla de lista de productos del Centro de vendedores de Walmart.

   - En la página Elementos del catálogo de productos, seleccione **[!UICONTROL Add Items]**. A continuación, seleccione **[!UICONTROL Add items in bulk]**.

     ![Agregar elementos en opción masiva en la configuración de elementos de Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - En la página de descarga, seleccione **[!UICONTROL Full Setup]**. A continuación, seleccione una categoría de artículo y descargue la plantilla de categoría.

     ![Descargar opción de plantilla de categoría en la configuración de elemento de Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - Compruebe que la plantilla incluye los atributos requeridos y recomendados para la lista de productos.

1. Desde el administrador de [!DNL Commerce], seleccione los datos de producto que desea exportar desde el sitio de Adobe [!DNL Commerce].

   - En el Administrador, seleccione [!UICONTROL **Sistema** > Transferencia de datos > **Exportar**].

   - En la página [!UICONTROL Export] del campo [!UICONTROL Entity Type], seleccione [!UICONTROL **Productos**].

   - En la tabla [!UICONTROL Entity Attributes], configure los criterios de selección para la exportación de datos del producto.

     Utilice los filtros para seleccionar y configurar los valores de atributo que se aplican a las categorías de producto que vende en. Asegúrese de incluir los atributos requeridos y recomendados de Walmart. (Consulte [Exportar datos](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) en la Guía del usuario de Adobe [!DNL Commerce] para obtener instrucciones detalladas).

     Para omitir un atributo de la exportación, seleccione la casilla de verificación [!UICONTROL **Excluir**] al principio de la fila.

1. Desplácese hasta el final de la tabla de atributos y seleccione [!UICONTROL **Continuar**] para iniciar la exportación de datos.

   El archivo de exportación CSV se procesa mediante una cola de mensajes mediante trabajos cron y se guarda en `var/export/folder`. (Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en la *Guía de configuración*).

1. Abra la plantilla de Excel para la categoría de productos Tienda de Walmart y utilice las funciones de macro de Excel para combinar los datos de productos exportados en la plantilla de Excel.

1. Cargue el archivo de Excel con los datos del producto exportados.

   - Vuelva a la página Artículos del catálogo de productos en el [Centro de vendedores de Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Seleccione [!UICONTROL **Agregar elementos** > **Agregar elementos de forma masiva**].
   - Arrastre la hoja de cálculo completada a la sección Cargar.
   - Seleccione [!UICONTROL **Enviar**].
   - Seleccione [!UICONTROL  **Fuente de actividades**] para ver el progreso.

Para obtener instrucciones completas, consulte [Agregar elementos en lote utilizando las especificaciones completas del elemento](https://sellerhelp.walmart.com/s/guide?article=000007680) en la [!DNL *Ayuda para vendedores de Walmart*].
