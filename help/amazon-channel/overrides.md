---
title: Anulaciones
description: La Sales Channel de Amazon proporciona la pestaña Sobrescrituras para ayudarle a identificar y administrar cómo está aplicando las anulaciones en sus anuncios de Amazon.
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Anulaciones

La pestaña _[!UICONTROL Overrides]_muestra los listados de Amazon a los que ha aplicado una anulación. Una anulación es una configuración específica de un listado que puede utilizarse para establecer un valor definido en un listado. Una anulación aplicada a un listado define la configuración del listado, independientemente de otras configuraciones de listado definidas o reglas para las que el listado sea elegible. Cuando se aplica una anulación a un listado, el listado aparece en la pestaña_[!UICONTROL Overrides]_. El valor definido en la anulación aparece en la columna correspondiente de la lista. Se pueden aplicar cuatro tipos de anulaciones: Precio, tiempo de manejo, condición y notas del vendedor.

## Tipos de anulaciones

| Tipo | Descripción |
|---|---|
| Precio | Una anulación que establece el precio del anuncio, ignorando todos los demás ajustes de precio del anuncio. <br><br>**Ejemplo**: Ha definido una regla de precio de descuento del 20 % que se aplica a todos los productos de una categoría específica del catálogo. Tiene un producto nuevo en el mercado y la demanda es alta, por lo que no desea que se aplique el precio de descuento a la lista aunque el producto esté en esa categoría. Puede seleccionar el listado, [crear una anulación de precio](./creating-editing-overrides.md#edit-override-single-listing), y definir el precio del anuncio en una anulación de precio. |
| Tiempo de administración | Una anulación que establece el tiempo de administración de una lista, ignorando el tiempo de administración predeterminado establecido en la configuración de la lista.<br><br>**Ejemplo**: El tiempo de administración predeterminado para sus anuncios está establecido en 2 días. Usted tiene un producto que es frágil y requiere un día extra para garantizar su embalaje especial para el envío. Puede ver la lista, [crear una anulación de tiempo de administración](./creating-editing-overrides.md#edit-override-single-listing), y definir el tiempo de administración en tres días.<br><br>**Nota:** No está disponible para productos configurados en  `Fulfilled by Amazon`. |
| Condición | Una anulación que establece el valor de condición de una lista, independientemente del atributo de condición asignado a la lista.<br><br>**Ejemplo**: La mayoría de los productos de su catálogo son New condition, pero usted tiene un producto que está en estado Refaccionado. Puede ver el listado, [crear una anulación de condición](./creating-editing-overrides.md#edit-override-single-listing) y definir la condición renovada para el listado.<br><br>**Nota:** No está disponible para productos configurados en  `Fulfilled by Amazon`. |
| Notas del vendedor | Una anulación que define la sección _Notas del vendedor_ del listado. Este campo se puede utilizar para añadir información adicional relacionada con el producto o con la anulación aplicada, utilizada normalmente para describir la condición de productos &quot;no nuevos&quot;. El texto de este campo aparece con la lista del comprador. Las notas del vendedor no se pueden agregar para un anuncio con un valor de condición `New`. <br><br>**Ejemplo**: Tiene un producto que está en  `Refurbished` condición. Normalmente los productos en esta condición no incluyen manuales ni documentos, pero tiene un proveedor diferente para este producto que incluye un manual. Puede ver el listado, [crear una anulación de notas de vendedor](./creating-editing-overrides.md#edit-override-single-listing), y agregar una nota de texto que sea única para este listado acerca del manual para que el comprador sepa que está incluido.<br><br>**Nota**: Si un producto tiene una condición definida de  `New`, puede introducir una anulación de las notas del vendedor, pero Amazon no muestra las notas del vendedor de un  `New` producto. |

Puede crear, editar o quitar una anulación para una [lista única](./creating-editing-overrides.md#edit-override-single-listing). En las pestañas _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ y _[!UICONTROL Ineligible]_, puede hacer clic **[!UICONTROL Select]**en la columna_[!UICONTROL Action]_ y elegir **[!UICONTROL Create Override]**. La acción _[!UICONTROL Edit Overrides]_solo está disponible cuando se ha aplicado una anulación a un listado y se ve en la pestaña_[!UICONTROL Overrides]_.

También puede crear, editar o eliminar una anulación de [varias listas](./creating-editing-overrides.md#edit-override-multiple-listings). En las pestañas _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ y _[!UICONTROL Ineligible]_, puede hacer clic **[!UICONTROL Select]**en la columna_[!UICONTROL Action]_ y elegir **[!UICONTROL Edit Listing Overrides]**.

Al eliminar una anulación, se indica a la lista que utilice los valores definidos por la configuración y las reglas de la lista.

Al definir una anulación, también puede elegir introducir un único tipo de anulación o cualquier combinación de los tipos.

Consulte [Crear y editar anulaciones](./creating-editing-overrides.md).

>[!NOTE]
>
>Si tiene anuncios en curso, el número de anuncios se muestra en un mensaje encima de las pestañas.

![Pestaña Overrides](assets/amazon-overrides.png)

Las páginas de inicio del canal de ventas de Amazon comparten algunos [controles del espacio de trabajo](./workspace-controls.md) comunes que le permiten personalizar los datos que se muestran.

## Columnas predeterminadas

| Columna | Descripción |
|---|---|
| [!UICONTROL Amazon Seller SKU] | El SKU (unidad de mantenimiento de stock) asignado por Amazon a un producto para identificar el producto, las opciones, el precio y el fabricante. |
| [!UICONTROL ASIN] | Un bloque único de 10 letras o números que identifican elementos.<br><br>ASIN significa los números de identificación estándar de Amazon. Un ASIN es un bloque único de 10 letras o números que identifican elementos. Para los libros, el ASIN es el mismo que el número ISBN, pero para todos los demás productos se crea un nuevo ASIN cuando el artículo se carga en su catálogo. Puede encontrar un artículo ASIN en la página de detalles del producto en Amazon, junto con más detalles relacionados con el artículo. |
| [!UICONTROL Condition Override] | La nueva condición definida en la anulación. Si la anulación aplicada al listado no es una anulación de condición, `Not Selected` aparece en esta columna. |
| [!UICONTROL Product Listing Name] | Nombre del producto. |
| [!UICONTROL Seller Notes Override] | Las nuevas notas del vendedor definidas en la anulación. Si la anulación aplicada al listado no es este tipo de anulación, esta columna está en blanco. |
| [!UICONTROL Handling Override] | El nuevo tiempo de gestión definido en la anulación (en días). Si la anulación aplicada a la lista no anula el tiempo de administración, esta columna está en blanco. |
| [!UICONTROL List Price Override] | El nuevo precio de anuncio definido en la anulación. Si la anulación aplicada al listado no es una anulación de precio, `N/A` aparece en esta columna. |
| [!UICONTROL Action] | Lista de acciones disponibles que se pueden aplicar a una lista específica. Para aplicar una acción, en la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Select]**y elija una opción:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
