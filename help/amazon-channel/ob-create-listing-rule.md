---
title: Crear una regla de listado de Amazon
description: Al completar el proceso de incorporación al canal de ventas de Amazon, crea las reglas de listado iniciales para generar listados de Amazon para tus [!DNL Commerce] productos.
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Crear una regla de listado de Amazon

Las reglas de listado se pueden definir durante la incorporación, pero también se pueden modificar en cualquier momento. Después de la incorporación, puedes acceder a las [reglas de listado](./listing-rules.md) en el [panel](./amazon-store-dashboard.md) de la tienda.

## Crear una regla de anuncio durante la incorporación

1. Una vez que la tienda esté conectada, haga clic en **[!UICONTROL View Store]** para la tienda agregada.

   Aparece el [tablero](./amazon-store-dashboard.md) de la tienda con el mensaje `No products listed to Amazon`.

1. Haga clic en **[!UICONTROL Preview and List Eligible Products]**.

   Aparecerá la página _[!UICONTROL Listing Rules]_.

1. Defina las condiciones que desee para que los productos que se van a incluir en la lista de Amazon cumplan los requisitos y haga clic en **[!UICONTROL Preview changes]**, o bien haga clic en **[!UICONTROL Preview changes]** para omitir este paso.

   Ver [Ejemplo: Definir una condición](./ob-define-condition-example.md).

1. Revisa tus anuncios en la sección Vista previa del anuncio:

   ![Vista previa del anuncio](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]**: los productos enumerados en esta ficha no cumplen los requisitos para el anuncio de Amazon según la configuración actual de reglas de anuncio.

     Los productos no aptos no se publican en Amazon. Si un producto no apto ya figura en Amazon y el listado de Amazon coincide con el producto del catálogo [!DNL Commerce], la cantidad del listado de Amazon cambia a `0` para evitar las ventas del producto. Para quitar manualmente un listado de Amazon, consulte [Finalizar un listado de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no aparecen aquí. Estos productos se enumeran en la ficha [[!UICONTROL Inactive Listings] ](./inactive-listings.md).

     Para cambiar un listado de `Ineligible` por uno de `Eligible`, repita este proceso y modifique las reglas del listado.

   - **[!UICONTROL Eligible Listings]**: los productos que aparecen en esta pestaña pueden aparecer en el anuncio de Amazon según la configuración actual de reglas del anuncio y cumplen los requisitos de Amazon. Esta pestaña incluye los anuncios existentes de Amazon que se importan (si tienes **[!UICONTROL Import Third Party Listings]** establecido en `Import Listing` en tu [configuración de anuncio](./listing-settings.md)).

   - **[!UICONTROL New Listings]**: los productos que aparecen en esta ficha incluyen los productos del catálogo [!DNL Commerce] que cumplen los requisitos para aparecer en el listado de Amazon según la configuración actual de reglas de listado y crean listados de Amazon.

1. Una vez finalizado, haga clic en **[!UICONTROL Save and Close]**.

   Se abre el [tablero](./amazon-store-dashboard.md) de la tienda.

Una vez completada la incorporación a un almacén, se inicia la sincronización de información entre [!DNL Commerce] y Amazon. Los anuncios de Amazon se han importado a [!DNL Commerce] y se intenta hacer coincidir con los productos del catálogo [!DNL Commerce].

Puede ver la información de pedidos de Amazon en la sección _[!UICONTROL Recent Orders]_del panel de la tienda. Ver [Panel de tienda](./amazon-store-dashboard.md) o [Administrar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Hay algunas configuraciones importantes de la tienda (anuncios, precios, reglas, cumplimiento, etc.) que tienen valores predeterminados para una nueva tienda. Para asegurarte de que tu tienda está configurada para tus necesidades específicas, revisa tu [configuración de la tienda](./default-store-settings.md) .

![Siguiente icono](assets/btn-next.png) [**Continuar con la configuración predeterminada de la tienda**](./default-store-settings.md)
