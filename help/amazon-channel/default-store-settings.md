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

Una vez que la tienda esté conectada y haya configurado la primera regla de listado, la sincronización de datos entre Amazon y [!DNL Commerce] comienza. Existen varios tipos de configuración de tienda que le permiten personalizar su tienda según sus necesidades. Se puede acceder a la configuración de la tienda en la tienda [tablero](./amazon-store-dashboard.md).

La configuración de la tienda incluye:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controle cómo interactúa su catálogo de productos con la variable [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) : Controle cómo se administran los pedidos de Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Defina qué productos de catálogo pueden incluirse en la lista de Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Defina cómo se altera el precio de la lista de Amazon para los anuncios cualificados.

- **[!UICONTROL Store reports]** - [Análisis de precios competitivo](./competitive-price-analysis.md) y [mejoras en la lista](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Cambios en la lista](./listing-changes-log.md) y [errores de comunicación](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise la configuración del nombre del almacén de canales de ventas de Amazon y de correo electrónico en [!DNL Commerce] Administrador.

## Algunos ajustes predeterminados importantes

| Configuración | Predeterminado | Descripción | Ubicación |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crea correspondiente [!DNL Commerce] pedidos cuando se reciben nuevos pedidos de Amazon, lo que permite administrar los pedidos en la variable [[!DNL Commerce] Pedidos](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} flujo de trabajo. When `Disabled`, Amazon solicita información de pedidos de importación para su revisión, pero los pedidos deben administrarse en su [!DNL Amazon Seller Central] cuenta. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Los datos de clientes de pedidos de Amazon no se importan en su [!DNL Commerce] base de datos. Los pedidos de Amazon importados se procesan como un cierre de compra de invitado. Si desea crear su [!DNL Commerce] base de datos de clientes, debe cambiar esta configuración a `Build New Customer Account`. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] catálogo de productos (que cumplen los requisitos de elegibilidad de Amazon) para publicar automáticamente en Amazon y crear listas de Amazon. Si desea revisar y publicar manualmente sus productos, debe cambiar esta configuración a `Do Not Automatically List Eligible Products`. Los productos que esperan la publicación manual aparecen en la página [_Listo para la lista_](./ready-to-list.md) pestaña . | [Acciones de lista de productos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define el atributo de origen de precio que se usa como base para los anuncios de Amazon. Si no desea usar la variable [!DNL Commerce] `Price` como el precio base en el que se basan sus reglas de precios, debe cambiar esta configuración a un atributo diferente. | [Precio de anuncio](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | El comerciante cumple todos los pedidos. Si utiliza el cumplimiento por parte de Amazon o una combinación de métodos de cumplimiento, debe cambiar esta configuración. | [Cumplimentado por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si todos los productos están en la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos. Si el catálogo contiene productos en diferentes condiciones (como Nuevo, Utilizado y Renovado), debe cambiar esta configuración a `Assign Condition Using Product Attribute` y asigne su [!DNL Commerce] atributos de condición a las condiciones de listado de Amazon. | [Condición de lista de productos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ninguno | Defina las reglas que se utilizarán para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas proporcionan muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como anuncios. | [Reglas de lista](./listing-rules.md) |
| Reglas de precios | ninguno | Defina su atributo de precio de anuncio de Amazon diferente del definido _[!UICONTROL Magento Price Source]_en su [Precio de anuncio](./listing-price.md). Para ajustar el precio de tu anuncio (arriba o abajo) contra tu_[!UICONTROL Magento Price Source]_ , cree reglas. | [Reglas de precios](./pricing-products.md) |

Para obtener más información, consulte [Configuración de almacén](./ob-store-review.md).
