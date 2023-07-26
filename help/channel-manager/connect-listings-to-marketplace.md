---
title: Conectar anuncios a Walmart
description: '''Conectar anuncios para [!DNL Commerce] productos a [!DNL Walmart Marketplace]para empezar a vender.'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 0%

---

# Conectar anuncios a Walmart

Al igual que otros mercados, [!DNL Walmart] permite a los vendedores externos poner en venta artículos vendidos por otros.

- [!DNL Walmart Marketplace] utiliza identificadores de producto como UPC y GTIN para hacer coincidir productos con productos existentes [!DNL Walmart Marketplace] anuncios.

- Para los productos que coinciden, la lista de Walmart Marketplace se actualiza para incluir la [!DNL Commerce] oferta de productos al conectar un producto desde [!DNL Channel Manager].

- Normalmente, las ofertas de productos con los precios más bajos aparecen primero en la [!DNL Walmart Marketplace] anuncio, pero otros factores como las críticas también afectan a la ubicación.

## Hacer coincidir productos

Cuando coinciden los productos, Channel Manager envía los datos del producto a [!DNL Walmart Marketplace] para buscar listados existentes con valores de atributo que coincidan con el asignado [!DNL Commerce] atributo de producto. Los criterios de coincidencia los determina la variable [configuración de asignación de atributos](map-catalog-attributes.md) para el canal de la tienda.

Si se encuentra una coincidencia, la lista de productos existente se actualiza para agregar la oferta.

### Requisitos previos

Antes de hacer coincidir productos, verifique que los valores de atributos del catálogo de productos cumplan los requisitos de Walmart y configure las opciones de atributos de productos. Consulte [Asignar atributos de catálogo](map-catalog-attributes.md).

#### Seleccionar y hacer coincidir productos

1. Abra un canal de ventas conectado.

1. Desde **[!UICONTROL Listings]**, seleccione los productos para la coincidencia que se encuentran en *[!UICONTROL Draft]* estado.

   ![Seleccionar productos de los anuncios y enviar para que coincidan](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. Seleccionar **[!UICONTROL Match Products]**.

   Un mensaje indica el número de productos enviados para su coincidencia.

   El estado de los productos seleccionados cambia a [!UICONTROL *Procesando*] hasta que finalice la operación de coincidencia. Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

### Comprobar estado de coincidencia

Una vez finalizada la coincidencia, seleccione **[!UICONTROL Refresh products]** para ver el estado actual del producto. *Coincidencia* o *Error*.

- **[!UICONTROL Match]** indica que el producto coincide correctamente. Su oferta de productos estaba conectada a un anuncio existente de Walmart Marketplace. Si la variable [El almacén de Marketplace no está activo](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* se muestra en la *[!UICONTROL Status detail]* columna. Los productos clasificados se conectan automáticamente cuando la variable [!DNL Walmart Marketplace] La tienda está activada.

- **[!UICONTROL Error]** indica que la operación de coincidencia falló debido a uno de los siguientes problemas:

   - [!DNL Channel Manager] no se pudo enviar para la coincidencia debido a un problema de conexión.

   - No se ha encontrado ninguna coincidencia.

   - Se ha encontrado una coincidencia, pero el listado no se puede conectar porque [!DNL Walmart Marketplace] ha devuelto un código de error. Consulte la **[!UICONTROL Error Description]** para obtener información sobre el problema.

### Ver listado en Walmart

Después de hacer coincidir productos, revise la lista de productos actualizada y verifique los detalles del producto, el precio y la cantidad de inventario en [[!UICONTROL Walmart Marketplace Seller Account Items] tablero](https://seller.walmart.com/items-and-inventory/manage-items) para revisar el producto actualizado.

### Solucionar errores de coincidencia de productos

Si la operación de coincidencia de productos falla con un error, el mensaje de error se muestra en la variable *[!UICONTROL Status detail]* en la columna [!UICONTROL Channel Manager] lista de productos.

Los errores comunes devueltos son valores de ID de producto con formato incorrecto o faltan atributos necesarios.

#### Corregir valores de ID de producto

| Tipo | Descripción | Ejemplo |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, el número de 12 dígitos, incluido el dígito de control. </br></br>Si su UPC tiene menos de 12 dígitos, como UPC-E que es de 8 dígitos, agregue ceros finales para cumplir con el requisito. | Cambiar de `45678912345` hasta `045678912345` |
| GTIN | GTIN-14, el número de 14 dígitos, incluido el dígito de control. </br></br>Si el GTIN tiene menos de 14 dígitos, añada ceros a la izquierda </br>para cumplir los requisitos. | Cambiar `456789123456` hasta `0045678912345` |
| EAN | GTIN-13, el número de 13 dígitos, incluido el dígito de control. </br></br>Si su EAN tiene menos de 13 dígitos, agregue el inicial </br>ceros para cumplir el requisito. | Cambiar de `4567891234` hasta `0004567891234` |

Para obtener más información sobre los códigos de error de Walmart Marketplace, consulte la [Ayuda para vendedores de Walmart](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Cargar nuevos listados de productos

Para los productos que no coinciden con Walmart Marketplace, utilice una plantilla de Excel de categoría de producto de Walmart para cargar listados de productos en lotes. La plantilla de Walmart se rellena con datos del catálogo de productos exportados desde su [!DNL Commerce] ejemplo.

Para nuevas listas de productos, revisa tu catálogo de productos para asegurarte de que los productos que planeas vender en Walmart Marketplace tengan los atributos requeridos para las listas de productos de Walmart Marketplace.

**Listas de Walmart Marketplace: requisitos de atributos**

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

- Compruebe que cumple los [Requisitos de Walmart](walmart-requirements.md).

- En su [!DNL Commerce] catálogo de productos, compruebe que la configuración del catálogo para los productos que se van a enumerar en Walmart Marketplace tiene todos los atributos necesarios y cumple las Directrices de contenido de Walmart Marketplace.

- Compruebe que el trabajo cron se está ejecutando para completar la operación de exportación.

   - Para instancias locales, consulte [Configurar y ejecutar cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html).

   - Para infraestructura de nube de Adobe, consulte [Configuración de trabajos cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html).

### Cree el archivo de datos del producto que desea cargar

1. De su [Cuenta de vendedor de Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller), descargue una plantilla de lista de productos del Centro de vendedores de Walmart.

   - En la página Artículos del catálogo de productos, seleccione **[!UICONTROL Add Items]**. A continuación, seleccione **[!UICONTROL Add items in bulk]**.

     ![Agregar elementos en opción masiva en la configuración de elementos de Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - En la página de descarga, seleccione **[!UICONTROL Full Setup]**. A continuación, seleccione una categoría de artículo y descargue la plantilla de categoría.

     ![Descargar opción de plantilla de categoría en la configuración de elementos de Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - Compruebe que la plantilla incluye los atributos requeridos y recomendados para la lista de productos.

1. Desde el [!DNL Commerce] El administrador debe seleccionar los datos de producto que se exportarán desde el Adobe [!DNL Commerce] sitio.

   - En Admin, seleccione [!UICONTROL **Sistema** > Transferencia de datos > **Exportar**].

   - En el [!UICONTROL Export] página en la [!UICONTROL Entity Type] , seleccione [!UICONTROL **Productos**].

   - En el [!UICONTROL Entity Attributes] , configure los criterios de selección para la exportación de datos del producto.

     Utilice los filtros para seleccionar y configurar los valores de atributo que se aplican a las categorías de producto que vende en. Asegúrese de incluir los atributos requeridos y recomendados de Walmart. (Consulte [Exportar datos](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) en el Adobe [!DNL Commerce] Guía del usuario para obtener instrucciones detalladas).

     Para omitir un atributo de la exportación, seleccione la opción [!UICONTROL **Excluir**] al principio de la fila.

1. Desplácese hasta el final de la tabla de atributos y seleccione [!UICONTROL **Continuar**] para iniciar la exportación de datos.

   El archivo de exportación CSV se procesa a través de una cola de mensajes mediante trabajos cron y se guarda en `var/export/folder`. (Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en el *Guía de configuración*.)

1. Abra la plantilla de Excel para la categoría de productos Tienda de Walmart y utilice las funciones de macro de Excel para combinar los datos de productos exportados en la plantilla de Excel.

1. Cargue el archivo de Excel con los datos del producto exportados.

   - Vuelva a la página Elementos del catálogo de productos en la [Centro de vendedores de Walmart](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Seleccionar [!UICONTROL **Agregar elementos** > **Agregar elementos de forma masiva**].
   - Arrastre la hoja de cálculo completada a la sección Cargar.
   - Seleccionar [!UICONTROL **Enviar**].
   - Seleccione el [!UICONTROL  **Fuente de actividades**] para ver el progreso.

Para obtener instrucciones completas, consulte [Adición de elementos por lotes utilizando todas las especificaciones de elementos](https://sellerhelp.walmart.com/s/guide?article=000007680) en el [!DNL *Ayuda para vendedores de Walmart*].
