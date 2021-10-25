---
title: Crear y editar anulaciones
description: Utilice las anulaciones de Sales Channel de Amazon para aplicar los cambios a un solo anuncio de Amazon o a varios anuncios.
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# Creación y edición de anulaciones

Puede crear y anular un listado, editar o quitar una anulación aplicada a un listado. Las anulaciones establecen un valor definido para una lista específica.

## Crear una anulación para un solo listado

La variable _[!UICONTROL Create Override]_la acción está disponible al ver anuncios en la_[!UICONTROL Inactive]_, _[!UICONTROL Active]_y_[!UICONTROL Ineligible]_ pestañas.

1. Ver un listado en un _[!UICONTROL Products Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_y_[!UICONTROL Ineligible]_ ).

1. En el _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Create Override]**para abrir la página Omisiones de lista de productos .

   ![crear anulación de listado de Amazon](assets/amazon-select-create-override.png)

1. Para asegurarse de que está viendo la lista correcta, verifique la variable _[!UICONTROL Listing Details]_.

1. Determine el tipo de anulación que está creando.

   Puede definir un solo tipo de anulación o cualquier combinación de tipos para el anuncio (Precio, Tiempo de manipulación, Condición, Notas del Vendedor).

   - **Precio** - Haga clic en **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para **[!UICONTROL Price Override]**.
   - **Tiempo de administración** - Haga clic en **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para **[!UICONTROL Handling Time Override]**.
   - **Condición** - Haga clic en **[!UICONTROL Change Condition]** y elija la opción correcta para la variable **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** - Haga clic en **[!UICONTROL Change Seller Notes]** e introduzca el texto de las notas para **[!UICONTROL Seller Notes Override]**.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   La variable _[!UICONTROL Product Listing Overrides]_se cerrará. El estado de la lista cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). El listado también se agrega al_[!UICONTROL Overrides]_ pestaña .

El siguiente ejemplo muestra una anulación que define un nuevo precio de `$55`, un nuevo tiempo de manipulación de `1 day`, una nueva condición de `Used; Like New`, y el nuevo texto de Nota del vendedor.

![Ejemplo de anulación de listado de Amazon](assets/amazon-overrides-edit.png)

## Editar o quitar una anulación de una única lista {#edit-override-single-listing}

La variable _[!UICONTROL Edit Overrides]_la acción está disponible al ver anuncios en la_[!UICONTROL Overrides]_ pestaña .

1. Ver un listado en la _[!UICONTROL Product Listings]_página (_[!UICONTROL Overrides]_ ).

1. En el _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   La variable _[!UICONTROL Product Listing Overrides]_se abre.

   ![Seleccione una anulación de listado de Amazon](assets/amazon-select-edit-overrides.png)

1. Para asegurarse de que está anulando el listado correcto, verifique la variable _[!UICONTROL Listing Details]_.

1. Para editar _[!UICONTROL Override]_, defina las secciones del tipo que desea cambiar (Precio, Tiempo de manipulación, Condición, Notas del vendedor).

   Para mantener el mismo tipo de anulación, seleccione `No Change To <override type>` (predeterminado). Esta configuración mantiene sin cambios el valor de anulación definido anteriormente.

   - **Precio** - Haga clic en **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para **[!UICONTROL Price Override]**.
   - **Tiempo de administración** - Haga clic en **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para **[!UICONTROL Handling Time Override]**.
   - **Condición** - Haga clic en **[!UICONTROL Change Condition]** y elija la opción correcta para **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** - Haga clic en **[!UICONTROL Change Seller Notes]** e introduzca el texto de las notas para **[!UICONTROL Seller Notes Override]**.

1. Para quitar un tipo de anulación, haga clic en **Eliminar** para cada uno de los tipos que desea eliminar. Si no se elimina, el valor definido anteriormente permanece en la anulación.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   La variable _[!UICONTROL Product Listing Overrides]_se cerrará. El estado de la lista cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). Si aún no aparece en la lista, los anuncios también se agregan al_[!UICONTROL Overrides]_ pestaña .

Piggyback en _Crear una anulación_ ejemplo. El siguiente ejemplo muestra una edición de la anulación creada anteriormente que define un nuevo precio de `$50`, elimina la anulación del Tiempo de manipulación y mantiene las anulaciones anteriores de Condición y Notas del vendedor.

![Edición o eliminación de una anulación](assets/amazon-overrides-edit-2.png)
__

## Editar o eliminar una anulación de varios anuncios {#edit-override-multiple-listings}

La variable _[!UICONTROL Edit Listing Overrides]_está disponible en la_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ y _[!UICONTROL Ineligible]_pestañas.

>[!NOTE]
>
>Como está modificando las anulaciones de varios listados, la variable _[!UICONTROL Listing Details]_no se muestra como cuando se modifica una lista única.

1. Ver el listado en un _[!UICONTROL Products Listings]_página (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ y _[!UICONTROL Ineligible]_).

1. Seleccione la casilla de verificación en la columna de la izquierda para cada una de las listas que desee modificar.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Edit Listing Overrides]**.

   La variable _[!UICONTROL Product Listing Overrides]_se abre.

   ![Seleccione una anulación de listado de Amazon](assets/amazon-actions-edit-listing-overrides.png)

1. Para editar _[!UICONTROL Override]_, defina las secciones del tipo que desea cambiar (Precio, Tiempo de manipulación, Condición, Notas del vendedor).

   Para mantener una anulación igual, seleccione `No Change To <override type>` (predeterminado). Esta configuración mantiene sin cambios el valor de anulación definido anteriormente.

   - **Precio** - Haga clic en **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para **[!UICONTROL Price Override]**.
   - **Tiempo de administración** - Haga clic en **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para **[!UICONTROL Handling Time Override]**.
   - **Condición** - Haga clic en **[!UICONTROL Change Condition]** y elija la opción correcta para **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** - Haga clic en **[!UICONTROL Change Seller Notes]** e introduzca el texto de las notas para **[!UICONTROL Seller Notes Override]**.

1. Para quitar un tipo de anulación, haga clic en **[!UICONTROL Remove]** para cada uno de los tipos que desea eliminar. Si no se elimina, el valor definido anteriormente permanece en la anulación.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   La variable _[!UICONTROL Product Listing Overrides]_se cerrará. El estado de los anuncios cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). Si aún no aparece en la lista, los anuncios también se agregan al_[!UICONTROL Overrides]_ pestaña .

### Anular tipos

| Sobrescribir | Descripción |
|--- |--- |
| [!UICONTROL Price Override] | Una anulación de precio define el precio de los anuncios. Esta anulación tiene prioridad sobre toda la configuración automatizada hasta que se elimina la anulación.<br><br>Para anular el precio del producto, elija **[!UICONTROL Change Listing Price]** e introduzca el nuevo precio para **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Una anulación del tiempo de manipulación define el tiempo (en días) que se tarda en procesar y enviar los productos. Una anulación del tiempo de administración tiene prioridad sobre todas las configuraciones de tiempo de administración automatizadas y predeterminadas hasta que se elimina la anulación.<br><br>El valor que existe en la variable _[!UICONTROL Handling Time Override]_es el tiempo de administración predeterminado definido en su [configuración de listado](./listing-settings.md) o el tiempo de administración de invalidación definido. Si elimina una anulación del tiempo de gestión, el listado usará de forma predeterminada el tiempo de administración definido en la configuración de listado.<br><br>Para definir una anulación del tiempo de gestión, elija **[!UICONTROL Change Handling Time]**e introduzca el nuevo tiempo de manipulación (en días) para **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Para anular la condición de listado, elija **[!UICONTROL Change Condition]** y seleccione la nueva condición de **Anulación de condición**. |
| [!UICONTROL Seller Notes Override] | Para los productos del catálogo que se definen con una condición distinta a `New`, se puede añadir una nota de vendedor para detallar más el producto y su condición a los compradores potenciales. Puede introducir una anulación de nota de vendedor para un `New` pero Amazon no muestra la nota.<br><br>Para anular las Notas del vendedor, elija **[!UICONTROL Change Seller Notes]** e introduzca la nueva nota para **[!UICONTROL Seller Notes Override]**. |
