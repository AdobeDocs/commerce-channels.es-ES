---
title: Tareas previas a la configuración
description: Revise las tareas necesarias que deben completarse antes de integrar su Adobe Commerce o tienda de Magento Open Source en la Sales Channel de Amazon.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Tareas previas a la configuración

Antes [Integración de tiendas](./store-integration.md), debe asegurarse de que su [!DNL Amazon Seller Central] y su [!DNL Commerce] están listas para la integración. Para integrar correctamente, hay algunas tareas previas a la configuración necesarias.

Al configurar la primera tienda de Amazon en el canal de ventas de Amazon, aparece una lista de tareas de configuración. Se recomienda revisar estas tareas antes de [añadir una tienda de Amazon](./store-integration.md). Después de añadir la primera tienda, puede revisar estas tareas en la vista Aprendizaje y preparación del canal de ventas de Amazon [página principal](./amazon-sales-channel-home.md).

## 1. Habilite tareas en segundo plano en [!DNL Commerce]

Todos los productos y datos sincronizados entre [!DNL Commerce] y Amazon se administra mediante un [trabajo cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Al completar tareas como agregar o actualizar anuncios y recibir pedidos, un trabajo cron envía y recibe datos entre sus [!DNL Commerce] backend y el [!DNL Amazon Seller Central] cuenta.

- [Habilitar [!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Para obtener el máximo rendimiento, [set [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} para ejecutarse una vez cada cinco minutos.

## 2. Cree su [!DNL Amazon Seller Central] account

Antes de comenzar a configurar el canal de ventas de Amazon, debe tener una [!DNL Amazon Seller Central] cuenta. Si no tiene una cuenta de vendedor de Amazon existente en la [América del Norte (EE.UU., CA, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} o [Europeo (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide)región {target=&quot;_blank&quot;}, puede completar el proceso de configuración de la cuenta de vendedor de Amazon.

El canal de ventas de Amazon requiere un [!DNL Professional Seller] cuenta en [!DNL Amazon Seller Central]. Amazon cobra una suscripción mensual y tarifas de venta. Consulte [Amazon: Elige tu plan de ventas](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Asegúrese de que es un vendedor de Amazon aprobado

Para la integración, debe tener una [!DNL Amazon Seller Central] cuenta. Su cuenta no debe tener restricciones para productos o categorías. Algunos productos y categorías requieren aprobación antes de crear anuncios. Revise las directivas de Amazon para la aprobación de categorías y productos para asegurarse de que sus productos están aprobados. Consulte [Amazon: Categorías y productos que requieren aprobación](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (se requiere inicio de sesión en Seller Central).

También es importante asegurarse de que ha configurado lo siguiente en su [!DNL Amazon Seller Central] cuenta:

- Asegúrese de que la directiva de retorno sea tan buena como o mejor que la directiva de retorno de Amazon. Consulte [Amazon: Política de retorno](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Asegúrese de que la configuración de impuestos esté configurada. Consulte [Amazon: Políticas fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (se requiere inicio de sesión en Seller Central).

- Asegúrese de que los métodos de envío estén configurados con precisión. Para configurar los métodos de envío que [!DNL Commerce] se ofrecen a los clientes de para que cumplan con sus pedidos de Amazon, actualicen los [Amazon: Configuración de envío](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} en su [!DNL Amazon Seller Central] cuenta.

## 4. Asegúrese de que el IVA esté configurado para sus tiendas

(Utilizado principalmente por vendedores del Reino Unido). Amazon recomienda registrarse en [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Si elige un método diferente, es responsable del cumplimiento del IVA.

>[!NOTE]
>
>Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

## 5. Aumente el número de coincidencias automáticas del catálogo

Durante la incorporación, el canal de ventas de Amazon usa atributos de producto para hacer coincidir sus anuncios de Amazon existentes (si corresponde) con los productos existentes en su [!DNL Commerce] catálogo. Después de la incorporación, estos atributos de producto se utilizan para publicar su [!DNL Commerce] artículos de catálogo en una lista de Amazon y para sincronizar los datos de producto entre [!DNL Commerce] y Amazon.

Para tener el número más alto de [!DNL Commerce] los productos coinciden automáticamente con los listados de Amazon, debe crear un conjunto de atributos de producto para [!DNL Commerce] catálogo. Antes de configurar el almacén de canales de ventas de Amazon, debe agregar [!DNL Commerce] atributos de producto para que coincidan con estos atributos de Amazon, por ejemplo: ASIN, EAN, ISBN, UPC o GCID. Consulte [Cree un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure su moneda y conversión (según sea necesario)

Si la tienda de Amazon usa una moneda diferente a la configurada para su [!DNL Commerce] almacenar, [activar la moneda](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} y establezca la variable [tasa de conversión de moneda](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Crear un atributo de condición del producto (según sea necesario)

Si las listas de Amazon contienen más de una condición de producto (por ejemplo, _new_, _used_ o _like new_), cree un [!DNL Commerce] y asigne valores de condición. Debe asignar este atributo durante la incorporación al atributo de producto Condición de Amazon. Consulte [Creación de atributos para Amazon](./ob-creating-magento-attributes.md).

## 8. Configure las [!DNL Amazon Seller Central] método de envío

Para configurar los métodos de envío que desea ofrecer para cumplir sus pedidos de Amazon, consulte [Configuración y configuración de envío][10] en su [!DNL Amazon Seller Central] cuenta.

## Configuraciones adicionales

Cuando la cuenta de Amazon está configurada y activa, hay varios [!DNL Commerce] recomendaciones que ayudan a optimizar el proceso de incorporación del canal de ventas de Amazon.

### Revise y anote los productos que desee excluir

Es posible que no quiera que algunos productos aparezcan en la lista de Amazon. El canal de ventas de Amazon tiene un motor de reglas de listado que se utiliza para determinar qué productos son aptos para su publicación en Amazon. [Reglas de lista](./listing-rules.md) le permite seleccionar subconjuntos de productos para publicarlos (o no publicarlos) en su [!DNL Amazon Seller Central] , como por selección de categorías o definiendo uno o más atributos de producto. Like [!DNL Commerce] [catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} o [carro de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;} reglas de precios, los atributos de producto utilizados para los requisitos de listado de Amazon deben tener **[!UICONTROL Use for Promo Rule Conditions]** configure como `Yes`. Consulte la **[!UICONTROL Use for Promo Rule Conditions]** en [Atributos del producto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Configure las [!DNL Amazon Seller Central] de región a inactiva

Para facilitar la transición de datos sin errores durante la integración, se recomienda establecer la región de Amazon en `Inactive` en Configuración > Información de la cuenta > Configuración de las vacaciones. Consulte [Amazon: Estado de anuncio de las vacaciones][11]. Cuando se haya completado la configuración, vuelva a cambiar el estado a `Active` en Amazon.

![Icono Siguiente](assets/btn-next.png) [**Continúe creando [!DNL Commerce] Atributos**](./ob-creating-magento-attributes.md)
