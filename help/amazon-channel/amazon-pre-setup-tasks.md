---
title: Tareas previas a la configuración
description: Revise las tareas necesarias que deben completarse antes de integrar su tienda de Adobe o Magento Open Source en la Sales Channel de Amazon.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Tareas previas a la configuración

Antes de [Store Integration](./store-integration.md), debe asegurarse de que su cuenta [!DNL Amazon Seller Central] y su cuenta [!DNL Commerce] estén listas para la integración. Para integrar correctamente, hay algunas tareas previas a la configuración necesarias.

Al configurar la primera tienda de Amazon en el canal de ventas de Amazon, aparece una lista de tareas de configuración. Se recomienda revisar estas tareas antes de [agregar una tienda de Amazon](./store-integration.md). Después de agregar su primera tienda, puede revisar estas tareas en la vista Aprendizaje y preparación de la página de inicio [del canal de ventas de Amazon](./amazon-sales-channel-home.md).

## 1. Habilitar tareas en segundo plano en [!DNL Commerce]

Todos los productos y datos sincronizados entre [!DNL Commerce] y Amazon se administran mediante un [trabajo cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Cuando se completan tareas como agregar o actualizar anuncios y recibir pedidos, un trabajo cron envía y recibe datos entre el back-end [!DNL Commerce] y su cuenta [!DNL Amazon Seller Central].

- [ [!DNL Commerce] Activar](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Para obtener el máximo rendimiento, [configure [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} para que se ejecute una vez cada cinco minutos.

## 2. Cree su cuenta [!DNL Amazon Seller Central]

Antes de comenzar a configurar el canal de ventas de Amazon, debe tener una cuenta [!DNL Amazon Seller Central] activa. Si no tiene una cuenta de Amazon Seller existente en la región [América del Norte (EE. UU., CA, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} o [Europa (Reino Unido)](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;}, puede completar el proceso de configuración de la cuenta de vendedor de Amazon.

El canal de ventas de Amazon requiere una cuenta [!DNL Professional Seller] en [!DNL Amazon Seller Central]. Amazon cobra una suscripción mensual y tarifas de venta. Consulte [Amazon: Elija su plan de venta](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Asegúrese de que es un vendedor de Amazon aprobado

Para integrar, debe tener una cuenta [!DNL Amazon Seller Central] aprobada. Su cuenta no debe tener restricciones para productos o categorías. Algunos productos y categorías requieren aprobación antes de crear anuncios. Revise las directivas de Amazon para la aprobación de categorías y productos para asegurarse de que sus productos están aprobados. Consulte [Amazon: Categorías y productos que requieren aprobación](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (se requiere el inicio de sesión de Seller Central).

También es importante asegurarse de que ha configurado lo siguiente en su cuenta [!DNL Amazon Seller Central]:

- Asegúrese de que la directiva de retorno sea tan buena como o mejor que la directiva de retorno de Amazon. Consulte [Amazon: Directiva de retorno](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Asegúrese de que la configuración de impuestos esté configurada. Consulte [Amazon: Directivas de impuestos](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (se requiere el inicio de sesión de Seller Central).

- Asegúrese de que los métodos de envío estén configurados con precisión. Para configurar los métodos de envío que [!DNL Commerce] se ofrecen a los clientes para que cumplan sus pedidos de Amazon, actualice el [Amazon: Configuración de envío](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} en su cuenta [!DNL Amazon Seller Central].

## 4. Asegúrese de que el IVA esté configurado para sus tiendas

(Utilizado principalmente por vendedores del Reino Unido). Amazon recomienda registrarse en [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Si elige un método diferente, es responsable del cumplimiento del IVA.

>[!NOTE]
>
>Amazon puede tardar entre 10 y 14 días en verificar y activar su cuenta del servicio de cálculo de IVA.

## 5. Aumente el número de coincidencias automáticas del catálogo

Durante la incorporación, el canal de ventas de Amazon usa atributos de producto para coincidir con los anuncios de Amazon existentes (si corresponde) con los productos existentes en su catálogo [!DNL Commerce]. Después de la incorporación, estos atributos de producto se utilizan para publicar sus [!DNL Commerce] artículos de catálogo en un listado de Amazon y para sincronizar los datos del producto entre [!DNL Commerce] y Amazon.

Para que el mayor número de [!DNL Commerce] productos coincida automáticamente con los listados de Amazon, debe crear un conjunto de atributos de producto para su catálogo [!DNL Commerce]. Antes de configurar el almacén de canales de ventas de Amazon, debe agregar [!DNL Commerce] atributos de producto para que coincidan con estos atributos de Amazon, por ejemplo: ASIN, EAN, ISBN, UPC o GCID. Consulte [Crear un atributo de producto en [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configure su moneda y conversión (según sea necesario)

Si la tienda de Amazon utiliza una moneda diferente a la configurada para su almacén [!DNL Commerce], [habilite la moneda](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} y establezca la [tasa de conversión de moneda](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Crear un atributo de condición del producto (según sea necesario)

Si las listas de Amazon contienen más de una condición de producto (como _new_, _used_ o _like new_), cree un atributo [!DNL Commerce] y asigne valores de condición. Debe asignar este atributo durante la incorporación al atributo de producto Condición de Amazon. Consulte [Creación de atributos para Amazon](./ob-creating-magento-attributes.md).

## 8. Configure su método de envío [!DNL Amazon Seller Central]

Para configurar los métodos de envío que desea ofrecer para cumplir sus pedidos de Amazon, consulte [Configuración y configuración de envío][10] en su cuenta [!DNL Amazon Seller Central].

## Configuraciones adicionales

Cuando su cuenta de Amazon está configurada y activa, existen varias [!DNL Commerce] recomendaciones que ayudan a optimizar el proceso de incorporación del canal de ventas de Amazon.

### Revise y anote los productos que desee excluir

Es posible que no quiera que algunos productos aparezcan en la lista de Amazon. El canal de ventas de Amazon tiene un motor de reglas de listado que se utiliza para determinar qué productos son aptos para su publicación en Amazon. [Las ](./listing-rules.md) reglas de lista permiten seleccionar subconjuntos de productos para publicarlos (o no) en su  [!DNL Amazon Seller Central] cuenta, como por selección de categorías o definiendo uno o más atributos de producto. Al igual que [!DNL Commerce] [catálogo](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} o [carro de compras](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}, los atributos de producto utilizados para los requisitos de listado de Amazon deben tener **[!UICONTROL Use for Promo Rule Conditions]** establecido en `Yes`. Consulte **[!UICONTROL Use for Promo Rule Conditions]** en [Atributos del producto](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Configure la región [!DNL Amazon Seller Central] como inactiva

Para facilitar la transición de datos sin errores durante la integración, se recomienda establecer la región de Amazon en estado `Inactive` en Configuración > Información de la cuenta > Configuración de las vacaciones. Consulte [Amazon: Estado de listado de Vacaciones][11]. Cuando haya completado la configuración, vuelva a cambiar el estado a `Active` en Amazon.

![Siguiente ](assets/btn-next.png) [**iconoContinuar con la creación de  [!DNL Commerce] atributos**](./ob-creating-magento-attributes.md)
