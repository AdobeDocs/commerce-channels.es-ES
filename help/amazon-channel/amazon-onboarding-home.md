---
title: "A bordo [!DNL Amazon Sales Channel]"
description: Obtenga información acerca de las tareas previas a la configuración, los pasos de incorporación y cómo funciona Amazon con la Sales Channel de Amazon en Adobe Commerce y Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# A bordo [!DNL Amazon Sales Channel]

En esta sección se describen las tareas previas a la configuración, los pasos de incorporación y algunos conceptos clave del funcionamiento de Amazon con el canal de ventas de Amazon en Adobe Commerce y Magento Open Source.

El [!DNL Amazon Sales Channel] La extensión de admite varias tiendas Amazon. Para un solo [!DNL Amazon Seller Central] cuenta que opera en la región de Amazon en EE. UU./Canadá/México, cree tres tiendas Amazon (una para ventas en EE. UU., otra para ventas en México y otra para ventas en Canadá). Cada una de las tres tiendas define el país de mercado durante su creación. Si tiene más de uno [!DNL Amazon Seller Central] cuenta, podría tener hasta tres tiendas Amazon para cada una de sus [!DNL Amazon Seller Central] cuentas. Si también vendes en el Reino Unido, tendrías una cuarta tienda de Amazon.

>[!TIP]
>
>A [Cuenta de vendedor profesional](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>La incorporación es sencilla: cree su tienda y conéctela a su [!DNL Amazon Seller Central] cuenta.
>Cuando la tienda está conectada, el canal de Amazon intenta importar los anuncios de Amazon y hacerlos coincidir con el catálogo, en función de las [asignación de atributos](./attributes-view.md).<br><br>
>La configuración del canal de ventas de Amazon afecta a los anuncios de Amazon. La configuración inicial del anuncio, los precios y el producto es la predeterminada. Puede modificar su [configuración de tienda](./ob-store-review.md) (listado, precios, pedidos e informes) después de que su tienda esté conectada a su [!DNL Amazon Seller Central] cuenta.

| Pasos | Qué sucede |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas previas a la instalación](./amazon-pre-setup-tasks.md) | Antes de incorporarse, debe asegurarse de que tiene un activo y aprobado [!DNL Amazon Seller Central] cuenta. También hay algunos [!DNL Commerce] requisitos y recomendaciones que se deben completar antes de la incorporación. |
| [Verificar la clave de API de Amazon](./amazon-verify-api-key.md) | Al acceder al canal de ventas de Amazon, [!DNL Commerce] comprueba y valida automáticamente la clave de API de Amazon que añadió en la configuración de la tienda. Si la clave de API no se ha añadido o no es válida, se le pedirá que [añadir o actualizar la clave de API de Amazon](./amazon-verify-api-key.md). |
| [Integración de tienda](./store-integration.md) | Este paso incluye la creación de un almacén de canales de ventas de Amazon y su posterior conexión con el [!DNL Amazon Seller Central] cuenta. Necesita las credenciales de inicio de sesión principales para su [!DNL Amazon Seller Central] cuenta (el correo electrónico o teléfono usado para crear la cuenta de vendedor) para este paso. |
| [Crear regla de anuncio](./ob-create-listing-rule.md) | Después de conectar el almacén del canal de ventas de Amazon, se le pedirá que cree una regla de listado. Se recomienda realizar este paso, pero también puede omitirlo para iniciar el proceso de importación del listado. También puede acceder a su [configuración de tiendas y listados](./ob-store-review.md) en la tienda [tablero](./amazon-store-dashboard.md). |
