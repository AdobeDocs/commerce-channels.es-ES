---
title: '''Incorporación: Crear regla de listado'''
description: Al completar el proceso de incorporación del canal de ventas de Amazon, cree las reglas de listado iniciales para generar anuncios de Amazon para su [!DNL Commerce] productos.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Incorporación: Crear regla de listado

Las reglas de listado se pueden definir durante la incorporación, pero también se pueden modificar en cualquier momento. Después de la incorporación, puede acceder a la [listar reglas](./listing-rules.md) en la tienda [tablero](./amazon-store-dashboard.md).

## Crear una regla de anuncio durante la incorporación

1. Una vez que la tienda esté conectada, haga clic en **[!UICONTROL View Store]** para la tienda añadida.

   La tienda [tablero](./amazon-store-dashboard.md) aparece con la variable `No products listed to Amazon` mensaje.

1. Haga clic en **[!UICONTROL Preview and List Eligible Products]**.

   La variable _[!UICONTROL Listing Rules]_se abre.

1. Defina las condiciones que desee para la idoneidad de los productos que se enumerarán en Amazon y haga clic en **[!UICONTROL Preview changes]** o haga clic en **[!UICONTROL Preview changes]** para omitir este paso.

   Consulte [Ejemplo: Definir una condición](./ob-define-condition-example.md).

1. Revise sus anuncios en la Vista previa del anuncio:

   ![Vista previa del anuncio](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Los productos que aparecen en esta ficha no pueden incluirse en la lista de Amazon según la configuración actual de la regla de la lista.

      Los productos no aptos no se publican en Amazon. Si un producto no apto ya aparece en la lista de Amazon y usted coincide con el listado de Amazon en su [!DNL Commerce] producto del catálogo, la cantidad de la lista de Amazon cambia a `0` para evitar ventas del producto. Para eliminar manualmente un listado de Amazon, consulte [Finalización de una lista de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no se enumeran aquí. Estos productos se incluyen en la lista [[!UICONTROL Inactive Listings] ficha](./inactive-listings.md).

      Para cambiar un `Ineligible` listado en un `Eligible` , repita este proceso y modifique las reglas de listado.

   - **[!UICONTROL Eligible Listings]** - Los productos que aparecen en esta ficha pueden incluirse en la lista de Amazon en función de la configuración actual de las reglas de la lista, y cumplen los requisitos de Amazon. Esta ficha incluye los anuncios de Amazon existentes que se importan (si tiene **[!UICONTROL Import Third Party Listings]** configure como `Import Listing` en su [Configuración de lista](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Los productos que aparecen en esta ficha incluyen su [!DNL Commerce] catálogo de productos que recientemente cumplen los requisitos para la lista de Amazon según la configuración actual de la regla de listado y cree anuncios de Amazon.

1. Cuando termine, haga clic en **[!UICONTROL Save and Close]**.

   La tienda [tablero](./amazon-store-dashboard.md) se abre.

Una vez completada la incorporación de una tienda, la sincronización de información entre [!DNL Commerce] y Amazon se ha iniciado. Los anuncios de Amazon se importan en [!DNL Commerce] e intente coincidir con los productos de su [!DNL Commerce] Catálogo.

Puede ver la información de pedidos de Amazon en la _[!UICONTROL Recent Orders]_del panel de almacenamiento. Consulte [Tablero de almacenamiento](./amazon-store-dashboard.md) o [Administrar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Hay algunas configuraciones de tienda importantes (anuncios, precios, reglas, cumplimiento, etc.) que tienen valores predeterminados para una nueva tienda. Para asegurarse de que su tienda está configurada para sus necesidades específicas, revise su [configuración de almacenamiento](./default-store-settings.md) .

![Icono Siguiente](assets/btn-next.png) [**Continuar con la configuración de almacén predeterminada**](./default-store-settings.md)
