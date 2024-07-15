---
title: 'Canal de ventas de Amazon: [!UICONTROL Overrides]'
description: La Sales Channel de Amazon proporciona la pestaña Anulaciones para ayudarle a identificar y administrar cómo aplica las anulaciones en los anuncios de Amazon.
feature: Sales Channels, Price Rules
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---

# [!UICONTROL Overrides]

La pestaña _[!UICONTROL Overrides]_muestra los anuncios de Amazon a los que ha aplicado una anulación. Una anulación es una configuración específica de un listado que se puede utilizar para establecer un valor definido en un listado. La anulación aplicada a un anuncio define su configuración, independientemente de la configuración o las reglas definidas para las que sea apto. Cuando se aplica una anulación a un listado, este aparece en la ficha_[!UICONTROL Overrides]_. El valor definido en la anulación aparece en la columna correspondiente al listado. Se pueden aplicar cuatro tipos de invalidaciones: precio, tiempo de manipulación, condición y notas del vendedor.

## Tipos de invalidaciones

| Tipo | Descripción |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Precio | Anulación que establece el precio del anuncio e ignora cualquier otra configuración de precio del anuncio. <br><br>**Ejemplo**: ha definido una regla de precio de descuento del 20% que se aplica a todos los productos de una categoría específica del catálogo. Tiene un producto nuevo en el mercado y la demanda es alta, por lo que no desea que se aplique el precio con descuento al anuncio aunque el producto esté en esa categoría. Puede seleccionar el anuncio, [crear una anulación de precio](./creating-editing-overrides.md#edit-override-single-listing) y definir el precio del anuncio en una anulación de precio. |
| Tiempo de manipulación | Omisión que define el tiempo de manipulación de un anuncio e ignora el tiempo de gestión predeterminado establecido en la configuración del anuncio.<br><br>**Ejemplo**: el tiempo de manipulación predeterminado de tus anuncios es de dos días. Usted tiene un producto que es frágil y requiere un día extra para garantizar su embalaje especial para el envío. Puedes ver el anuncio, [crear un reemplazo de tiempo de manipulación](./creating-editing-overrides.md#edit-override-single-listing) y definir el tiempo de manipulación en tres días.<br><br>**Nota:** No disponible para los productos establecidos en `Fulfilled by Amazon`. |
| Condición | Anulación que establece el valor de condición de un listado, independientemente del atributo de condición asignado al listado.<br><br>**Ejemplo**: la mayoría de los productos del catálogo son nuevos, pero tiene un producto que se encuentra en estado Reacondicionado. Puede ver el listado, [crear una invalidación de condición](./creating-editing-overrides.md#edit-override-single-listing) y definir la condición restaurada para el listado.<br><br>**Nota:** No disponible para los productos establecidos en `Fulfilled by Amazon`. |
| Notas del vendedor | Una anulación que define la sección _Notas del vendedor_ del anuncio. Este campo se puede utilizar para añadir información adicional relacionada con el producto o la anulación aplicada, utilizada generalmente para describir la condición de productos &quot;no nuevos&quot;. El texto de este campo aparece con el listado del comprador. No se pueden agregar notas de vendedor a un anuncio con un valor de condición de `New`. <br><br>**Ejemplo**: Tiene un producto que está en la condición `Refurbished`. Normalmente, los productos en esta condición no incluyen manuales ni documentos, pero tiene un proveedor diferente para este producto que incluye un manual. Puedes ver el anuncio, [crear una anulación de notas de vendedor](./creating-editing-overrides.md#edit-override-single-listing) y añadir una nota de texto que sea única en este anuncio sobre el manual para que el comprador sepa que está incluido.<br><br>**Nota**: si un producto tiene una condición definida de `New`, puede escribir una anulación de las notas de vendedor, pero Amazon no muestra las notas de vendedor de un producto de `New`. |

Puede crear, editar o quitar una invalidación de [listado único](./creating-editing-overrides.md#edit-override-single-listing). En las fichas _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ y _[!UICONTROL Ineligible]_, puede hacer clic en **[!UICONTROL Select]**en la columna_[!UICONTROL Action]_ y elegir **[!UICONTROL Create Override]**. La acción _[!UICONTROL Edit Overrides]_solo está disponible cuando un anuncio tiene una anulación aplicada y se ve en la ficha_[!UICONTROL Overrides]_.

También puedes crear, editar o quitar una invalidación de [varios anuncios](./creating-editing-overrides.md#edit-override-multiple-listings). En las fichas _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ y _[!UICONTROL Ineligible]_, puede hacer clic en **[!UICONTROL Select]**en la columna_[!UICONTROL Action]_ y elegir **[!UICONTROL Edit Listing Overrides]**.

Al eliminar una anulación, se indica al anuncio que utilice los valores definidos por la configuración y las reglas del anuncio.

Al definir una sustitución, también puede introducir un único tipo de sustitución o cualquier combinación de los tipos.

Ver [Crear y editar invalidaciones](./creating-editing-overrides.md).

>[!NOTE]
>
>Si tiene listados en proceso, el número de listados se muestra en un mensaje encima de las pestañas.

![Pestaña Invalidaciones](assets/amazon-overrides.png){width="600" zoomable="yes"}

las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | El SKU (código de referencia) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa los números de identificación estándar de Amazon. Un ASIN es un bloque único de 10 letras y/o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar artículos ASIN en la página de detalles del producto de Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Condition Override] | La nueva condición definida en la anulación. Si la anulación aplicada al listado no es una anulación de condición, `Not Selected` aparece en esta columna. |
| [!UICONTROL Product Listing Name] | El nombre del producto. |
| [!UICONTROL Seller Notes Override] | Las nuevas notas del vendedor definidas en la anulación. Si la anulación aplicada al listado no es de este tipo, esta columna está en blanco. |
| [!UICONTROL Handling Override] | El nuevo tiempo de manipulación definido en la anulación (en días). Si la anulación aplicada al listado no es una anulación de tiempo de manipulación, esta columna está en blanco. |
| [!UICONTROL List Price Override] | El nuevo precio de anuncio definido en la anulación. Si la anulación aplicada al listado no es una anulación de precio, `N/A` aparece en esta columna. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a un listado específico. Para aplicar una acción, en la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**y elija una opción:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
