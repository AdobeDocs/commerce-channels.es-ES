---
title: Tareas comunes de procesamiento de pedidos
description: Utilice el [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Administrador.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Tareas comunes de procesamiento de pedidos

[[!DNL Commerce] procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} puede administrar sus pedidos de Amazon, incluido el envío por correo electrónico al comprador, el cumplimiento del pedido (envío), la emisión de créditos/reembolsos, la adición de comentarios y mucho más. Para administrar sus pedidos de Amazon, su [**Importar pedidos de Amazon**](./order-settings.md) debe configurarse como `Enabled` de modo que [!DNL Commerce] los pedidos se crean cuando se reciben los pedidos de Amazon. La información de pedidos de Amazon se muestra en la sección *[!UICONTROL Recent Orders]* del panel de almacenamiento.

Cuando está activado, corresponde [!DNL Commerce] los pedidos se crean para los pedidos de Amazon y el número de pedido de Amazon se muestra en la _[!UICONTROL Order Number]_para abrir el Navegador. Si corresponde a [!DNL Commerce] se crea el pedido, haga clic en el número de pedido para abrirlo en el [!DNL Commerce] [procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html)página {target=&quot;_blank&quot;}. Puede administrar el orden como lo hace con el otro [[!DNL Commerce] procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

La variable [!DNL Commerce] el número de pedido no se muestra con la variable _[!UICONTROL Recent Orders]_información. La variable [!DNL Commerce] el número de pedido solo se muestra al hacer clic en el número de pedido en el panel de almacenamiento y abrir el pedido en [[!DNL Commerce] procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Al ver la variable [!DNL Commerce] el número de pedido de Amazon aparece en la sección *[!UICONTROL Payment & Shipping Method]*para obtener más información. También incluye opciones para *[!UICONTROL View or Cancel Amazon Order]*y *[!UICONTROL View all Amazon Orders]*, según el estado de envío del pedido.

Consulte [cancelar un pedido sin enviar](./cancel-unshipped-order.md).

![Información de pedido de Amazon en el orden de comercio](assets/amazon-order-number-payment-info.png)

Al procesar un pedido de Amazon, el canal de ventas de Amazon actualiza y sincroniza la información del pedido con su [!DNL Amazon Seller Central] cuenta. La configuración de su cron determina la frecuencia con la que se sincroniza la información de pedidos entre el canal de ventas de Amazon y Amazon.

Frecuentes [!DNL Commerce] [procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html)Las tareas {target=&quot;_blank&quot;} incluyen:

- [Acciones de pedido](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Búsqueda de pedidos](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Procesar un pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Ver un pedido](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Procesar un pedido](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Información de pedidos y cuentas](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Información de dirección](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Método de Pago y Envío](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Revisar elementos ordenados](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Emisión de un crédito/reembolso](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Cumplimentar/enviar un pedido](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Crear una factura](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Cancelar un pedido sin enviar](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si un pedido está en `Unshipped` estado, puede [cancelar una solicitud de Amazon](./cancel-unshipped-order.md) en el [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Si se ha enviado un pedido, no se puede cancelar.

Consulte [Administración de pedidos de comercio](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
