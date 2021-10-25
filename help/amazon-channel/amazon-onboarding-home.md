---
title: Sales Channel integrada de Amazon
description: Obtenga información sobre las tareas previas a la configuración, los pasos de incorporación y cómo funciona Amazon con la Sales Channel de Amazon en Adobe Commerce y Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Canal de ventas integrado de Amazon

En esta sección se describen las tareas previas a la configuración, los pasos para la incorporación y algunos conceptos clave sobre cómo funciona Amazon con el canal de ventas de Amazon en Adobe Commerce y el Magento Open Source.

La variable [!DNL Amazon Sales Channel] admite varias tiendas Amazon. Para un [!DNL Amazon Seller Central] cuenta que opera en la región de Amazon EE.UU./Canadá/México, cree tres tiendas de Amazon (una para ventas en EE.UU., ventas en México y ventas en Canadá). Cada una de las tres tiendas define el país del mercado durante su creación. Si tiene más de uno [!DNL Amazon Seller Central] podría tener hasta tres tiendas de Amazon para cada una de sus [!DNL Amazon Seller Central] cuentas. Si también vende en el Reino Unido, tendrá una cuarta tienda de Amazon.

>[!TIP]
>
>A [Cuenta de vendedor profesional](https://sell.amazon.com/){target=&quot;_blank&quot;} en [!DNL Amazon Seller Central] en la región de América del Norte o Europa (Reino Unido). Amazon cobra una suscripción mensual y tarifas de venta. Consulte [Amazon: Elige tu plan de ventas](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>La incorporación es sencilla: cree su tienda y conéctela a su [!DNL Amazon Seller Central] cuenta.
>Cuando la tienda está conectada, el canal de Amazon intenta importar los anuncios de Amazon y hacerlos coincidir con el catálogo, según el [asignación de atributos](./attributes-view.md).<br><br>
>La configuración del canal de ventas de Amazon afecta a los anuncios de Amazon. Su anuncio inicial, sus precios y la configuración del producto tienen valores predeterminados para usted. Puede modificar su [configuración de almacenamiento](./ob-store-review.md) (listado, precio, pedido e informe) una vez que la tienda esté conectada a su [!DNL Amazon Seller Central] cuenta.

| Pasos | Qué sucede |
|--- |--- |
| [Tareas previas a la configuración](./amazon-pre-setup-tasks.md) | Antes de incorporarse, debe asegurarse de tener una [!DNL Amazon Seller Central] cuenta. También hay algunas [!DNL Commerce] requisitos y recomendaciones que deben cumplimentarse antes de la incorporación. |
| [Comprobación de la clave de API de Amazon](./amazon-verify-api-key.md) | Al acceder al canal de ventas de Amazon, [!DNL Commerce] comprueba y valida automáticamente la clave de API de Amazon que ha añadido en la configuración de la tienda. Si la clave de API no se ha agregado o no es válida, se le pedirá que [agregar o actualizar la clave de API de Amazon](./amazon-verify-api-key.md). |
| [Integración de tiendas](./store-integration.md) | Este paso incluye la creación de un almacén de canales de ventas de Amazon y luego la conexión a su [!DNL Amazon Seller Central] cuenta. Necesita las credenciales de inicio de sesión principales para su [!DNL Amazon Seller Central] cuenta (el correo electrónico o el teléfono utilizados para crear la cuenta de vendedor) para este paso. |
| [Crear regla de lista](./ob-create-listing-rule.md) | Después de conectar el almacén de canales de ventas de Amazon, se le pedirá que cree una regla de anuncio. Se recomienda realizar este paso, pero también se puede omitir para iniciar el proceso de importación de listas. También puede acceder a su [configuración de tiendas y listas](./ob-store-review.md) en la tienda [tablero](./amazon-store-dashboard.md). |
