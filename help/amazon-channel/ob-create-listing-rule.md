---
title: '''Incorporación: Crear regla de listado'''
description: Al completar el proceso de incorporación del canal de ventas de Amazon, cree las reglas de listado iniciales para generar anuncios de Amazon para sus productos [!DNL Commerce] .
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Incorporación: Crear regla de listado

Las reglas de listado se pueden definir durante la incorporación, pero también se pueden modificar en cualquier momento. Después de la incorporación, puede acceder a las [reglas de listado](./listing-rules.md) en el [tablero](./amazon-store-dashboard.md) de la tienda.

## Crear una regla de anuncio durante la incorporación

1. Una vez que la tienda esté conectada, haga clic en **[!UICONTROL View Store]** para la tienda agregada.

   El [panel](./amazon-store-dashboard.md) del almacén aparece con el mensaje `No products listed to Amazon`.

1. Haga clic en **[!UICONTROL Preview and List Eligible Products]**.

   Aparece la página _[!UICONTROL Listing Rules]_.

1. Defina las condiciones que desee para la idoneidad de los productos que se enumerarán en Amazon y haga clic en **[!UICONTROL Preview changes]** o haga clic en **[!UICONTROL Preview changes]** para omitir este paso.

   Consulte [Ejemplo: Defina una condición](./ob-define-condition-example.md).

1. Revise sus anuncios en la Vista previa del anuncio:

   ![Vista previa del anuncio](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Los productos que aparecen en esta ficha no pueden incluirse en la lista de Amazon según la configuración actual de la regla de la lista.

      Los productos no aptos no se publican en Amazon. Si un producto no apto ya aparece en la lista de Amazon y usted relaciona la lista de Amazon con su producto de catálogo [!DNL Commerce], la cantidad de la lista de Amazon cambia a `0` para evitar ventas del producto. Para eliminar manualmente una lista de Amazon, consulte [Finalización de una lista de Amazon](./end-listings-manually.md). Los productos que no cumplen los requisitos de Amazon no se enumeran aquí. Estos productos se enumeran en la pestaña [[!UICONTROL Inactive Listings]](./inactive-listings.md).

      Para cambiar un listado `Ineligible` a un listado `Eligible`, repita este proceso y modifique las reglas del listado.

   - **[!UICONTROL Eligible Listings]** - Los productos que aparecen en esta ficha pueden incluirse en la lista de Amazon en función de la configuración actual de las reglas de la lista, y cumplen los requisitos de Amazon. Esta pestaña incluye las listas de Amazon existentes que se importan (si tiene **[!UICONTROL Import Third Party Listings]** configurado como `Import Listing` en la [Configuración de listas](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Los productos que se enumeran en esta ficha incluyen los productos de  [!DNL Commerce] catálogo que recientemente cumplen los requisitos para la lista de Amazon, según la configuración actual de la regla de la lista, y crean anuncios de Amazon.

1. Cuando termine, haga clic en **[!UICONTROL Save and Close]**.

   Se abre el [tablero](./amazon-store-dashboard.md) de la tienda.

Una vez completada la incorporación de una tienda, se inicia la sincronización de información entre [!DNL Commerce] y Amazon. Los listados de Amazon se importan en [!DNL Commerce] e intentan coincidir con los productos de su catálogo [!DNL Commerce].

Puede ver la información de sus pedidos de Amazon en la sección _[!UICONTROL Recent Orders]_del panel de la tienda. Consulte [Tablero de almacenamiento](./amazon-store-dashboard.md) o [Administrar pedidos](./managing-orders.md).

>[!IMPORTANT]
>
>Hay algunas configuraciones de tienda importantes (anuncios, precios, reglas, cumplimiento, etc.) que tienen valores predeterminados para una nueva tienda. Para asegurarse de que la tienda está configurada para sus necesidades específicas, revise la [configuración de la tienda](./default-store-settings.md) .

![Icono siguiente](assets/btn-next.png) [**Continuar a la configuración de almacenamiento predeterminada**](./default-store-settings.md)
