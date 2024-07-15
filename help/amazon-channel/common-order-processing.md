---
title: Tareas comunes de procesamiento de pedidos de Amazon
description: Utilice los  [!DNL Commerce] pedidos creados para los pedidos de Amazon correspondientes para administrar la actividad de pedidos y el procesamiento en el administrador de [!UICONTROL Commerce].
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Tareas comunes de procesamiento de pedidos de Amazon

[Procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) puede administrar tus pedidos de Amazon, como enviarle correos electrónicos al comprador, cumplir el pedido (envío), emitir créditos/reembolsos, agregar comentarios y mucho más. Para administrar los pedidos de Amazon, la configuración de [**Importar pedidos de Amazon**](./order-settings.md) debe establecerse en `Enabled` para que se creen los pedidos de [!DNL Commerce] correspondientes cuando se reciban los pedidos de Amazon. La información de pedidos de Amazon se muestra en la sección *[!UICONTROL Recent Orders]* del panel del almacén.

Cuando está habilitada, se crean los [!DNL Commerce] pedidos correspondientes para los pedidos de Amazon y el número de pedido de Amazon se muestra en la columna _[!UICONTROL Order Number]_. Si se crea un pedido [!DNL Commerce] correspondiente, haga clic en el número de pedido para abrir el pedido en la página [Procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Puede administrar el pedido al igual que lo hace con los otros [[!DNL Commerce] procesamientos de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

El número de pedido [!DNL Commerce] no se muestra con la información _[!UICONTROL Recent Orders]_. El número de pedido de Commerce solo se muestra al hacer clic en el número de pedido en el panel del almacén y al abrir el pedido en [procesamiento de pedidos de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Al ver el pedido [!DNL Commerce], el número de pedido Amazon aparece en la sección *[!UICONTROL Payment & Shipping Method]*. También incluye opciones para *[!UICONTROL View or Cancel Amazon Order]*y *[!UICONTROL View all Amazon Orders]*, según el estado de envío del pedido.

Ver [cancelar un pedido no enviado](./cancel-unshipped-order.md).

![Información de pedido Amazon en el pedido Commerce](assets/amazon-order-number-payment-info.png){width="500"}

Al procesar un pedido de Amazon, el canal de ventas de Amazon actualiza y sincroniza la información del pedido con su cuenta de [!DNL Amazon Seller Central]. La configuración de cron determina la frecuencia con la que se sincroniza la información de pedidos entre Amazon y el canal de ventas de Amazon.

Las tareas comunes de procesamiento de pedidos [de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) incluyen:

- [Acciones de pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Búsqueda de pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Procesar un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Ver un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Procesar un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Información de pedido y cuenta](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Información de dirección](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Método de pago y envío](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Revisar elementos pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Emitir un crédito/reembolso](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Cumplir/enviar un pedido](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Crear una factura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Cancelar un pedido no enviado](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si un pedido está en estado `Unshipped`, puede [cancelar un pedido de Amazon](./cancel-unshipped-order.md) en la página [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Si se ha enviado un pedido, no se puede cancelar.

Consulte [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
