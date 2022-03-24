---
title: Publicar anuncios en Walmart
description: Publique anuncios de productos de Commerce en Walmart Marketplace para comenzar a vender.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Publicar anuncios en Walmart

Al igual que otros mercados, Walmart permite a los vendedores de terceros listar artículos que otros venden.

La plataforma utiliza identificadores de producto como UPC y GTIN para hacer coincidir elementos que ya están en venta.
Para los productos coincidentes, la lista de Walmart Marketplace existente se actualiza para incluir la oferta para el producto Commerce.
Normalmente, los productos con los precios más bajos aparecen primero en los resultados. Sin embargo, otros factores como las revisiones también afectan a la ubicación.

## Flujo de trabajo de coincidencias

Cuando coincide con productos, Channel Manager envía los datos del producto a Walmart Marketplace para buscar anuncios existentes con valores de atributo que coincidan con el atributo del producto de Commerce asignado.

Si se encuentra una coincidencia, la lista de productos existente se actualiza para añadir la oferta.

## Requisitos previos

Antes de hacer coincidir productos, compruebe que los valores de atributos del catálogo de productos cumplen los requisitos de Walmart y configure los atributos. Consulte [Configurar la coincidencia de productos](map-product-attributes-for-matching.md)

## Seleccionar y buscar coincidencias en los productos

1. Abra un canal de ventas conectado.

1. De **[!UICONTROL Listings]**, seleccione los productos para las coincidencias que se encuentran en *[!UICONTROL Draft]* estado.

   ![Seleccione productos de los anuncios y envíe para que coincidan](assets/products-in-marketplace-sales-channel.png)

1. Select **[!UICONTROL Match Products]**.

   Un mensaje indica el número de productos enviados para la coincidencia.

   ![Enviar productos al canal de ventas conectado](assets/products-submit-for-matching.png)

   Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

   El estado de los productos seleccionados cambia a *[!UICONTROL Processing]* hasta que se completen las operaciones de coincidencia. Walmart Marketplace puede tardar hasta 30 minutos en completar la operación del partido.

## Comprobar estado de coincidencia

1. Select **Actualizar productos** para actualizar el estado del producto más actual.

1. Compruebe el estado del producto.

   Una vez finalizada la coincidencia, el estado puede ser *Coincidencia* o *Error*.

   * **[!UICONTROL Match]** indica que el producto se encontró correctamente. Su oferta de producto se publicó en una lista de Walmart Marketplace existente.

   * **[!UICONTROL Error]** indica una de las siguientes opciones:

      * Se produjo un error y la operación de coincidencia falló.

      * No se encontró ninguna coincidencia.

      * Coincidencia encontrada, pero producto publicado como ensayo porque la variable [El almacén de Marketplace no está activo](walmart-prerequisites.md#walmart-marketplace-store-status).

## Solución de problemas de errores de coincidencia de productos

Si la operación de coincidencia del producto falla, Walmart Marketplace devuelve un código de error y Channel Manager muestra el estado de error en la información de la lista del producto.

Vea los detalles de los mensajes de error pasando el ratón sobre el **Error** etiqueta de estado. Los errores comunes devueltos tienen un formato incorrecto de los valores de ID de producto o carecen de los atributos necesarios.

## Corrección de los valores de ID de producto

| Tipo | Descripción | Ejemplo |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, el número de 12 dígitos incluyendo el dígito de comprobación.</br></br>Si su UPC tiene menos de 12 dígitos, como UPC-E que es de 8 dígitos, agregue</br>llevar ceros a cumplir el requisito. | Cambiar desde `45678912345` a `045678912345` |
| GTIN | GTIN-14, el número de 14 dígitos incluyendo el dígito de comprobación.</br></br>Si su GTIN tiene menos de 14 dígitos, agregue ceros a la izquierda </br>para satisfacer los requisitos. | Cambiar `456789123456` a `0045678912345` |
| EAN | GTIN-13, el número de 13 dígitos incluyendo el dígito de comprobación.</br></br>Si el EAN tiene menos de 13 dígitos, agregue al principio</br>ceros para satisfacer los requisitos. | Cambiar desde `4567891234` a `0004567891234` |

Para obtener más información sobre los códigos de error de Walmart Marketplace, consulte la [Ayuda para vendedores de Walmart](https://sellerhelp.walmart.com/s/guide?article=000005844).
