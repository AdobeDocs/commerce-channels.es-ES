---
title: "Incorporado [!DNL Amazon Sales Channel]"
description: Obtenga información acerca de las tareas previas a la configuración, los pasos de incorporación y cómo funciona Amazon con la Sales Channel de Amazon en Adobe Commerce y Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Incorporar [!DNL Amazon Sales Channel]

En esta sección se describen las tareas previas a la configuración, los pasos de incorporación y algunos conceptos clave del funcionamiento de Amazon con el canal de ventas de Amazon en Adobe Commerce y Magento Open Source.

La extensión [!DNL Amazon Sales Channel] admite varias tiendas Amazon. Para una sola cuenta de [!DNL Amazon Seller Central] que opere en la región de Amazon en EE. UU./Canadá/México, cree tres tiendas Amazon (una para ventas en EE. UU., otra para ventas en México y otra para ventas en Canadá). Cada una de las tres tiendas define el país de mercado durante su creación. Si tiene más de una cuenta de [!DNL Amazon Seller Central], podría tener potencialmente hasta tres tiendas Amazon para cada una de sus cuentas de [!DNL Amazon Seller Central]. Si también vendes en el Reino Unido, tendrías una cuarta tienda de Amazon.

>[!TIP]
>
>Se requiere una [cuenta de vendedor profesional](https://sell.amazon.com/){target="_blank"} en [!DNL Amazon Seller Central] en la región de Norteamérica o Europa (Reino Unido). Amazon cobra una suscripción mensual y tarifas por vender. Ver [Amazon: elige tu plan de venta](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>La incorporación es sencilla: crea tu tienda y luego conéctala a tu cuenta de [!DNL Amazon Seller Central].
>Cuando tu tienda está conectada, el canal de Amazon intenta importar tus anuncios de Amazon y hacerlos coincidir con tu catálogo, según tu [asignación de atributos](./attributes-view.md).<br><br>
>La configuración del canal de ventas de Amazon afecta a los anuncios de Amazon. La configuración inicial del anuncio, los precios y el producto es la predeterminada. Puedes modificar tu [configuración de la tienda](./ob-store-review.md) (anuncio, precio, pedido e informes) una vez que la tienda esté conectada a tu cuenta de [!DNL Amazon Seller Central].

| Pasos | Qué sucede |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas previas a la instalación](./amazon-pre-setup-tasks.md) | Antes de incorporarse, debe asegurarse de que tiene una cuenta de [!DNL Amazon Seller Central] activa y aprobada. También hay algunos [!DNL Commerce] requisitos y recomendaciones que se deben completar antes de la incorporación. |
| [Verificar la clave API de Amazon](./amazon-verify-api-key.md) | Al acceder al canal de ventas de Amazon, [!DNL Commerce] comprueba y valida automáticamente la clave de API de Amazon que añadió en la configuración de su tienda. Si la clave de API no se ha agregado o no es válida, se le pedirá que [agregue o actualice la clave de API de Amazon](./amazon-verify-api-key.md). |
| [Integración de tienda](./store-integration.md) | Este paso incluye la creación de un almacén de canales de ventas de Amazon y luego conectarlo a su cuenta de [!DNL Amazon Seller Central]. Necesita las credenciales de inicio de sesión principales de la cuenta de [!DNL Amazon Seller Central] (el correo electrónico o el teléfono usado para crear la cuenta de vendedor) para realizar este paso. |
| [Crear regla de anuncio](./ob-create-listing-rule.md) | Después de conectar el almacén del canal de ventas de Amazon, se le pedirá que cree una regla de listado. Se recomienda realizar este paso, pero también puede omitirlo para iniciar el proceso de importación del listado. También puedes acceder a la configuración de tu [tienda y anuncio](./ob-store-review.md) en el [tablero](./amazon-store-dashboard.md) de la tienda. |
