---
title: Tareas comunes de procesamiento de pedidos de Amazon
description: Utilice el correspondiente [!DNL Commerce] pedidos creados para pedidos de Amazon para administrar la actividad de pedidos y el procesamiento en [!UICONTROL Commerce] Administrador.
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Tareas comunes de procesamiento de pedidos de Amazon

[Procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) Puede administrar sus pedidos de Amazon, incluido el envío por correo electrónico al comprador, el cumplimiento del pedido (envío), la emisión de créditos/reembolsos, la adición de comentarios y mucho más. Para administrar sus pedidos de Amazon, su [**Importar pedidos de Amazon**](./order-settings.md) la configuración debe establecerse en `Enabled` por lo que correspondiente [!DNL Commerce] los pedidos se crean cuando se reciben los pedidos de Amazon. La información de pedidos de Amazon se muestra en la *[!UICONTROL Recent Orders]* del tablero de la tienda.

Cuando está habilitado, corresponde a [!DNL Commerce] los pedidos se crean para pedidos de Amazon y el número de pedido de Amazon se muestra en la _[!UICONTROL Order Number]_columna. Si corresponde a [!DNL Commerce] Para crear un pedido, haga clic en el número de pedido para abrir el pedido en [Procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) página. Puede administrar el pedido como lo hace con el otro [[!DNL Commerce] procesamiento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

El [!DNL Commerce] el número de pedido no se muestra con _[!UICONTROL Recent Orders]_información. El número de pedido de Commerce solo se muestra al hacer clic en el número de pedido en el panel de la tienda y al abrir el pedido en [Procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Al ver el [!DNL Commerce] pedido, el número de pedido de Amazon aparece en la *[!UICONTROL Payment & Shipping Method]*sección. También incluye opciones para *[!UICONTROL View or Cancel Amazon Order]*y *[!UICONTROL View all Amazon Orders]*, según el estado de envío del pedido.

Consulte [cancelar un pedido no enviado](./cancel-unshipped-order.md).

![Información de pedido de Amazon en el pedido de Commerce](assets/amazon-order-number-payment-info.png){width="500"}

Al procesar un pedido de Amazon, el canal de ventas de Amazon actualiza y sincroniza la información del pedido con su [!DNL Amazon Seller Central] cuenta. La configuración de cron determina la frecuencia con la que se sincroniza la información de pedidos entre Amazon y el canal de ventas de Amazon.

Common Commerce [procesamiento de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) las tareas incluyen:

- [Acciones de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Búsqueda de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Procesar un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Ver un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Procesar un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Información de pedido y cuenta](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Información de dirección](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Pago y método de envío](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Revisar artículos pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Emisión de un crédito/reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Cumplimiento/envío de un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Crear una factura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Cancelar un pedido no enviado](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si un pedido está en `Unshipped` estado, puede [cancelar un pedido de Amazon](./cancel-unshipped-order.md) en el [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) página. Si se ha enviado un pedido, no se puede cancelar.

Consulte [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
