---
title: Configuración de tienda predeterminada para los anuncios de Amazon
description: Modifique la configuración predeterminada de Commerce para personalizar la Sales Channel de Amazon para su tienda.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Configuración de tienda predeterminada para los anuncios de Amazon

Una vez que la tienda esté conectada y hayas configurado la primera regla de anuncio, se sincronizan los datos entre Amazon y [!DNL Commerce] comienza. Existen varios tipos de configuraciones de tienda que le permiten personalizar su tienda según sus necesidades. Se accede a la configuración de la tienda en la tienda [tablero](./amazon-store-dashboard.md).

La configuración de tienda incluye:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Controlar la interacción del catálogo de productos con [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Controle cómo se administran los pedidos de Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) : defina qué productos del catálogo pueden aparecer en Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Define cómo se modifica el precio de lista de Amazon para los anuncios aptos.

- **[!UICONTROL Store reports]** - [Análisis de precios competitivos](./competitive-price-analysis.md) y [mejoras de listado](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Cambios de anuncio](./listing-changes-log.md) y [errores de comunicación](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Revise la configuración de correo electrónico y nombre de tienda de canal de ventas de Amazon en la [!DNL Commerce] Administrador.

## Algunos ajustes predeterminados importantes

| Configuración | Predeterminado | Descripción | Ubicación |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crea el correspondiente [!DNL Commerce] pedidos cuando se reciben nuevos pedidos desde Amazon, lo que permite administrar los pedidos en la [[!DNL Commerce] Pedidos](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) flujo de trabajo. Cuándo `Disabled`, los pedidos de Amazon importan información de pedidos para su revisión, pero los pedidos deben gestionarse en su [!DNL Amazon Seller Central] cuenta. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Los datos del cliente de los pedidos de Amazon no se importan en su [!DNL Commerce] base de datos. Los pedidos Amazon importados se procesan como un cierre de compra de invitado. Si desea crear su [!DNL Commerce] base de datos de clientes, debe cambiar esta configuración a `Build New Customer Account`. | [Configuración de pedidos](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] catalogar productos (que cumplan los requisitos de idoneidad de Amazon) para publicarlos automáticamente en Amazon y crear anuncios de Amazon. Si desea revisar y publicar manualmente sus productos, debe cambiar esta configuración a `Do Not Automatically List Eligible Products`. Los productos que esperan una publicación manual aparecen en la [_Listo para la lista_](./ready-to-list.md) pestaña. | [Acciones de lista de productos](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Define el atributo de origen de precio que se usa como base para los anuncios de Amazon. Si no desea utilizar la variable [!DNL Commerce] `Price` como precio base en el que se basan las reglas de asignación de precios, debe cambiar esta configuración a otro atributo. | [Precio del anuncio](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | El comerciante cumple todas las órdenes. Si utiliza Satisfacción de Pedidos por Amazon o utiliza una combinación de métodos de satisfacción de pedidos, debe cambiar esta configuración. | [Cumplido por](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si todos los productos tienen la misma condición, puede seleccionar una de las opciones de condición de Amazon para representar todos los productos. Si el catálogo contiene productos en condiciones diferentes (como Nuevo, Utilizado y Reacondicionado), debe cambiar esta configuración a `Assign Condition Using Product Attribute` y asigne los [!DNL Commerce] atributos de condición de a las condiciones de listado de Amazon. | [Condición de lista de productos](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ninguno | Defina las reglas utilizadas para determinar qué productos publica el canal de ventas de Amazon en Amazon. Estas reglas ofrecen muchas opciones para crear reglas sencillas o complejas para incluir o excluir productos como listados. | [Reglas de listado](./listing-rules.md) |
| Reglas de precios | ninguno | Defina el atributo de precio del listado de Amazon de forma diferente al definido _[!UICONTROL Magento Price Source]_en su [Precio del anuncio](./listing-price.md). Para ajustar el precio del anuncio (al alza o a la baja) según sus_[!UICONTROL Magento Price Source]_ configuración, crear reglas. | [Reglas de precios](./pricing-products.md) |

Para obtener más información, consulte [Configuración de tienda](./ob-store-review.md).
