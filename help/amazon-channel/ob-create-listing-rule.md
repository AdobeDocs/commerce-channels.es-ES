---
title: Crear una regla de listado de Amazon
description: Al completar el proceso de incorporación al canal de ventas de Amazon, cree las reglas de anuncio iniciales para generar anuncios de Amazon para su [!DNL Commerce] productos.
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Crear una regla de listado de Amazon

Las reglas de listado se pueden definir durante la incorporación, pero también se pueden modificar en cualquier momento. Después de la incorporación, puede acceder a las [enumerar reglas](./listing-rules.md) en la tienda [tablero](./amazon-store-dashboard.md).

## Crear una regla de anuncio durante la incorporación

1. Una vez conectada la tienda, haga clic en **[!UICONTROL View Store]** para el almacén añadido.

   La tienda [tablero](./amazon-store-dashboard.md) aparece con la variable `No products listed to Amazon` Mensaje.

1. Haga clic **[!UICONTROL Preview and List Eligible Products]**.

   El _[!UICONTROL Listing Rules]_página.

1. Defina las condiciones deseadas para la idoneidad de los productos que se enumerarán en Amazon y haga clic en **[!UICONTROL Preview changes]** o haga clic en **[!UICONTROL Preview changes]** para omitir este paso.

   Consulte [Ejemplo: Definición de una condición](./ob-define-condition-example.md).

1. Revisa tus anuncios en la sección Vista previa del anuncio:

   ![Vista previa del anuncio](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** : los productos que aparecen en esta pestaña no pueden aparecer en el anuncio de Amazon según la configuración actual de las reglas de anuncio.

     Los productos no aptos no se publican en Amazon. Si un producto no apto ya figura en Amazon y usted relaciona el anuncio de Amazon con su [!DNL Commerce] producto del catálogo, la cantidad del listado de Amazon cambia a `0` para evitar la venta del producto. Para eliminar manualmente un anuncio de Amazon, consulte [Finalizar un anuncio de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no aparecen aquí. Estos productos se enumeran en la [[!UICONTROL Inactive Listings] pestaña](./inactive-listings.md).

     Para cambiar un `Ineligible` poner en venta un `Eligible` anuncio, repite este proceso y modifica las reglas del anuncio.

   - **[!UICONTROL Eligible Listings]** : los productos que aparecen en esta pestaña pueden aparecer en el anuncio de Amazon según la configuración actual de reglas del anuncio y cumplen los requisitos de Amazon. Esta pestaña incluye los anuncios existentes de Amazon que se importan (si tiene **[!UICONTROL Import Third Party Listings]** establezca en `Import Listing` en su [Configuración de anuncio](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Los productos que aparecen en esta pestaña incluyen su [!DNL Commerce] productos de catálogo que acaban de ser aptos para el anuncio de Amazon según la configuración actual de reglas de anuncio y crean anuncios de Amazon.

1. Cuando termine, haga clic en **[!UICONTROL Save and Close]**.

   La tienda [tablero](./amazon-store-dashboard.md) abre.

Una vez finalizada la incorporación de una tienda, la información se sincroniza entre [!DNL Commerce] y se inicia Amazon. Los anuncios de Amazon se han importado a [!DNL Commerce] e intenta hacer coincidir con los productos de su [!DNL Commerce] Catálogo.

Puede ver la información de pedidos de Amazon en la _[!UICONTROL Recent Orders]_del tablero de la tienda. Consulte [Tablero de tienda](./amazon-store-dashboard.md) o [Administrar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Hay algunas configuraciones importantes de la tienda (anuncios, precios, reglas, cumplimiento, etc.) que tienen valores predeterminados para una nueva tienda. Para asegurarte de que tu tienda está configurada para tus necesidades específicas, revisa tu [configuración de tienda](./default-store-settings.md) .

![Icono Siguiente](assets/btn-next.png) [**Continuar con la configuración predeterminada de la tienda**](./default-store-settings.md)
