---
title: Tareas previas a la configuración para  [!DNL Amazon sales channel]
description: Revise las tareas necesarias que debe completar antes de integrar su tienda de Adobe Commerce o Magento Open Source en la Sales Channel de Amazon.
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Tareas previas a la configuración de [!DNL Amazon sales channel]

Antes de la [integración de tiendas](./store-integration.md), debes asegurarte de que tu cuenta de [!DNL Amazon Seller Central] y tu cuenta de [!DNL Commerce] estén listos para la integración. Para integrarse correctamente, hay algunas tareas de preconfiguración necesarias.

Cuando configura su primera tienda Amazon en el canal de ventas de Amazon, aparece una lista de tareas de configuración. Se recomienda revisar estas tareas antes de [agregar una tienda Amazon](./store-integration.md). Después de agregar su primera tienda, puede revisar estas tareas en la vista Aprendizaje y preparación del canal de ventas de Amazon [página de inicio](./amazon-sales-channel-home.md).

## 1. Habilitar tareas en segundo plano en [!DNL Commerce]

Todos los productos y datos sincronizados entre [!DNL Commerce] y Amazon se administran mediante un [trabajo cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). Cuando completa tareas como agregar o actualizar listados y recibe pedidos, un trabajo cron envía y recibe datos entre su servidor [!DNL Commerce] y su cuenta [!DNL Amazon Seller Central].

- [Habilitar [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- Para obtener el máximo rendimiento, [establezca [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) para que se ejecute una vez cada cinco minutos.

## 2. Cree su cuenta de [!DNL Amazon Seller Central]

Antes de comenzar a configurar el canal de ventas de Amazon, debe tener una cuenta activa de [!DNL Amazon Seller Central]. Si no tienes una cuenta de vendedor de Amazon en la región [Norteamérica (EE. UU., CA, MX)](https://sell.amazon.com/){target="_blank"} o [Europa (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"}, puedes completar el proceso de configuración de la cuenta de vendedor de Amazon.

El canal de ventas de Amazon requiere una cuenta de [!DNL Professional Seller] en [!DNL Amazon Seller Central]. Amazon cobra una suscripción mensual y tarifas por vender. Ver [Amazon: elige tu plan de venta](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Asegúrate de que eres un vendedor de Amazon autorizado

Para integrarse, debe tener una cuenta de [!DNL Amazon Seller Central] aprobada. Su cuenta no debe tener restricciones para productos o categorías. Algunos productos y categorías requieren aprobación antes de crear anuncios. Revise las directivas de Amazon para la aprobación de categorías y productos con el fin de asegurarse de que se aprueban los productos. Ver [Amazon: categorías y productos que requieren aprobación](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (se requiere el inicio de sesión en la central de vendedores).

También es importante asegurarse de que ha configurado lo siguiente en su cuenta de [!DNL Amazon Seller Central]:

- Asegúrese de que la política de devoluciones sea igual o mejor que la política de devoluciones de Amazon. Ver [Amazon: Política de devoluciones](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Asegúrese de que la configuración de impuestos está establecida. Ver [Amazon: Políticas fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (se requiere el inicio de sesión en la Central de vendedores).

- Asegúrese de que los métodos de envío estén configurados con precisión. Para configurar los métodos de envío que se ofrecen a los clientes [!DNL Commerce] para que cumplan sus pedidos de Amazon, actualice [Amazon: Configuración de envío](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} en su cuenta de [!DNL Amazon Seller Central].

## 4. Asegúrate de que el IVA está configurado para tus tiendas

(Utilizado principalmente por vendedores del Reino Unido). Amazon recomienda registrarse en el [Servicio de cálculo de IVA de Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Si eliges un método diferente, eres responsable del cumplimiento del IVA.

>[!NOTE]
>
>Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

## 5. Aumente el número de coincidencias automáticas de catálogo

Durante la incorporación, el canal de ventas de Amazon usa atributos de producto para hacer coincidir los anuncios de Amazon existentes (si corresponde) con los productos existentes en el catálogo [!DNL Commerce]. Después de la incorporación, estos atributos de producto se usan para publicar los elementos de catálogo [!DNL Commerce] en un listado de Amazon y para sincronizar los datos de producto entre [!DNL Commerce] y Amazon.

Para que el número máximo de [!DNL Commerce] productos coincida automáticamente con los listados de Amazon, debe crear un conjunto de atributos de productos para el catálogo [!DNL Commerce]. Antes de configurar el canal de ventas de Amazon, debe agregar [!DNL Commerce] atributos de producto para que coincidan con estos atributos de Amazon, por ejemplo: ASIN, EAN, ISBN, UPC o GCID. Ver [Crear un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure la divisa y la conversión (según sea necesario)

Si la tienda Amazon usa una divisa diferente a la configurada para la tienda [!DNL Commerce], [habilita la divisa](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) y establece la [tasa de conversión de divisa](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Cree un atributo de condición de producto (según sea necesario)

Si los anuncios de Amazon contienen más de una condición de producto (como _nuevo_, _usado_ o _como nuevo_), crea un atributo [!DNL Commerce] y asigna valores de condición. Debe asignar este atributo durante la incorporación al atributo de producto Condición de Amazon. Consulte [Creación de atributos para Amazon](./ob-creating-magento-attributes.md).

## 8. Configurar el método de envío [!DNL Amazon Seller Central]

Para configurar los métodos de envío que quieres ofrecer para cumplir tus pedidos de Amazon, consulta _Configuración y configuración de envío_ en tu cuenta de [!DNL Amazon Seller Central].

## Configuraciones adicionales

Cuando su cuenta de Amazon está configurada y activa, hay varias [!DNL Commerce] recomendaciones que ayudan a optimizar el proceso de incorporación al canal de ventas de Amazon.

### Revise y anote los productos que desee excluir

Es posible que no quiera que algunos productos aparezcan en Amazon. El canal de ventas de Amazon tiene un motor de reglas de listado que se utiliza para determinar qué productos cumplen los requisitos para su publicación en Amazon. [Las reglas de listado](./listing-rules.md) le permiten seleccionar subconjuntos de productos para publicar (o no publicar) en su cuenta de [!DNL Amazon Seller Central], por ejemplo, mediante la selección de categorías o la definición de uno o más atributos de productos. Al igual que las reglas de precio de [!DNL Commerce] [catálogo](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) o [carro de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html), los atributos de producto utilizados para la idoneidad para el anuncio de Amazon deben tener **[!UICONTROL Use for Promo Rule Conditions]** establecido en `Yes`. Ver **[!UICONTROL Use for Promo Rule Conditions]** en [Atributos del producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Indique la región [!DNL Amazon Seller Central] como inactiva

Para facilitar la transición de datos sin errores durante la integración, se recomienda establecer la región de Amazon en el estado `Inactive` en Configuración > Información de cuenta > Configuración de vacaciones. Cuando finalice la instalación, vuelva a cambiar el estado a `Active` en Amazon.

![Siguiente icono](assets/btn-next.png) [**Continuar creando [!DNL Commerce] atributos**](./ob-creating-magento-attributes.md)
