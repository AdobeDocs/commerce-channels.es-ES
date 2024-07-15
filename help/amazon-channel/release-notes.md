---
title: '[!DNL Amazon Sales Channel] notas de la versión'
description: Revise las notas de la versión para obtener información acerca de todas las  [!DNL Amazon Sales Channel] versiones.
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] notas de la versión

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] se puede instalar en instancias con Magento Open Source, Adobe Commerce y Adobe Commerce en las versiones 2.3.x y 2.4.x de la infraestructura en la nube. La extensión ya no es compatible con Adobe Commerce 2.1, Magento Open Source 2.2 ni Magento 1.
> <br>La compatibilidad solo está disponible para [!DNL Amazon sales channel] versiones 4.0.0 y 4.1.0 en versiones de Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] la versión 4.2.0 o posterior es compatible con las versiones de Adobe Commerce 2.3.x, pero la compatibilidad solo está disponible para las versiones de Adobe Commerce 2.4.x.
>

Estas notas de la versión describen la versión inicial de [!DNL Amazon sales channel] e incluyen:

![Nuevas](../assets/new.svg) nuevas características
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para ver las versiones, la compatibilidad y la compatibilidad.

Consulte [Disponibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para saber qué versiones de Adobe Commerce admiten esta extensión.

## Versión 4.5.0

*30 de agosto de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó la puerta de enlace de la API Adobe.IO, cambiando de MAGI, para mejorar la seguridad de la autenticación. `ServicesId` proporciona una nueva interfaz de usuario para administrar las credenciales de Adobe.IO, similar a otros [servicios de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Los comerciantes deben asegurarse de que las [claves API privadas y públicas](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) se actualicen para su producción.


![Se corrigió un problema](../assets/fix.svg) que identificó un problema con la configuración y corrigió el flujo de creación de pedidos.

## Versión 4.4.4

*7 de marzo de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Se ha corregido un problema](../assets/fix.svg) Se ha agregado compatibilidad con Adobe Commerce 2.4.6 y PHP 8.2.

![Se corrigió un problema](../assets/fix.svg) Se redujo el ruido en los registros.

![Se ha corregido un problema](../assets/fix.svg) que mejoraba la estabilidad al extraer actualizaciones.

![Se ha corregido un problema](../assets/fix.svg) que simplificaba el proceso de ejecutar una extracción única similar a una acción o de aplicar desde CLI.

![Se ha corregido un problema](../assets/fix.svg) que actualizaba la dependencia de `magento/services-connector`.

![Se corrigió un problema](../assets/fix.svg) Se corrigieron problemas de sincronización en cuentas del Reino Unido con código de país no válido.

![Problema corregido](../assets/fix.svg) El entity_type_id codificado para la entidad de producto del catálogo causa problemas con Magento Price Source.

![Se ha corregido un problema](../assets/fix.svg) que impedía que las cuentas que se eliminaban en un servidor de otra instancia también se eliminaran de la interfaz de usuario.

![Se ha corregido un problema](../assets/fix.svg) que provocaba que algunas reglas del carro de compras infringieran el orden de importación.

## Versión 4.4.3

*7 de marzo de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Corrección](../assets/fix.svg) agregó compatibilidad con Adobe Commerce 2.4.4.

## Versión 4.4.2

*11 de noviembre de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Corrección](../assets/fix.svg) Dependencias actualizadas para admitir otras extensiones actualizadas.
![Corrección](../assets/fix.svg) agregó compatibilidad con PHP 8.1.

## Versión 4.4.1

*11 de noviembre de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Corrección](../assets/fix.svg): se ha cambiado la forma en que Adobe Commerce recibe el campo _Nombre de usuario_ de Amazon. Anteriormente, se producía un error durante la creación del pedido cuando el campo _Nombre de usuario_ contenía caracteres especiales. Adobe Commerce ahora recibe los datos de _Nombre de usuario_ y filtra los caracteres especiales para que el pedido se pueda crear correctamente.

## Versión 4.4.0

*9 de abril de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con el modo de solo lectura a la configuración. Ver [configuración del canal de ventas](sales-channel-settings.md).

![Corrección](../assets/fix.svg) cambió el flujo de datos para que varias copias de la misma instancia puedan obtener actualizaciones simultáneamente.

![Corrección](../assets/fix.svg) cambió el proceso de sincronización para sincronizar la información de la cuenta. Se ha agregado un trabajo cron para sincronizar con una cuenta remota y se ha agregado la misma funcionalidad a los comandos CLI.

![Corregir](../assets/fix.svg) Se agregaron argumentos y marcas de comando de CLI para un control más preciso.

![Corrección](../assets/fix.svg) corrigió el Source de tareas en segundo plano (cron) en la configuración del sistema.

![Corrección](../assets/fix.svg) corrigió el problema que impedía la creación de pedidos cuando el código de país se establecía en Puerto Rico (PR).

## Versión 4.3.0

*3 de marzo de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Corrección](../assets/fix.svg) <!--CHAN-xxxx-->La característica _Detalles del pedido_ se ha rediseñado y ya no depende de la configuración de _Importar pedidos_. Los detalles del pedido ahora aparecen en la interfaz de Sales Channel de Amazon para todos los pedidos.

![Corrección](../assets/fix.svg) En el menú _[!UICONTROL Marketing]_del Administrador, el nombre se ha cambiado de_[!UICONTROL Amazon]_ a _[!UICONTROL Amazon Sales Channel]_.

![Problema conocido](../assets/bug.svg) **Importante**: Los problemas conocidos con la compatibilidad con Adobe Commerce 2.4.0 se resuelven en la versión Adobe Commerce 2.4.1.

- Procesos cron de Amazon en estado `error`
- La instalación con Commerce 2.4.0 falla al crear almacenes en la base de datos
- La creación del producto falla cuando se instala MSI

## Versión 4.2.0

*3 de marzo de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

Si tiene instalada una versión anterior de [!DNL Amazon sales channel] e intenta actualizar el Adobe Commerce a la versión 2.4.0, se le pedirá que actualice la extensión antes de poder completar la actualización de Adobe Commerce.

![Problema conocido](../assets/bug.svg) Cuando [!DNL Amazon sales channel] 4.2.0 está integrado con la versión 2.4.0 y [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) está habilitado, hay un problema conocido que impide la adición de productos en su catálogo de Commerce. Este problema se solucionará en una versión futura de Commerce.

![Nuevo](../assets/new.svg) [!DNL Amazon sales channel] se ha mejorado para aceptar datos de direcciones basados en texto y hacerlos coincidir con formatos de direcciones estandarizados, incluidos ciudad, estado y código postal. Esta actualización permite que los datos de pedidos y envíos se sincronicen (sincronicen) con Amazon sin errores de dirección.<br/>Por ejemplo, un comprador introduce la ciudad, el estado y el código postal como `Escondido, californiA 92025-1501`. La Sales Channel de Amazon importa y hace coincidir los datos con el formato estándar como `Escondido, CA 92025` y, a continuación, los sincroniza de nuevo con Amazon en este formato estandarizado.

![Nuevo](../assets/new.svg) agregó compatibilidad con PHP 7.4.

![Nuevo](../assets/new.svg) <!--CHAN-4334-->Se agregó compatibilidad con Adobe Commerce 2.4.x. Las versiones anteriores pueden ser compatibles con Commerce 2.4.x, pero no son compatibles. Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para ver la compatibilidad de versiones. La Sales Channel de Amazon debe actualizarse a 4.2.0 antes de poder completar la actualización de Adobe Commerce 2.4.0.

![Corrección](../assets/fix.svg) <!--CHAN-4431-->Se ha corregido un problema que causaba un error de _Acceso denegado_ para los clientes del Reino Unido.

![Corregir](../assets/fix.svg) <!--CHAN-4394-->Se ha corregido un problema que impedía que el estado de envío de Amazon se sincronizara con el pedido de Commerce correspondiente, &quot;bloqueando&quot; así el estado de envío del pedido como `Pending` en Commerce y `Unshipped` en Amazon. Con la nueva función de dirección estandarizada, se han resuelto estos errores de estado de envío.

![Corregir](../assets/fix.svg) <!--ticket#-->Se actualizó la sincronización de pedidos (sincronización) para que se pasen por alto las importaciones de pedidos erróneas, reduciendo así los intentos de sincronización múltiples y permitiendo que se procesen las importaciones subsiguientes, con solicitudes de sincronización de pedidos enviadas cada cinco minutos. Los errores de sincronización se siguen registrando en el registro de errores, pero se marcan como &quot;procesados&quot; para permitir funciones de registro adicionales. Además, [!DNL Amazon sales channel] ahora elimina automáticamente los datos sobrantes recopilados para los pedidos que no se crean en Commerce.

![Corregir](../assets/fix.svg) Se actualizó el registro de errores para recopilar más información de errores de excepción y actualización de extensión no detectados.

![Corrección](../assets/fix.svg) <!--ticket#-->Se ha corregido un problema que hacía que fallara la sincronización inicial de los datos de _precio más bajo_ debido a la falta de un valor de _price_.

![Corregir](../assets/fix.svg) <!--CHAN-4410-->Problemas corregidos que causaban errores de filtrado en la vista _Pedidos Amazon_ cuando el campo de intervalo de fecha se deja en blanco.

![Corrección](../assets/fix.svg) <!--CHAN-4439-->Se ha corregido un problema que causaba errores de sincronización de satisfacción y existencias relacionados con la cantidad. La extensión ahora redondea los valores de cantidad introducidos como decimales antes de sincronizarlos con Amazon.<br/> Por ejemplo, cuando un comerciante introduce manualmente una cantidad de `2.5`, la extensión redondea el valor a `2` y, a continuación, sincroniza la cantidad actualizada con Amazon.

## Versión 4.1.0

*7 de mayo de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) <!--4247, 4230-->Se ha cambiado el proceso de importación de pedidos para que se ajuste a los requisitos de pedidos de Commerce. Estos cambios corrigen problemas que impiden que Commerce cree el orden correspondiente para un pedido importado. Consulte [Administrar pedidos](managing-orders.md) para obtener información sobre bloqueadores de pedidos y soluciones.

![Nuevo](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Actualizó la sección _Pedidos recientes_ del panel de la tienda y agregó una nueva vista de _Todos los pedidos_ que muestra todos sus pedidos de Amazon, incluidas las opciones de filtro y la paginación para ver más pedidos. Ver [Tablero de la tienda Amazon](amazon-store-dashboard.md) y [Ver pedidos Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) agregó la columna _[!UICONTROL Order Notes]_de la tabla_[!UICONTROL Amazon Orders]_ rediseñada en las vistas _[!UICONTROL Recent Orders]_y_[!UICONTROL All Orders]_. _[!UICONTROL Order Notes]_informa al comerciante que hay un problema con la importación del pedido. Consulte [Ver pedidos de Amazon](amazon-orders-all.md).

![Nuevo](../assets/new.svg) <!--CHAN-4013-->Se han actualizado los parámetros de condición del producto para alinearlos con el programa [Amazon renovado](https://sell.amazon.com/programs/renewed). Ver [Productos renovados](renewed-products.md).

![Nuevo](../assets/new.svg) <!--CHAN-3680-->Se han actualizado [los detalles de pedidos de Amazon](amazon-order-details.md) para incluir &quot;datos genéricos&quot; de los pedidos que Amazon cumple. Ver [Satisfecho por](fulfilled-by.md).

![Corrección](../assets/fix.svg) <!--CHAN-4069-->Se ha corregido un problema que causaba la distorsión de los iconos de la tarjeta de la tienda.

![Corrección](../assets/fix.svg) <!--CHAN-4165-->Se ha corregido un error que impedía que la pantalla de _Inicio de sesión_ apareciera después de que se agotara el tiempo de espera de la sesión.

![Corrección](../assets/fix.svg) <!--CHAN-4211-->Se ha corregido un problema que impedía que el importe de impuestos de pedidos de Amazon se importara en el nuevo pedido de Commerce.

![Corrección](../assets/fix.svg) <!--CHAN-4234-->Se ha corregido un problema que provocaba que los totales de ingresos mostrados en el panel de la tienda incluyeran pedidos con estado `Canceled` o `Error`.

![Corrección](../assets/fix.svg) <!--CHAN-4326-->Se ha corregido un problema que causaba errores de importación de pedidos asociados con extensiones de terceros que usan métodos de _Magento Shipping_ para crear pedidos.

![Corrección](../assets/fix.svg) <!--CHAN-4357-->Se corrigió un problema que causaba errores al ejecutar la sincronización cron. Se ha agregado un bloqueo al comando CLI que impide que dos trabajos cron se sincronicen al mismo tiempo.

![Corrección](../assets/fix.svg) Se ha actualizado la directiva de seguridad de contenido para que sea compatible con Commerce versión 2.3.5.

## Versión 4.0.0

*25 de marzo de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

>[!IMPORTANT]
>
>La Sales Channel de Amazon 4.0.0 no es compatible con Adobe Commerce 2.3.5. Para obtener compatibilidad con Adobe Commerce 2.3.5, actualice a la Sales Channel de Amazon 4.1.0.

![Nuevo](../assets/new.svg) presentó una nueva página de inicio de [Sales Channel de Amazon](amazon-sales-channel-home.md) con &quot;vista de tarjeta&quot; mejorada para la información de tu tienda.

![Nuevo](../assets/new.svg) presentó un nuevo [tablero de tienda](amazon-store-dashboard.md) con listados, pedidos recientes e información de configuración de tienda.

![Nuevo](../assets/new.svg) ha introducido un [proceso de incorporación](amazon-onboarding-home.md) y [configuración de tienda predeterminada](default-store-settings.md) más sencillo y optimizado para que tus tiendas se integren más rápido.

![Problema conocido](../assets/bug.svg) <!--CHAN-4102--> Cuando [creando atributos](managing-attributes.md) para importar imágenes de listados y **Vistas de la tienda** está establecido en `All Store Views (Global)`, existe un problema conocido que impide que las imágenes se importen a todas las vistas de la tienda. Si cambia la configuración de **Vistas de tienda (para importar valores en)** a un almacén específico, las imágenes se importan para ese almacén.

## Versión 3.0.1

*11 de noviembre de 2019*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Corrección](../assets/fix.svg) **Configuración de campos numéricos**: <!--CHAN-3779-->Los campos que requieren un valor basado en valores numéricos se han actualizado para aceptar únicamente caracteres numéricos. Ejemplo: Configuración de Reglas de Asignación de Precios > Campo Importe de Ajuste

![Corregir](../assets/fix.svg) **Vínculos a la Guía del usuario**: <!--CHAN-3778-->Se han corregido vínculos incorrectos de _Guía del usuario_.

![Corregir](../assets/fix.svg) **Anuncios de Amazon duplicados**: <!--CHAN-3593-->Se ha corregido un problema notificado anteriormente que causaba anuncios de Amazon duplicados. Antes de esta versión, la extensión añadía el código de país de la región de Amazon a los valores SKU al importar anuncios. El listado coincidía con el elemento de catálogo, pero la extensión creaba un nuevo listado duplicado con el SKU adjunto. Con esta versión, la extensión no modifica el SKU de los anuncios importados y no se realizan cambios en los anuncios existentes. Puedes usar la opción [!UICONTROL End Listing(s)] en Amazon para quitar los anuncios duplicados.

## Versión 3.0.0

*7 de octubre de 2019*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) **Marketplace de Amazon en el Reino Unido ya disponible**: los usuarios pueden elegir el marketplace del Reino Unido al crear e integrar una tienda Commerce. Esta actualización para el Reino Unido incluye compatibilidad adicional con:

- [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- Información del [código de impuesto sobre el producto](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

![Nuevo](../assets/new.svg) **Registro mejorado**: <!--CHAN-3642, 3672-->Se ha implementado la característica **Habilitar registro de depuración** para recopilar datos de sincronización adicionales cuando se necesite solucionar problemas. Consulte el tema [Configuración de Sales Channel](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) en la Referencia de configuración.

![Corrección](../assets/fix.svg) **Catálogo de productos**: <!--CHAN-3687-->Se ha corregido un problema que impedía que las imágenes importadas con un listado de Amazon se aplicaran al producto del catálogo de Commerce correspondiente.

![Corrección](../assets/fix.svg) **Creación de pedidos**: <!--CHAN-3708-->Se ha corregido un problema que impedía que Commerce creara pedidos para un pedido de Amazon que no coincidiera con un producto de catálogo de Commerce.

![Problema conocido](../assets/bug.svg) **Anuncios de Amazon duplicados**: <!--CHAN-3593-->Este problema hace que el catálogo cree un artículo para un anuncio importado, usando el mismo SKU pero con un código de región agregado al final. A continuación, Amazon procesa el SKU modificado como un artículo nuevo y crea un anuncio. Este problema se solucionará en una versión futura.

## Versión 2.0.0

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

>[!NOTE]
>
>La versión 1.0.0 solo estaba disponible en versiones limitadas.

![Nueva](../assets/new.svg) **Incorporación y mantenimiento simplificados**: agrega e integra con tu cuenta de vendedor de Amazon a través de un proceso paso a paso con instrucciones detalladas disponibles a través del administrador. Mantenga sus tiendas, cuentas y productos enumerados a través de un tablero.

![Nueva](../assets/new.svg) **compatibilidad con varias cuentas**: administra y supervisa varias marcas y regiones de mercado de Amazon a través del administrador.

![Nuevo](../assets/new.svg) **Precio inteligente**: establece reglas de reasignación de precios automatizadas para aumentar tus posibilidades de obtener el codiciado Buy Box. Configure los precios para que se ajusten dinámicamente al precio de Buy Box actual o al precio de competidor más bajo. Establece límites a la reasignación de precios para proteger tu margen.

![Nuevo](../assets/new.svg) **Administración de anuncios**: automatiza las listas de productos y sincroniza tu catálogo de Commerce con Amazon Marketplace mediante reglas de listado. Añada invalidaciones específicas para controlar con precisión las ofertas. Controla y administra todos tus anuncios directamente desde el administrador.

![Nuevo](../assets/new.svg) **Inventory management coherente**: Mantenga las cantidades de inventario de Commerce y Amazon en sincronización constante.

![Nuevo](../assets/new.svg) **Administración de pedidos y pedidos**: realiza un seguimiento de los pedidos de Amazon a través del panel, con una comunicación fluida y actualizaciones de inventario. Complete y rastree los envíos de pedidos según Amazon, los satisfechos por el comerciante o una combinación de métodos.

![Problema conocido](../assets/bug.svg): es posible que tenga que esperar más para actualizar las cantidades de productos. Las actualizaciones de la cantidad de productos pueden tardar aproximadamente dos horas en sincronizarse.

![Problema conocido](../assets/bug.svg) Los pedidos importados pueden tener un tipo de pedidos _Prime_ o _Premium_. Debes verificar estos pedidos en tu cuenta de vendedor de Amazon.

![Problema conocido](../assets/bug.svg) Es posible que los productos agrupados que no cumplen los requisitos se muestren como aptos para anunciarse en Amazon. Es posible que uno de los productos incluidos en el paquete no sea apto. Si tiene problemas, compruebe el estado de idoneidad para los artículos de productos agrupados.

![Problema conocido](../assets/bug.svg) Al usar Inventory management para Commerce 2.3.x, es posible que un reíndice de existencias parcial no entre en déclencheur cuando se crea un pedido. La cantidad vendible se vuelve a calcular cada hora, lo que puede causar un exceso de ventas durante este intervalo de actualización.
