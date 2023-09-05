---
title: '[!DNL Amazon Sales Channel] notas de la versión'
description: Revise las notas de la versión para obtener información acerca de todos los [!DNL Amazon Sales Channel] versiones.
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: fd9423ba7030ce15f47fdead6854487bc0c29f11
workflow-type: tm+mt
source-wordcount: '2006'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] notas de la versión

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x y 2.4.x de la infraestructura en la nube. La extensión ya no es compatible con Adobe Commerce 2.1, Magento Open Source 2.2 ni Magento 1.
> <br>Compatibilidad disponible para [!DNL Amazon sales channel]  solo en las versiones 4.0.0 y 4.1.0 en las versiones 2.3.x de Adobe Commerce.
> <br>[!DNL Amazon sales channel] la versión 4.2.0 o posterior es compatible con las versiones de Adobe Commerce 2.3.x, pero la compatibilidad solo está disponible para las versiones de Adobe Commerce 2.4.x.
>

Estas notas de la versión describen la versión inicial de [!DNL Amazon sales channel] e incluir:

![Nuevo](../assets/new.svg) Nuevas funciones
![Problema corregido](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para versiones, compatibilidad y compatibilidad.

## v4.5.0

*30 de agosto de 2023*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) Se ha agregado la puerta de enlace de la API Adobe.IO, cambiando de MAGI, para mejorar la seguridad de la autenticación. `ServicesId` proporciona una nueva interfaz de usuario para administrar las credenciales de Adobe.IO, similar a otras [Servicios de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Los comerciantes deben asegurarse de que [claves API privadas y públicas](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) se actualizan para la producción.


![Problema corregido](../assets/fix.svg) Se ha identificado un problema con la configuración y se ha corregido el flujo de creación de pedidos.

## v4.4.4

*7 de marzo de 2023*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Problema corregido](../assets/fix.svg) Se ha agregado compatibilidad con Adobe Commerce 2.4.6 y PHP 8.2.

![Problema corregido](../assets/fix.svg) Reducción del ruido en los registros.

![Problema corregido](../assets/fix.svg) Se ha mejorado la estabilidad al extraer actualizaciones.

![Problema corregido](../assets/fix.svg) Se ha simplificado el proceso para ejecutar una sola extracción similar a una acción o para aplicar desde CLI.

![Problema corregido](../assets/fix.svg) Se ha actualizado la dependencia para `magento/services-connector`.

![Problema corregido](../assets/fix.svg) Se han corregido problemas de sincronización en cuentas de Reino Unido con un código de país no válido.

![Problema corregido](../assets/fix.svg) El valor entity_type_id codificado para la entidad de producto del catálogo causa problemas con el origen de precios de Magento.

![Problema corregido](../assets/fix.svg) Se ha corregido un problema que impedía que las cuentas que se eliminaban en un servidor de otra instancia también se eliminaran de la interfaz de usuario.

![Problema corregido](../assets/fix.svg) Se ha corregido un problema con algunas reglas del carro de compras que infringían la importación de orden.

## v4.4.3

*7 de marzo de 2023*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) Se ha añadido compatibilidad con Adobe Commerce 2.4.4.

## v4.4.2

*11 de noviembre de 2021*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) Dependencias actualizadas para admitir otras extensiones actualizadas.
![Fix](../assets/fix.svg) Se ha agregado compatibilidad con PHP 8.1.

## v4.4.1

*11 de noviembre de 2021*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) Se ha cambiado la forma en que Adobe Commerce recibe el _Nombre de usuario_ de Amazon. Anteriormente, se producía un error durante la creación del pedido cuando la variable _Nombre de usuario_ el campo contenía caracteres especiales. Adobe Commerce ahora recibe la _Nombre de usuario_ y filtra los caracteres especiales para que el pedido se pueda crear correctamente.

## v4.4.0

*9 de abril de 2021*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con el modo de solo lectura a la configuración. Consulte [configuración de canal de ventas](sales-channel-settings.md).

![Fix](../assets/fix.svg) Se ha cambiado el flujo de datos para que varias copias de la misma instancia puedan recuperar actualizaciones simultáneamente.

![Fix](../assets/fix.svg) Se ha cambiado el proceso de sincronización para sincronizar la información de la cuenta. Se ha agregado un trabajo cron para sincronizar con una cuenta remota y se ha agregado la misma funcionalidad a los comandos CLI.

![Fix](../assets/fix.svg) Se agregaron argumentos y indicadores de comandos CLI para un control más preciso.

![Fix](../assets/fix.svg) Se ha corregido la fuente de tareas en segundo plano (cron) en la configuración del sistema.

![Fix](../assets/fix.svg) Se ha corregido el problema que impedía la creación de pedidos cuando el código de país se establecía en Puerto Rico (PR).

## v4.3.0

*3 de marzo de 2021*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) <!--CHAN-xxxx-->El _Detalles del pedido_ se ha rediseñado y ya no depende de la _Importar pedidos_ configuración. Los detalles del pedido ahora aparecen en la interfaz de Sales Channel de Amazon para todos los pedidos.

![Fix](../assets/fix.svg) En el _[!UICONTROL Marketing]_menú en Admin, el nombre se ha cambiado de_[!UICONTROL Amazon]_ hasta _[!UICONTROL Amazon Sales Channel]_.

![Problema conocido](../assets/bug.svg) **Importante**: los problemas conocidos con la compatibilidad con Adobe Commerce 2.4.0 se resuelven en la versión Adobe Commerce 2.4.1.

- Procesos cron de Amazon en `error` state
- La instalación con Commerce 2.4.0 falla al crear tiendas en la base de datos
- La creación del producto falla cuando se instala MSI

## v4.2.0

*3 de marzo de 2021*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

Si tiene un [!DNL Amazon sales channel] versión instalada e intente actualizar el Adobe Commerce a la versión 2.4.0, se le pedirá que actualice la extensión antes de poder completar la actualización de Adobe Commerce.

![Problema conocido](../assets/bug.svg) Cuándo [!DNL Amazon sales channel] 4.2.0 está integrado con la versión 2.4.0 y [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) está habilitado, hay un problema conocido que impide la adición de productos en el catálogo de Commerce. Este problema se solucionará en una versión futura de Commerce.

![Nuevo](../assets/new.svg) [!DNL Amazon sales channel] se ha mejorado para aceptar datos de direcciones basados en texto y hacerlos coincidir con formatos de direcciones estandarizados, incluidos ciudad, estado y código postal. Esta actualización permite que los datos de pedidos y envíos se sincronicen (sincronicen) con Amazon sin errores de dirección.<br/>Por ejemplo, un comprador introduce la ciudad, el estado y el código postal como `Escondido, californiA 92025-1501`. Amazon Sales Channel importa y hace coincidir los datos con el formato estándar como `Escondido, CA 92025`y luego lo vuelve a sincronizar con Amazon en este formato estandarizado.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con PHP 7.4.

![Nuevo](../assets/new.svg) <!--CHAN-4334-->Se ha agregado compatibilidad con Adobe Commerce 2.4.x. Las versiones anteriores pueden ser compatibles con Commerce 2.4.x, pero no son compatibles. Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para la compatibilidad de versiones. La Sales Channel de Amazon debe actualizarse a 4.2.0 antes de poder completar la actualización de Adobe Commerce 2.4.0.

![Fix](../assets/fix.svg) <!--CHAN-4431-->Se ha corregido un problema que provocaba un error _Acceso denegado_ error para clientes del Reino Unido.

![Fix](../assets/fix.svg) <!--CHAN-4394-->Se ha corregido un problema que impedía que el estado de envío de Amazon se sincronizara con el pedido de comercio correspondiente, lo que &quot;bloqueaba&quot; el estado de envío del pedido como `Pending` en Commerce y `Unshipped` en Amazon. Con la nueva función de dirección estandarizada, se han resuelto estos errores de estado de envío.

![Fix](../assets/fix.svg) <!--ticket#-->Se ha actualizado la sincronización de pedidos (sincronización) para que ignore las importaciones de pedidos fallidas, lo que reduce varios intentos de sincronización y permite que se procesen las importaciones posteriores, con solicitudes de sincronización de pedidos enviadas cada cinco minutos. Los errores de sincronización se siguen registrando en el registro de errores, pero se marcan como &quot;procesados&quot; para permitir funciones de registro adicionales. Además, [!DNL Amazon sales channel] ahora elimina automáticamente los datos sobrantes recopilados para los pedidos que no se crean en Commerce.

![Fix](../assets/fix.svg) Se ha actualizado el registro de errores para recopilar más información sobre errores de excepción y actualización de extensión no detectados.

![Fix](../assets/fix.svg) <!--ticket#-->Se ha corregido un problema que provocaba la sincronización inicial del _precio más bajo_ Faltan los datos debido a un error _precio_ valor.

![Fix](../assets/fix.svg) <!--CHAN-4410-->Se han corregido problemas que provocaban errores de filtrado en _Pedidos de Amazon_ ver cuándo se deja en blanco el campo de intervalo de fechas.

![Fix](../assets/fix.svg) <!--CHAN-4439-->Se ha corregido un problema que provocaba errores de sincronización de satisfacción y existencias relacionados con la cantidad. La extensión ahora redondea los valores de cantidad introducidos como decimales antes de sincronizarlos con Amazon.<br/> Por ejemplo, cuando un comerciante introduce manualmente una cantidad de `2.5`, la extensión redondea el valor a `2` y, a continuación, sincroniza la cantidad actualizada con Amazon.

## v4.1.0

*7 de mayo de 2020*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) <!--4247, 4230-->Se ha cambiado el proceso de importación de pedidos para que se ajuste a los requisitos de pedidos de Commerce. Estos cambios corrigen problemas que impiden que Commerce cree el pedido correspondiente para un pedido importado. Consulte [Administrar pedidos](managing-orders.md) para obtener información sobre bloqueadores de pedidos y soluciones.

![Nuevo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Se ha actualizado el _Pedidos recientes_ del tablero de la tienda y se ha añadido una nueva sección _Todos los pedidos_ vista que muestra todos sus pedidos de Amazon, incluidas las opciones de filtro y la paginación para ver más pedidos. Consulte [Tablero de Amazon Store](amazon-store-dashboard.md) y [Ver pedidos de Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) Se ha añadido la _[!UICONTROL Order Notes]_de la columna rediseñada_[!UICONTROL Amazon Orders]_ tabla en ambos _[!UICONTROL Recent Orders]_y_[!UICONTROL All Orders]_ vistas. _[!UICONTROL Order Notes]_informe al comerciante de que hay un problema con la importación del pedido. Consulte [Ver pedidos de Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) <!--CHAN-4013-->Se han actualizado los parámetros de condición del producto para alinearlos con [Amazon renovado](https://sell.amazon.com/programs/renewed) programa. Consulte [Productos renovados](renewed-products.md).

![Nuevo](../assets/new.svg) <!--CHAN-3680-->Actualizado [Detalles de pedidos de Amazon](amazon-order-details.md) para incluir &quot;datos genéricos&quot; para pedidos que cumple Amazon. Consulte [Cumplido por](fulfilled-by.md).

![Fix](../assets/fix.svg) <!--CHAN-4069-->Se ha corregido un problema que provocaba la distorsión de los iconos de la tarjeta de la tienda.

![Fix](../assets/fix.svg) <!--CHAN-4165-->Se ha corregido un error que impedía que _Iniciar sesión_ que aparezca después de que se agote el tiempo de espera de la sesión.

![Fix](../assets/fix.svg) <!--CHAN-4211-->Se ha corregido un problema que impedía que el importe de impuestos del pedido de Amazon se importara en el nuevo pedido de Commerce.

![Fix](../assets/fix.svg) <!--CHAN-4234-->Se ha corregido un problema que provocaba que los totales de ingresos mostrados en el panel de la tienda incluyeran pedidos en `Canceled` o `Error` estado.

![Fix](../assets/fix.svg) <!--CHAN-4326-->Se ha corregido un problema que provocaba errores de importación de pedidos asociados a extensiones de terceros que utilizan _Magento Shipping_ métodos para crear pedidos.

![Fix](../assets/fix.svg) <!--CHAN-4357-->Se ha corregido un problema que provocaba errores al ejecutar la sincronización cron. Se ha agregado un bloqueo al comando CLI que impide que dos trabajos cron se sincronicen al mismo tiempo.

![Fix](../assets/fix.svg) Se ha actualizado la política de seguridad de contenido para la compatibilidad con Commerce versión 2.3.5.

## v4.0.0

*25 de marzo de 2020*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

>[!IMPORTANT]
>
>La Sales Channel de Amazon 4.0.0 no es compatible con Adobe Commerce 2.3.5. Para obtener compatibilidad con Adobe Commerce 2.3.5, actualice a la Sales Channel de Amazon 4.1.0.

![Nuevo](../assets/new.svg) Se ha introducido un nuevo [Sales Channel de Amazon](amazon-sales-channel-home.md) página de inicio con &quot;vista de tarjeta&quot; mejorada para la información de la tienda.

![Nuevo](../assets/new.svg) Se ha introducido un nuevo [tablero de tienda](amazon-store-dashboard.md) con información de listado, pedidos recientes y configuración de tienda.

![Nuevo](../assets/new.svg) Presentamos una versión más simple y optimizada [proceso de incorporación](amazon-onboarding-home.md) y [configuración de tienda predeterminada](default-store-settings.md) para que tus tiendas se integren más rápido.

![Problema conocido](../assets/bug.svg) <!--CHAN-4102--> Cuándo [creación de atributos](managing-attributes.md) para importar imágenes de listados y **Vistas de tienda** se establece en `All Store Views (Global)`, existe un problema conocido que impide que las imágenes se importen a todas las vistas de la tienda. Si cambia la configuración de **Almacenar vistas (para importar valores en)** a un almacén específico, las imágenes se importan para ese almacén.

## v3.0.1

*11 de noviembre de 2019*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) **Configuración de campo numérico**: <!--CHAN-3779-->Los campos que requieren un valor numérico se han actualizado para aceptar solo caracteres numéricos. Ejemplo: Configuración de Reglas de Asignación de Precios > Campo Importe de Ajuste

![Fix](../assets/fix.svg) **Vínculos de guía del usuario**: <!--CHAN-3778-->Incorrecto _Guía del usuario_ Se han corregido los vínculos.

![Fix](../assets/fix.svg) **Duplicar anuncios de Amazon**: <!--CHAN-3593-->Se ha corregido un problema notificado anteriormente que causaba anuncios duplicados de Amazon. Antes de esta versión, la extensión añadía el código de país de la región de Amazon a los valores SKU al importar anuncios. El listado coincidía con el elemento de catálogo, pero la extensión creaba un nuevo listado duplicado con el SKU adjunto. Con esta versión, la extensión no modifica el SKU de los anuncios importados y no se realizan cambios en los anuncios existentes. Puede usar el complemento [!UICONTROL End Listing(s)] en la opción de Amazon para eliminar los anuncios duplicados.

## v3.0.0

*7 de octubre de 2019*

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) **Amazon UK Marketplace ya disponible**: los usuarios pueden elegir el mercado del Reino Unido al crear e integrar una tienda de Commerce. Esta actualización para el Reino Unido incluye compatibilidad adicional con:

- [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Código de impuesto del producto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} información.

![Nuevo](../assets/new.svg) **Registro mejorado**: <!--CHAN-3642, 3672-->Se ha implementado el **Habilitar registro de depuración** para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas. Consulte la [Configuración de Sales Channel](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) en la Referencia de configuración.

![Fix](../assets/fix.svg) **Catálogo de productos**: <!--CHAN-3687-->Se ha corregido un problema que impedía que las imágenes importadas con un listado de Amazon se aplicaran al producto del catálogo de Commerce correspondiente.

![Fix](../assets/fix.svg) **Creación de pedidos**: <!--CHAN-3708-->Se ha corregido un problema que impedía que Commerce creara pedidos para un pedido de Amazon que no coincidiera con un producto del catálogo de Commerce.

![Problema conocido](../assets/bug.svg) **Duplicar anuncios de Amazon**: <!--CHAN-3593-->Este problema hace que el catálogo cree un artículo para un anuncio importado, usando el mismo SKU pero con un código de región añadido al final. A continuación, Amazon procesa el SKU modificado como un artículo nuevo y crea un anuncio. Este problema se solucionará en una versión futura.

## v2.0.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

>[!NOTE]
>
>La versión 1.0.0 solo estaba disponible en versiones limitadas.

![Nuevo](../assets/new.svg)  **Incorporación y mantenimiento simplificados**: Añada e integre con su cuenta de vendedor de Amazon mediante un proceso paso a paso con instrucciones detalladas disponibles a través del administrador. Mantenga sus tiendas, cuentas y productos enumerados a través de un tablero.

![Nuevo](../assets/new.svg)  **Compatibilidad con varias cuentas**: administre y supervise varias marcas de Amazon y regiones de mercado a través del administrador.

![Nuevo](../assets/new.svg)  **Precios inteligentes**: establezca reglas de reasignación de precios automatizadas para aumentar las posibilidades del codiciado Buy Box. Configure los precios para que se ajusten dinámicamente al precio de Buy Box actual o al precio de competidor más bajo. Establece límites a la reasignación de precios para proteger tu margen.

![Nuevo](../assets/new.svg)  **Administración de listados**: automatice las listas de productos y sincronice el catálogo de Commerce con Amazon Marketplace mediante reglas de lista. Añada invalidaciones específicas para controlar con precisión las ofertas. Controla y administra todos tus anuncios directamente desde el administrador.

![Nuevo](../assets/new.svg)  **Inventory management coherente**: Mantenga las cantidades de inventario de Commerce y Amazon en sincronización constante.

![Nuevo](../assets/new.svg)  **Gestión de Pedidos y Satisfacción**: haga un seguimiento de los pedidos de Amazon a través del panel, con una comunicación fluida y actualizaciones de inventario. Complete y rastree los envíos de pedidos según Amazon, los satisfechos por el comerciante o una combinación de métodos.

![Problema conocido](../assets/bug.svg)  Es posible que se produzcan tiempos de espera más largos para actualizar las cantidades de productos. Las actualizaciones de la cantidad de productos pueden tardar aproximadamente dos horas en sincronizarse.

![Problema conocido](../assets/bug.svg)  Los pedidos importados pueden tener un tipo de _Prime_ o _Premium_ pedidos. Debes verificar estos pedidos en tu cuenta de vendedor de Amazon.

![Problema conocido](../assets/bug.svg)  Los productos agrupados no aptos pueden mostrarse como aptos para la venta en Amazon. Es posible que uno de los productos incluidos en el paquete no sea apto. Si tiene problemas, compruebe el estado de idoneidad para los artículos de productos agrupados.

![Problema conocido](../assets/bug.svg)  Al utilizar Inventory management for Commerce 2.3.x, es posible que un reíndice de existencias parcial no genere déclencheur cuando se crea un pedido. La cantidad vendible se vuelve a calcular cada hora, lo que puede causar un exceso de ventas durante este intervalo de actualización.
