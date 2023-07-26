---
title: Tareas previas a la configuración para [!DNL Amazon sales channel]
description: Revise las tareas necesarias que debe completar antes de integrar su tienda de Adobe Commerce o Magento Open Source en la Sales Channel de Amazon.
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Tareas previas a la configuración para [!DNL Amazon sales channel]

Antes [Integración de tienda](./store-integration.md), debe asegurarse de que sus [!DNL Amazon Seller Central] y su [!DNL Commerce] Las cuentas de están listas para la integración de. Para integrarse correctamente, hay algunas tareas de preconfiguración necesarias.

Cuando configura su primera tienda Amazon en el canal de ventas de Amazon, aparece una lista de tareas de configuración. Se recomienda que revise estas tareas antes de comenzar [añadir una tienda Amazon](./store-integration.md). Después de añadir su primera tienda, puede revisar estas tareas en la vista Aprendizaje y preparación del canal de ventas de Amazon [página principal](./amazon-sales-channel-home.md).

## 1. Habilitar tareas en segundo plano en [!DNL Commerce]

Todos los productos y datos sincronizados entre [!DNL Commerce] y Amazon está gestionado por un [trabajo cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). Cuando completa tareas como agregar o actualizar listados y recibe pedidos, un trabajo cron envía y recibe datos entre sus [!DNL Commerce] back-end y su [!DNL Amazon Seller Central] cuenta.

- [Activar [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- Para obtener el máximo rendimiento, [set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) para ejecutar una vez cada cinco minutos.

## 2. Cree su [!DNL Amazon Seller Central] account

Antes de comenzar a configurar el canal de ventas de Amazon, debe tener un activo [!DNL Amazon Seller Central] cuenta. Si no tienes una cuenta de vendedor de Amazon en [América del Norte (EE.UU., CA, MX)](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} región, puedes completar el proceso de configuración de la cuenta de vendedor de Amazon.

El canal de ventas de Amazon requiere un [!DNL Professional Seller] cuenta en [!DNL Amazon Seller Central]. Amazon cobra una suscripción mensual y tarifas por vender. Consulte [Amazon: elige tu plan de venta](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Asegúrate de que eres un vendedor de Amazon autorizado

Para integrarse, debe tener un aprobado [!DNL Amazon Seller Central] cuenta. Su cuenta no debe tener restricciones para productos o categorías. Algunos productos y categorías requieren aprobación antes de crear anuncios. Revise las directivas de Amazon para la aprobación de categorías y productos con el fin de asegurarse de que se aprueban los productos. Consulte [Amazon: categorías y productos que requieren aprobación](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (Se requiere el inicio de sesión en Seller Central).

También es importante asegurarse de que ha configurado lo siguiente en su [!DNL Amazon Seller Central] cuenta:

- Asegúrese de que la política de devoluciones sea igual o mejor que la política de devoluciones de Amazon. Consulte [Amazon: Política de devoluciones](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Asegúrese de que la configuración de impuestos está establecida. Consulte [Amazon: Políticas Fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (Se requiere el inicio de sesión en Seller Central).

- Asegúrese de que los métodos de envío estén configurados con precisión. Para configurar los métodos de envío que [!DNL Commerce] se ofrecen a los clientes de para que cumplan sus pedidos de Amazon, actualice el [Amazon: Configuración de envío](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} en su [!DNL Amazon Seller Central] cuenta.

## 4. Asegúrate de que el IVA está configurado para tus tiendas

(Utilizado principalmente por vendedores del Reino Unido). Amazon recomienda registrarse en [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Si eliges un método diferente, eres responsable del cumplimiento del IVA.

>[!NOTE]
>
>Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

## 5. Aumente el número de coincidencias automáticas de catálogo

Durante la incorporación, el canal de ventas de Amazon utiliza atributos de producto para hacer coincidir los anuncios de Amazon existentes (si corresponde) con los productos existentes en su [!DNL Commerce] catálogo. Después de la incorporación, estos atributos de producto se utilizan para publicar su [!DNL Commerce] elementos de catálogo a un listado de Amazon y para sincronizar los datos de producto entre [!DNL Commerce] y Amazon.

Para tener el número más alto de [!DNL Commerce] Los productos de coinciden automáticamente con los listados de Amazon. Debe crear un conjunto de atributos de producto para [!DNL Commerce] catálogo. Antes de configurar el almacén de canales de ventas de Amazon, debe añadir [!DNL Commerce] atributos de producto para que coincidan con estos atributos de Amazon, por ejemplo: ASIN, EAN, ISBN, UPC o GCID. Consulte [Creación de un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure la divisa y la conversión (según sea necesario)

Si su tienda Amazon usa una divisa diferente a la configurada para su [!DNL Commerce] tienda, [habilitar la moneda](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) y configure el [tasa de conversión de moneda](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Cree un atributo de condición de producto (según sea necesario)

Si los anuncios de Amazon contienen más de una condición de producto (como _nuevo_, _usado_, o _como nuevo_), cree un [!DNL Commerce] y asigne valores de condición. Debe asignar este atributo durante la incorporación al atributo de producto Condición de Amazon. Consulte [Creación de atributos para Amazon](./ob-creating-magento-attributes.md).

## 8. Configure su [!DNL Amazon Seller Central] método de envío

Para configurar los métodos de envío que desea ofrecer para cumplir los pedidos de Amazon, consulte _Configuración y configuración de envío_ en su [!DNL Amazon Seller Central] cuenta.

## Configuraciones adicionales

Cuando su cuenta de Amazon está configurada y activa, hay varias [!DNL Commerce] recomendaciones que ayudan a optimizar el proceso de incorporación al canal de ventas de Amazon.

### Revise y anote los productos que desee excluir

Es posible que no quiera que algunos productos aparezcan en Amazon. El canal de ventas de Amazon tiene un motor de reglas de listado que se utiliza para determinar qué productos cumplen los requisitos para su publicación en Amazon. [Reglas de listado](./listing-rules.md) le permite seleccionar subconjuntos de productos para publicarlos (o no publicarlos) en su [!DNL Amazon Seller Central] cuenta, como por selección de categoría o definiendo uno o varios atributos de producto. Like [!DNL Commerce] [catalogar](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) o [carro de compras](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) reglas de precios, los atributos de producto utilizados para la idoneidad del listado de Amazon deben tener **[!UICONTROL Use for Promo Rule Conditions]** establezca en `Yes`. Consulte la **[!UICONTROL Use for Promo Rule Conditions]** in [Atributos del producto](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Configure su [!DNL Amazon Seller Central] región a inactiva

Para facilitar la transición de datos sin errores durante la integración, se recomienda establecer la región de Amazon en `Inactive` en Configuración > Información de la cuenta > Configuración de vacaciones. Cuando finalice la configuración, vuelva a cambiar el estado a `Active` en Amazon.

![Icono Siguiente](assets/btn-next.png) [**Continuar con la creación [!DNL Commerce] Atributos**](./ob-creating-magento-attributes.md)
