---
title: Configuración de tienda predeterminada para los anuncios de Amazon
description: Modifique la configuración predeterminada de Commerce para personalizar la Sales Channel de Amazon para su tienda.
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Configuración de tienda predeterminada para los anuncios de Amazon

Una vez que la tienda esté conectada y hayas configurado la primera regla de anuncio, se iniciará la sincronización de datos entre Amazon y [!DNL Commerce]. Existen varios tipos de configuraciones de tienda que le permiten personalizar su tienda según sus necesidades. Se tiene acceso a la configuración de la tienda en el [tablero](./amazon-store-dashboard.md) de la tienda.

La configuración de tienda incluye:

- [**[!UICONTROL Listing settings]**](./listing-settings.md): controla cómo interactúa el catálogo de productos con [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controlar cómo se administran los pedidos de Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md): defina qué productos del catálogo pueden aparecer en la lista de Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md): define cómo se modifica el precio de lista de Amazon para los anuncios aptos.

- **[!UICONTROL Store reports]** - [Análisis de precios competitivo](./competitive-price-analysis.md) y [mejoras en el anuncio](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Cambios de lista](./listing-changes-log.md) y [errores de comunicación](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md): revise la configuración del correo electrónico y el nombre del almacén del canal de ventas de Amazon en el administrador de [!DNL Commerce].

## Algunos ajustes predeterminados importantes

| Configuración | Predeterminado | Descripción | Ubicación |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crea los [!DNL Commerce] pedidos correspondientes cuando se reciben nuevos pedidos desde Amazon, lo que permite administrar los pedidos en el flujo de trabajo [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Cuando `Disabled`, los pedidos de Amazon importan información de pedidos para su revisión, pero los pedidos deben administrarse en su cuenta de [!DNL Amazon Seller Central]. | [Configuración de pedido](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Los datos de clientes de los pedidos de Amazon no se importan en la base de datos [!DNL Commerce]. Los pedidos Amazon importados se procesan como un cierre de compra de invitado. Si desea crear su base de datos de clientes de [!DNL Commerce], debe cambiar esta configuración a `Build New Customer Account`. | [Configuración de pedido](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] productos de catálogo (que cumplen los requisitos de elegibilidad de Amazon) para publicarlos automáticamente en Amazon y crear anuncios de Amazon. Si desea revisar y publicar manualmente sus productos, debe cambiar esta configuración a `Do Not Automatically List Eligible Products`. Los productos que esperan una publicación manual aparecen en la ficha [_Listo para publicar_](./ready-to-list.md). | [Acciones de lista de productos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define el atributo de origen de precio que se usa como base para los anuncios de Amazon. Si no desea usar el atributo [!DNL Commerce] `Price` como precio base en el que se basan las reglas de precios, debe cambiar esta configuración a un atributo diferente. | [Precio de anuncio](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | El comerciante cumple todas las órdenes. Si utiliza Satisfacción de Pedidos por Amazon o utiliza una combinación de métodos de satisfacción de pedidos, debe cambiar esta configuración. | [Satisfecho por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si todos los productos tienen la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos. Si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Reacondicionado), debe cambiar esta configuración a `Assign Condition Using Product Attribute` y asignar los atributos de condición [!DNL Commerce] a las condiciones del listado de Amazon. | [Condición de lista de productos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ninguno | Defina las reglas utilizadas para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas ofrecen muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como listados. | [Reglas de anuncio](./listing-rules.md) |
| Reglas de precios | ninguno | Defina un atributo de precio de anuncio de Amazon distinto del _[!UICONTROL Magento Price Source]_definido en el [precio de anuncio](./listing-price.md). Para ajustar el precio del anuncio (al alza o a la baja) según la configuración de_[!UICONTROL Magento Price Source]_, cree reglas. | [Reglas de precios](./pricing-products.md) |

Para obtener más información, consulte [Configuración de tienda](./ob-store-review.md).
