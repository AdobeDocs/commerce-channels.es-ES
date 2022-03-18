---
title: '''[!DNL Amazon Sales Channel] Notas de la versión'''
description: Revise las notas de la versión para obtener información sobre todas las [!DNL Amazon Sales Channel] versiones.
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: 19424bf0deebf2b5464f973edad48f63d6042463
workflow-type: tm+mt
source-wordcount: '2090'
ht-degree: 0%

---

# Notas de la versión

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x y 2.4.x de la infraestructura de nube. La extensión ya no es compatible con Adobe Commerce 2.1, Magento Open Source 2.2 o Magento 1.
> <br>La compatibilidad con [!DNL Amazon sales channel]  versiones 4.0.0 y 4.1.0 solo en Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] la versión 4.2.0 o posterior es compatible con las versiones de Adobe Commerce 2.3.x, pero solo está disponible para las versiones de Adobe Commerce 2.4.x.

Estas notas de la versión describen la versión inicial de [!DNL Amazon sales channel] e incluyen:

![Nuevo](../assets/new.svg) Nuevas funciones
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

Consulte [Próximas versiones](https://devdocs.magento.com/release/){target=&quot;_blank&quot;} para versiones, compatibilidad y compatibilidad.

## v4.4.2

[!DNL Amazon sales channel]  4.4.2 es compatible con las versiones 2.3.x y 2.4.0 de Adobe Commerce, pero solo es compatible con las versiones 2.4.1 y posteriores de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube

Esta versión de [!DNL Amazon sales channel] incluye la siguiente corrección.

![Corrección](../assets/fix.svg) Se han actualizado las dependencias para admitir otras extensiones actualizadas.
![Corrección](../assets/fix.svg) Se ha agregado compatibilidad con PHP 8.1.

## v4.4.1

[!DNL Amazon sales channel] 4.4.1 es compatible con las versiones 2.3.x y 2.4.0 de Adobe Commerce, pero solo es compatible con las versiones 2.4.1 y posteriores de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

Esta versión de [!DNL Amazon sales channel]  incluye la siguiente corrección.

![Corrección](../assets/fix.svg) Se ha cambiado la forma en que Adobe Commerce recibe la variable _Nombre de usuario_ de Amazon. Anteriormente, se producía un error durante la creación del pedido cuando la variable _Nombre de usuario_ contiene caracteres especiales. Adobe Commerce ahora recibe la variable _Nombre de usuario_ y filtra los caracteres especiales para que el orden se pueda crear correctamente.

## v4.4.0

[!DNL Amazon sales channel] 4.4.0 es compatible con las versiones 2.3.x y 2.4.0 de Adobe Commerce, pero solo es compatible con las versiones 2.4.1 y posteriores de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

Esta versión de [!DNL Amazon sales channel] incluye las siguientes mejoras y correcciones.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con el modo de solo lectura a la configuración. Consulte [configuración del canal de ventas](sales-channel-settings.md).

![Corrección](../assets/fix.svg) Se ha cambiado el flujo de datos para que varias copias de la misma instancia puedan recuperar actualizaciones simultáneamente.

![Corrección](../assets/fix.svg) Se ha cambiado el proceso de sincronización para sincronizar la información de la cuenta. Se ha agregado un trabajo cron para sincronizar con una cuenta remota y se ha agregado la misma funcionalidad a los comandos CLI.

![Corrección](../assets/fix.svg) Se han agregado argumentos y indicadores de comando CLI para un control más preciso.

![Corrección](../assets/fix.svg) Se ha corregido el origen Tareas en segundo plano (cron) en la configuración del sistema.

![Corrección](../assets/fix.svg) Se ha corregido el problema que impedía la creación de pedidos cuando el código de país se establecía en Puerto Rico (PR).

## v4.3.0

[!DNL Amazon sales channel] La versión 4.3.0 es compatible con las versiones 2.3.x y 2.4.0 de Adobe Commerce. La compatibilidad solo está disponible para las versiones 2.4.1 y posteriores de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

Esta versión de [!DNL Amazon sales channel] incluye las siguientes mejoras y correcciones.

![Corrección](../assets/fix.svg) <!--CHAN-xxxx-->La variable _Detalles del pedido_ se ha rediseñado y ya no se basa en la función _Importar pedidos_ configuración. Los detalles del pedido ahora aparecen en la interfaz de Sales Channel de Amazon para todos los pedidos.

![Corrección](../assets/fix.svg) En el _[!UICONTROL Marketing]_en el menú Administrador, el nombre se ha cambiado de_[!UICONTROL Amazon]_ a _[!UICONTROL Amazon Sales Channel]_.

![Problema conocido](../assets/bug.svg) **Importante**: Los problemas conocidos con la compatibilidad con Adobe Commerce 2.4.0 se resuelven en la versión Adobe Commerce 2.4.1.

- Procesos cron de Amazon en `error` state
- La instalación con Commerce 2.4.0 falla al crear almacenes en la base de datos
- La creación del producto falla cuando MSI está instalado

## v4.2.0

[!DNL Amazon sales channel] 4.2.0 es compatible con las versiones 2.3.x de Adobe Commerce, pero solo es compatible con las versiones 2.4.x de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube. Si tiene un [!DNL Amazon sales channel] instalado e intente actualizar el Adobe Commerce a la versión 2.4.0., se le pedirá que actualice la extensión antes de completar la actualización de Adobe Commerce.

Esta versión de [!DNL Amazon sales channel] incluye una nueva función junto con mejoras y correcciones.

![Problema conocido](../assets/bug.svg) When [!DNL Amazon sales channel] 4.2.0 está integrado con la versión 2.4.0 y [Inventory management](https://docs.magento.com/user-guide/catalog/inventory.html) está habilitado, existe un problema conocido que impide la adición de productos en el catálogo de comercio. Este problema se solucionará en una futura versión de Commerce.

![Nuevo](../assets/new.svg) [!DNL Amazon sales channel] se ha mejorado para aceptar datos de direcciones basados en texto y hacerlos coincidir con formatos de direcciones estandarizados, como ciudad, estado y código postal. Esta actualización permite que los datos de pedidos y envíos se sincronicen (sincronicen) con Amazon sin errores de dirección.<br/>Por ejemplo, un comprador introduce la ciudad, el estado y el código postal como `Escondido, californiA 92025-1501`. La Sales Channel de Amazon importa y hace coincidir los datos con el formato estándar de `Escondido, CA 92025`y luego la sincroniza con Amazon en este formato estandarizado.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con PHP 7.4.

![Nuevo](../assets/new.svg) <!--CHAN-4334-->Se ha agregado compatibilidad con Adobe Commerce 2.4.x. Las versiones anteriores pueden ser compatibles con Commerce 2.4.x, pero no con Commerce 2.4.x. Consulte [Próximas versiones](https://devdocs.magento.com/release/){:target=&quot;_blank&quot;} para compatibilidad con versiones. La Sales Channel de Amazon debe actualizarse a la versión 4.2.0 antes de poder completar la actualización a Adobe Commerce 2.4.0.

![Corrección](../assets/fix.svg) <!--CHAN-4431-->Se ha corregido un problema que provocaba una _Acceso denegado_ error para clientes del Reino Unido.

![Corrección](../assets/fix.svg) <!--CHAN-4394-->Se ha corregido un problema que impedía que el estado de envío de Amazon se sincronizara con el pedido comercial correspondiente, por lo que se &quot;bloqueaba&quot; el estado de envío del pedido como `Pending` en Comercio y `Unshipped` en Amazon. Con la nueva función de direcciones estandarizadas, se han resuelto estos errores de estado de envío.

![Corrección](../assets/fix.svg) <!--ticket#-->Se ha actualizado la sincronización de pedidos (sincronización) para ignorar las importaciones de pedidos fallidas, lo que reduce los intentos de sincronización múltiple y permite que las importaciones subsiguientes se procesen con las solicitudes de sincronización de pedidos enviadas cada cinco minutos. Los errores de sincronización se siguen registrando en el registro de errores, pero se marcan como &quot;procesados&quot; para permitir más funciones de registro. Además, [!DNL Amazon sales channel] ahora elimina automáticamente los datos sobrantes recopilados para los pedidos que no se pueden crear en Commerce.

![Corrección](../assets/fix.svg) Se ha actualizado el registro de errores para recopilar más información sobre excepciones no detectadas y errores de actualización de extensiones.

![Corrección](../assets/fix.svg) <!--ticket#-->Se ha corregido un problema que provocaba la sincronización inicial de la variable _precio más bajo_ Fallo en los datos debido a la falta de _precio_ valor.

![Corrección](../assets/fix.svg) <!--CHAN-4410-->Se corrigieron problemas que causaban errores de filtrado en la variable _Pedidos de Amazon_ vista cuando el campo de intervalo de fechas se deja en blanco.

![Corrección](../assets/fix.svg) <!--CHAN-4439-->Se ha corregido un problema que provocaba errores de sincronización de stock y de cumplimiento relacionados con la cantidad. La extensión ahora redondea los valores de cantidad introducidos como decimales antes de sincronizar con Amazon.<br/> Por ejemplo, cuando un comerciante introduce manualmente una cantidad de `2.5`, la extensión redondea el valor a `2` y, a continuación, sincroniza la cantidad actualizada con Amazon.

## v4.1.0

La Sales Channel de Amazon 4.1.0 es compatible con Adobe Commerce 2.3.x de código abierto de comercio, Adobe Commerce y Adobe Commerce en la infraestructura de nube. Esta versión de la Sales Channel de Amazon incluye mejoras en la interfaz de usuario, así como correcciones de errores menores.

![Nuevo](../assets/new.svg) <!--4247, 4230-->Se ha cambiado el proceso de importación de pedidos para que se ajuste a los requisitos de pedidos comerciales. Estos cambios corrigen los problemas que impedían que Commerce creara el orden correspondiente para un pedido importado. Consulte [Administrar pedidos](managing-orders.md) para obtener información sobre los bloqueadores de pedidos y las soluciones.

![Nuevo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Se ha actualizado el _Pedidos recientes_ sección del panel de almacenamiento y se ha añadido una nueva _Todos los pedidos_ vista que muestra todos sus pedidos de Amazon, incluidas las opciones de filtro y paginación para ver más pedidos. Consulte [Tablero de Amazon Store](amazon-store-dashboard.md) y [Ver pedidos de Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) Se ha añadido la variable _[!UICONTROL Order Notes]_de la columna rediseñada_[!UICONTROL Amazon Orders]_ en ambas _[!UICONTROL Recent Orders]_y_[!UICONTROL All Orders]_ vistas. _[!UICONTROL Order Notes]_informe al comerciante de que existe un problema con la importación del pedido. Consulte [Ver pedidos de Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) <!--CHAN-4013-->Se han actualizado los parámetros de condición del producto para que se alineen con la variable [Amazon renovado](https://sell.amazon.com/programs/renewed) programa. Consulte [Productos renovados](renewed-products.md).

![Nuevo](../assets/new.svg) <!--CHAN-3680-->Actualizado [Detalles de pedidos de Amazon](amazon-order-details.md) para incluir &quot;datos genéricos&quot; para los pedidos que Amazon cumple. Consulte [Cumplimentado por](fulfilled-by.md).

![Corrección](../assets/fix.svg) <!--CHAN-4069-->Se ha corregido un problema que provocaba la distorsión de los iconos en la tarjeta de la tienda.

![Corrección](../assets/fix.svg) <!--CHAN-4165-->Se ha corregido un error que impedía que se mostrara la variable _Inicio de sesión_ cuando se agota el tiempo de espera de la sesión.

![Corrección](../assets/fix.svg) <!--CHAN-4211-->Se ha corregido un problema que impedía que el importe del impuesto de pedido de Amazon se importara al nuevo pedido de comercio.

![Corrección](../assets/fix.svg) <!--CHAN-4234-->Se ha corregido un problema que provocaba que los totales de ingresos mostrados en el panel de la tienda incluyeran pedidos en `Canceled` o `Error` estado.

![Corrección](../assets/fix.svg) <!--CHAN-4326-->Se ha corregido un problema que provocaba errores de importación de pedidos asociados con extensiones de terceros que utilizan _Magento Shipping_ métodos para crear pedidos.

![Corrección](../assets/fix.svg) <!--CHAN-4357-->Se ha corregido un problema que provocaba errores al ejecutar la sincronización cron. Se ha agregado un bloqueo en el comando CLI que impide que dos trabajos cron se sincronicen al mismo tiempo.

![Corrección](../assets/fix.svg) Se ha actualizado la directiva de seguridad de contenido para la compatibilidad con Commerce versión 2.3.5.

## v4.0.0

La Sales Channel de Amazon 4.0.0 es compatible con las versiones 2.3.0, 2.3.1, 2.3.2, 2.3.3 y 2.3.4 de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube. Esta versión de la Sales Channel de Amazon incluye muchas actualizaciones de la interfaz de usuario, además de correcciones de errores menores.

>[!IMPORTANT]
>
>La Sales Channel de Amazon 4.0.0 no es compatible con Adobe Commerce 2.3.5. Para obtener compatibilidad con Adobe Commerce 2.3.5, actualice a la Sales Channel de Amazon 4.1.0.

![Nuevo](../assets/new.svg) Se ha introducido un nuevo [Sales Channel de Amazon](amazon-sales-channel-home.md) página de inicio con la &quot;vista de tarjeta&quot; mejorada para la información de su tienda.

![Nuevo](../assets/new.svg) Se ha introducido un nuevo [tablero de almacenamiento](amazon-store-dashboard.md) con la información de listado, pedidos recientes y configuración de la tienda.

![Nuevo](../assets/new.svg) Se ha introducido un [proceso de incorporación](amazon-onboarding-home.md) y [configuración predeterminada de la tienda](default-store-settings.md) para que sus tiendas se integren más rápido.

![Problema conocido](../assets/bug.svg) <!--CHAN-4102--> When [creación de atributos](managing-attributes.md) para importar imágenes de anuncios y **Vistas de tiendas** está configurado como `All Store Views (Global)`, existe un problema conocido que impide que las imágenes se importen a todas las vistas del almacén. Si cambia la configuración de **Almacenar vistas (para importar valores en)** a un almacén específico, las imágenes se importan para ese almacén.

## v3.0.1

La Sales Channel de Amazon 3.0.1 es compatible con las versiones de Adobe Commerce 2.2.4 y 2.3.x de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

![Corrección](../assets/fix.svg) **Configuración de campos numéricos**: <!--CHAN-3779-->Los campos que requieren un valor numérico se han actualizado para que acepten únicamente caracteres numéricos. Ejemplo: Configuración de regla de precios > Campo Importe de ajuste

![Corrección](../assets/fix.svg) **Vínculos de la guía del usuario**: <!--CHAN-3778-->Incorrecto _Guía del usuario_ se han corregido.

![Corrección](../assets/fix.svg) **Duplicar anuncios de Amazon**: <!--CHAN-3593-->Se ha corregido un problema que ya se había notificado y que causaba duplicados en los anuncios de Amazon. Antes de esta versión, la extensión agregaba el código de país de la región de Amazon a los valores SKU al importar anuncios. El listado coincidió con el artículo del catálogo, pero la extensión creó un nuevo listado duplicado con el SKU adjunto. Con esta versión, la extensión no modifica el SKU de los anuncios importados y no se realizan cambios en los anuncios existentes. Puede usar la variable [!UICONTROL End Listing(s)] en la opción Amazon para eliminar anuncios duplicados.

## v3.0.0

La Sales Channel de Amazon 3.0.0 es compatible con las versiones de Adobe Commerce 2.2.4 y 2.3.x de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

![Nuevo](../assets/new.svg) **Amazon UK Marketplace ya está disponible**: Los usuarios pueden elegir el mercado del Reino Unido al crear e integrar una tienda de comercio. Esta actualización a Reino Unido incluye compatibilidad adicional para:

- [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources){target=&quot;_blank&quot;}

- [Código de impuesto del producto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US)Información de {target=&quot;_blank&quot;}.

![Nuevo](../assets/new.svg) **Registro mejorado**: <!--CHAN-3642, 3672-->Se ha implementado el **Habilitar el registro de depuración** para recopilar datos de sincronización adicionales cuando sea necesario solucionar el problema. Consulte la [Configuración de Sales Channel](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html) en la Referencia de configuración.

![Corrección](../assets/fix.svg) **Catálogo de productos**: <!--CHAN-3687-->Se ha corregido un problema que impedía que las imágenes importadas con una lista de Amazon se aplicaran al producto del catálogo de comercio correspondiente.

![Corrección](../assets/fix.svg) **Creación de pedidos**: <!--CHAN-3708-->Se ha corregido un problema que impedía que Comercio creara pedidos para un pedido de Amazon que no coincidiera con un producto de catálogo de comercio.

![Problema conocido](../assets/bug.svg) **Duplicar anuncios de Amazon**: <!--CHAN-3593-->Este problema hace que el catálogo cree un elemento para un anuncio importado, usando el mismo SKU pero con un código de región añadido al final. A continuación, Amazon procesa el SKU modificado como un nuevo elemento y crea un listado. Este problema se solucionará en una versión futura.

## v2.0.0

Amazon Sales Channel 2.0.0 es compatible con las versiones 2.2.4 y 2.3.x de Magento Open Source, Adobe Commerce y Adobe Commerce en la infraestructura de nube.

>[!NOTE]
>
>La versión 1.0.0 solo estaba disponible en versión limitada.

![Nuevo](../assets/new.svg)  **Integración y mantenimiento simplificados**: Añada e integre con su cuenta de Vendedor de Amazon mediante un proceso paso a paso con instrucciones detalladas disponibles a través del Administrador. Mantenga sus tiendas, cuentas y productos enumerados a través de un tablero.

![Nuevo](../assets/new.svg)  **Compatibilidad con varias cuentas**: Administre y supervise varias marcas de Amazon y regiones de mercado a través del administrador.

![Nuevo](../assets/new.svg)  **Precios inteligentes**: Establezca reglas de reasignación de precios automatizadas para aumentar sus posibilidades para el codiciado Buy Box. Establezca los precios para ajustarlos de forma dinámica al precio actual del Buy Box o al precio más bajo del competidor. Establezca límites para volver a fijar los precios para proteger su margen.

![Nuevo](../assets/new.svg)  **Administración de anuncios**: Automatice las listas de productos y sincronice el catálogo de comercio con Amazon Marketplace mediante reglas de listado. Añada anulaciones específicas para controlar las ofertas. Supervise y administre todas sus listas directamente desde el administrador.

![Nuevo](../assets/new.svg)  **Inventory management coherente**: Mantenga las cantidades de inventario de Commerce y Amazon en sincronización constante.

![Nuevo](../assets/new.svg)  **Administración de pedidos y pedidos**: Rastree los pedidos de Amazon a través del panel, con una comunicación fluida y actualizaciones de inventario. Lleve a cabo y realice un seguimiento de los envíos de pedidos que Amazon cumpla, de los que el comerciante haya cumplido o de una combinación de métodos.

![Problema conocido](../assets/bug.svg)  Puede encontrar tiempos de espera más largos para actualizar las cantidades de productos. Las actualizaciones de la cantidad del producto pueden tardar ~2 horas en sincronizarse.

![Problema conocido](../assets/bug.svg)  Los pedidos importados pueden tener un tipo de _Prime_ o _Premium_ pedidos. Debe verificar estos pedidos en su cuenta de vendedor de Amazon.

![Problema conocido](../assets/bug.svg)  Los productos agrupados no aptos pueden aparecer como aptos para entrar en Amazon. Es posible que uno de los productos incluidos en el producto agrupado no sea apto. Si tiene problemas, compruebe el estado de elegibilidad de los artículos de productos agrupados.

![Problema conocido](../assets/bug.svg)  Cuando se utiliza Inventory management para Commerce 2.3.x, es posible que un reíndice de existencias parcial no genere déclencheur al crear un pedido. La cantidad salable vuelve a calcular cada hora, lo que puede provocar una sobreventa durante este intervalo de actualización.
