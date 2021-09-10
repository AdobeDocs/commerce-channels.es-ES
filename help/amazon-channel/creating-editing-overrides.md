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

La acción _[!UICONTROL Create Override]_está disponible al ver anuncios en las pestañas_[!UICONTROL Inactive]_, _[!UICONTROL Active]_y_[!UICONTROL Ineligible]_.

1. Ver un listado en una página _[!UICONTROL Products Listings]_(pestaña_[!UICONTROL Inactive]_, _[!UICONTROL Active]_y_[!UICONTROL Ineligible]_).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Create Override]**para abrir la página Sustituciones de lista de productos .

   ![crear anulación de listado de Amazon](assets/amazon-select-create-override.png)

1. Para asegurarse de que está viendo el listado correcto, verifique el _[!UICONTROL Listing Details]_.

1. Determine el tipo de anulación que está creando.

   Puede definir un solo tipo de anulación o cualquier combinación de tipos para el anuncio (Precio, Tiempo de manipulación, Condición, Notas del Vendedor).

   - **Precio** : haga clic en  **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para  **[!UICONTROL Price Override]**.
   - **Tiempo de gestión** : haga clic en  **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para  **[!UICONTROL Handling Time Override]**.
   - **Condición** : haga clic en  **[!UICONTROL Change Condition]** y elija la opción correcta para la  **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** : haga clic en  **[!UICONTROL Change Seller Notes]** e introduzca el texto de sus notas para  **[!UICONTROL Seller Notes Override]**.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   Se cierra la página _[!UICONTROL Product Listing Overrides]_. El estado de la lista cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). El listado también se agrega a la pestaña_[!UICONTROL Overrides]_.

El siguiente ejemplo muestra una anulación que define un nuevo precio de `$55`, un nuevo tiempo de manipulación de `1 day`, una nueva condición de `Used; Like New` y un nuevo texto de Nota del vendedor.

![Ejemplo de anulación de listado de Amazon](assets/amazon-overrides-edit.png)

## Editar o quitar una anulación de una única lista {#edit-override-single-listing}

La acción _[!UICONTROL Edit Overrides]_está disponible cuando se visualizan anuncios en la pestaña_[!UICONTROL Overrides]_.

1. Ver un listado en la página _[!UICONTROL Product Listings]_(pestaña_[!UICONTROL Overrides]_ ).

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   Se abre la página _[!UICONTROL Product Listing Overrides]_.

   ![Seleccione una anulación de listado de Amazon](assets/amazon-select-edit-overrides.png)

1. Para asegurarse de que está anulando el listado correcto, verifique el _[!UICONTROL Listing Details]_.

1. Para editar la configuración de _[!UICONTROL Override]_, defina las secciones del tipo que desea cambiar (Precio, Tiempo de manipulación, Condición, Notas del vendedor).

   Para mantener el mismo tipo de anulación, seleccione `No Change To <override type>` (valor predeterminado). Esta configuración mantiene sin cambios el valor de anulación definido anteriormente.

   - **Precio** : haga clic en  **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para  **[!UICONTROL Price Override]**.
   - **Tiempo de gestión** : haga clic en  **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para  **[!UICONTROL Handling Time Override]**.
   - **Condición** : haga clic en  **[!UICONTROL Change Condition]** y elija la opción correcta para  **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** : haga clic en  **[!UICONTROL Change Seller Notes]** e introduzca el texto de sus notas para  **[!UICONTROL Seller Notes Override]**.

1. Para quitar un tipo de anulación, haga clic en **Quitar** para cada uno de los tipos que desee eliminar. Si no se elimina, el valor definido anteriormente permanece en la anulación.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   Se cierra la página _[!UICONTROL Product Listing Overrides]_. El estado de la lista cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). Si aún no aparece en la lista, los listados también se añaden a la pestaña_[!UICONTROL Overrides]_.

Copias de seguridad en el ejemplo _Create an Override_. En el siguiente ejemplo se muestra una edición de la anulación creada anteriormente que define un nuevo precio de `$50`, elimina la anulación del tiempo de manipulación y mantiene las anulaciones anteriores de Condición y Notas del vendedor.

![Edición o eliminación de una anulación](assets/amazon-overrides-edit-2.png)
__

## Editar o eliminar una anulación de varios anuncios {#edit-override-multiple-listings}

La acción _[!UICONTROL Edit Listing Overrides]_está disponible en las pestañas_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ y _[!UICONTROL Ineligible]_.

>[!NOTE]
>
>Como está modificando las anulaciones de varios listados, la sección _[!UICONTROL Listing Details]_no se muestra tal cual al modificar un solo listado.

1. Ver el listado en una página _[!UICONTROL Products Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ y _[!UICONTROL Ineligible]_pestaña).

1. Seleccione la casilla de verificación en la columna de la izquierda para cada una de las listas que desee modificar.

1. En _[!UICONTROL Actions]_, haga clic en **[!UICONTROL Edit Listing Overrides]**.

   Se abre la página _[!UICONTROL Product Listing Overrides]_.

   ![Seleccione una anulación de listado de Amazon](assets/amazon-actions-edit-listing-overrides.png)

1. Para editar la configuración de _[!UICONTROL Override]_, defina las secciones del tipo que desea cambiar (Precio, Tiempo de manipulación, Condición, Notas del vendedor).

   Para mantener una anulación igual, seleccione `No Change To <override type>` (predeterminado). Esta configuración mantiene sin cambios el valor de anulación definido anteriormente.

   - **Precio** : haga clic en  **[!UICONTROL Change Listing Price]** e introduzca el valor de precio definido para  **[!UICONTROL Price Override]**.
   - **Tiempo de gestión** : haga clic en  **[!UICONTROL Change Handling Time]** e introduzca el valor de tiempo definido (en días) para  **[!UICONTROL Handling Time Override]**.
   - **Condición** : haga clic en  **[!UICONTROL Change Condition]** y elija la opción correcta para  **[!UICONTROL Condition Override]**.
   - **Notas del vendedor** : haga clic en  **[!UICONTROL Change Seller Notes]** e introduzca el texto de sus notas para  **[!UICONTROL Seller Notes Override]**.

1. Para quitar un tipo de anulación, haga clic en **[!UICONTROL Remove]** para cada uno de los tipos que desee eliminar. Si no se elimina, el valor definido anteriormente permanece en la anulación.

1. Haga clic en **[!UICONTROL Save Listing Override]**.

   Se cierra la página _[!UICONTROL Product Listing Overrides]_. El estado de las listas cambia a `Relist in Progress`. El cambio se publicará en Amazon con la siguiente sincronización de datos (según lo configurado en la configuración de cron). Si aún no aparece en la lista, los listados también se añaden a la pestaña_[!UICONTROL Overrides]_.

### Anular tipos

| Sobrescribir | Descripción |
|--- |--- |
| [!UICONTROL Price Override] | Una anulación de precio define el precio de los anuncios. Esta anulación tiene prioridad sobre toda la configuración automatizada hasta que se elimina la anulación.<br><br>Para anular el precio del producto, seleccione  **[!UICONTROL Change Listing Price]** e introduzca el nuevo precio de  **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Una anulación del tiempo de manipulación define el tiempo (en días) que se tarda en procesar y enviar los productos. Una anulación del tiempo de administración tiene prioridad sobre todas las configuraciones de tiempo de administración automatizadas y predeterminadas hasta que se elimina la anulación.<br><br>El valor que existe en el  _[!UICONTROL Handling Time Override]_cuadro es el tiempo de gestión predeterminado definido en la configuración de  [listado o el tiempo de gestión de invalidación definido ](./listing-settings.md) . Si elimina una anulación del tiempo de gestión, el listado usará de forma predeterminada el tiempo de administración definido en la configuración de listado.<br><br>Para definir una anulación del tiempo de gestión, seleccione **[!UICONTROL Change Handling Time]**e introduzca el nuevo tiempo de gestión (en días) para **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Para anular la condición de lista, elija **[!UICONTROL Change Condition]** y elija la nueva condición en **Sustitución de condición**. |
| [!UICONTROL Seller Notes Override] | Para los productos del catálogo que se definen con una condición distinta a `New`, se puede añadir una nota de vendedor para detallar más el producto y su condición a los compradores potenciales. Puede introducir una anulación de nota del vendedor para un producto de condición `New`, pero Amazon no muestra la nota.<br><br>Para anular las Notas del Vendedor, seleccione  **[!UICONTROL Change Seller Notes]** e introduzca la nueva nota para  **[!UICONTROL Seller Notes Override]**. |
