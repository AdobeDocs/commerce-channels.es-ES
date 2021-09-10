---
title: Configuración predeterminada de la tienda
description: Modifique la configuración de comercio predeterminada para personalizar la Sales Channel de Amazon para su tienda.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Configuración predeterminada de la tienda

Una vez que la tienda esté conectada y haya configurado la primera regla de listado, se iniciará la sincronización de datos entre Amazon y [!DNL Commerce]. Existen varios tipos de configuración de tienda que le permiten personalizar su tienda según sus necesidades. Se accede a la configuración del almacén en el [panel](./amazon-store-dashboard.md) de la tienda.

La configuración de la tienda incluye:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controle cómo interactúa su catálogo de productos con  [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) : Controle cómo se administran los pedidos de Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Defina qué productos de catálogo pueden incluirse en la lista de Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Defina cómo se altera el precio de la lista de Amazon para los anuncios cualificados.

- **[!UICONTROL Store reports]** -  [Análisis de precios ](./competitive-price-analysis.md) competitivos y  [mejoras](./listing-improvements.md) en los listados.

- **[!UICONTROL Logs]** -  [Enumerar ](./listing-changes-log.md) cambios y errores de  [comunicación](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise la configuración del nombre del almacén de canales de ventas de Amazon y de correo electrónico en  [!DNL Commerce] Administración.

## Algunos ajustes predeterminados importantes

| Configuración | Predeterminado | Descripción | Ubicación |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crea los [!DNL Commerce] pedidos correspondientes cuando se reciben nuevos pedidos de Amazon, lo que permite administrar los pedidos en el flujo de trabajo [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}. Cuando `Disabled`, Amazon solicita información de pedidos de importación para su revisión, pero los pedidos deben administrarse en su cuenta [!DNL Amazon Seller Central]. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Los datos del cliente procedentes de pedidos Amazon no se importan en la base de datos [!DNL Commerce]. Los pedidos de Amazon importados se procesan como un cierre de compra de invitado. Si desea crear la base de datos de clientes [!DNL Commerce], debe cambiar esta configuración a `Build New Customer Account`. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] catálogo de productos (que cumplen los requisitos de elegibilidad de Amazon) para publicar automáticamente en Amazon y crear listas de Amazon. Si desea revisar y publicar manualmente sus productos, debe cambiar esta configuración a `Do Not Automatically List Eligible Products`. Los productos que esperan la publicación manual aparecen en la pestaña [_Ready to List_](./ready-to-list.md). | [Acciones de lista de productos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define el atributo de origen de precio que se usa como base para los anuncios de Amazon. Si no desea utilizar el atributo [!DNL Commerce] `Price` como precio base en el que se basan las reglas de precios, debe cambiar esta configuración a un atributo diferente. | [Precio de anuncio](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | El comerciante cumple todos los pedidos. Si utiliza el cumplimiento por parte de Amazon o una combinación de métodos de cumplimiento, debe cambiar esta configuración. | [Cumplimentado por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si todos los productos están en la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos. Si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Restaurado), debe cambiar esta configuración a `Assign Condition Using Product Attribute` y asignar los atributos de condición [!DNL Commerce] a las condiciones de listado de Amazon. | [Condición de lista de productos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ninguno | Defina las reglas que se utilizarán para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas proporcionan muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como anuncios. | [Reglas de lista](./listing-rules.md) |
| Reglas de precios | ninguno | Defina su atributo de precio de anuncio de Amazon diferente del _[!UICONTROL Magento Price Source]_definido en su [Precio de anuncio](./listing-price.md). Para ajustar el precio del anuncio (arriba o abajo) con la configuración_[!UICONTROL Magento Price Source]_, cree reglas. | [Reglas de precios](./pricing-products.md) |

Para obtener más información, consulte [Configuración de almacenamiento](./ob-store-review.md).
