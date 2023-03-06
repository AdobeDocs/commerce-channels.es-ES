---
title: Tareas de procesamiento de orden común
description: Utilice el correspondiente [!DNL Commerce] pedidos creados para pedidos de Amazon para administrar la actividad de pedidos y el procesamiento en [!UICONTROL Commerce] Administrador.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Tareas de procesamiento de orden común

[[!DNL Commerce] procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} Puede administrar sus pedidos de Amazon, incluido el envío por correo electrónico al comprador, el cumplimiento del pedido (envío), la emisión de créditos/reembolsos, la adición de comentarios y mucho más. Para administrar sus pedidos de Amazon, su [**Importar pedidos de Amazon**](./order-settings.md) la configuración debe establecerse en `Enabled` por lo que correspondiente [!DNL Commerce] los pedidos se crean cuando se reciben los pedidos de Amazon. La información de pedidos de Amazon se muestra en la *[!UICONTROL Recent Orders]* del tablero de la tienda.

Cuando está habilitado, corresponde a [!DNL Commerce] los pedidos se crean para pedidos de Amazon y el número de pedido de Amazon se muestra en la _[!UICONTROL Order Number]_columna. Si corresponde a [!DNL Commerce] Para crear un pedido, haga clic en el número de pedido para abrir el pedido en [!DNL Commerce] [procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

El [!DNL Commerce] el número de pedido no se muestra con _[!UICONTROL Recent Orders]_información. El [!DNL Commerce] el número de pedido solo se muestra al hacer clic en el número de pedido en el panel del almacén y al abrir el pedido en [[!DNL Commerce] procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}. Al ver el [!DNL Commerce] pedido, el número de pedido de Amazon aparece en la *[!UICONTROL Payment & Shipping Method]*sección. También incluye opciones para *[!UICONTROL View or Cancel Amazon Order]*y *[!UICONTROL View all Amazon Orders]*, según el estado de envío del pedido.

Consulte [cancelar un pedido no enviado](./cancel-unshipped-order.md).

![Información de pedido de Amazon en el pedido de Commerce](assets/amazon-order-number-payment-info.png)

Al procesar un pedido de Amazon, el canal de ventas de Amazon actualiza y sincroniza la información del pedido con su [!DNL Amazon Seller Central] cuenta. La configuración de cron determina la frecuencia con la que se sincroniza la información de pedidos entre Amazon y el canal de ventas de Amazon.

Común [!DNL Commerce] [procesamiento de pedidos](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} las tareas incluyen:

- [Acciones de pedido](https://docs.magento.com/user-guide/sales/order-actions.html){target="_blank"}
- [Búsqueda de pedidos](https://docs.magento.com/user-guide/sales/orders-search.html){target="_blank"}
- [Procesar un pedido](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}
   - [Ver un pedido](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target="_blank"}
   - [Procesar un pedido](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target="_blank"}
   - [Información de pedido y cuenta](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target="_blank"}
   - [Información de dirección](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target="_blank"}
   - [Pago y método de envío](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target="_blank"}
   - [Revisar artículos pedidos](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target="_blank"}
- [Emisión de un crédito/reembolso](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target="_blank"}
- [Cumplimiento/envío de un pedido](https://docs.magento.com/user-guide/sales/shipments-create.html){target="_blank"}
- [Crear una factura](https://docs.magento.com/user-guide/sales/invoice-create.html){target="_blank"}
- [Cancelar un pedido no enviado](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si un pedido está en `Unshipped` estado, puede [cancelar un pedido de Amazon](./cancel-unshipped-order.md) en el [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Si se ha enviado un pedido, no se puede cancelar.

Consulte [Commerce Order Management](https://docs.magento.com/user-guide/sales/order-management.html){target="_blank"}.
