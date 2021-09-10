---
user-guide-title: Guía del usuario de Amazon Sales Channel
user-guide-description: Genere ventas a través de Amazon integrando Adobe Commerce o Magento Open Source con su cuenta [!DNL Amazon Seller Central] .
breadcrumb-title: Administrador de canales para comercio
source-git-commit: 52f2dd0f5a722af337be72a5d556f3780aad6548
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Canal de ventas de Amazon: [!DNL channel manager] para comercio de Adobe {#amazon}

- [Canal de ventas de Amazon](overview.md)
- Introducción {#getting-started}
   - [Acerca del canal de ventas de Amazon](about-amazon-sales-channel.md)
   - [Acerca de Amazon Marketplace](about-amazon-marketplace.md)
   - [Acerca de Amazon y su catálogo de comercio](about-listings-and-catalog.md)
   - [Prácticas recomendadas y limitaciones](amazon-best-practices.md)
   - [Instalación de la extensión](install.md)
- Incorporación {#onboarding}
   - [Canal de ventas integrado de Amazon](amazon-onboarding-home.md)
   - [Tareas previas a la configuración](amazon-pre-setup-tasks.md)
   - [Crear atributos [!DNL Commerce] para Amazon](ob-creating-magento-attributes.md)
   - [Comprobación de la clave de API de Amazon](amazon-verify-api-key.md)
   - [Integración de tiendas](store-integration.md)
   - [Crear regla de listado](ob-create-listing-rule.md)
   - [Configuración predeterminada de la tienda](default-store-settings.md)
- Administrar el canal de ventas {#manage}
   - [Página principal](amazon-sales-channel-home.md)
   - [Tiendas Amazon](managing-stores.md)
   - [Controles de Workspace](workspace-controls.md)
   - [Aprendizaje y preparación](learning-preparation.md)
   - Atributos {#attributes}
      - [Ver atributos](attributes-view.md)
      - [Administrar atributos](managing-attributes.md)
      - [Crear y editar atributos](creating-attributes.md)
      - [Ver asignación de atributos](amazon-matching-attributes-values.md)
   - [Configuración de administración del canal de ventas](sales-channel-settings.md)
   - [Panel de Amazon Store](amazon-store-dashboard.md)
   - [Configuración de almacenamiento](ob-store-review.md)
- Configuración de lista {#listing-settings}
   - [Ver configuración de listado](listing-settings.md)
   - [Acciones de listado de productos](product-listing-actions.md)
   - [Anuncios de terceros](third-party-listing-settings.md)
   - [Precio de anuncio](listing-price.md)
   - [(B2B) Precios comerciales](business-pricing.md)
   - [Existencias/Cantidad](stock-quantity.md)
   - [Cumplido por](fulfilled-by.md)
   - [Buscar en el catálogo](catalog-search.md)
   - [Condición de lista de productos](product-listing-condition.md)
   - [Productos renovados](renewed-products.md)
- [Configuración de pedidos](order-settings.md)
- [Configuración de integración de almacén](store-integration-settings.md)
- Reglas de lista y precios {#rules}
   - [Reglas de lista](listing-rules.md)
   - Reglas de precios {#pricing-rules}
      - [Administrar precios](pricing-products.md)
      - [Añadir nueva regla de precios](add-pricing-rule.md)
      - [Configuración general de regla de precio](pricing-rule-general-settings.md)
      - [Condiciones de regla de precio](pricing-rule-conditions.md)
      - [Acciones de regla de precio](pricing-rule-actions.md)
      - [Regla de precio estándar](standard-price-rules.md)
      - [Regla de reprecio inteligente](intelligent-repricing-rules.md)
      - [Variaciones condicionales de la competencia](competitor-conditional-variances.md)
      - [Ajuste de precio](price-adjustment.md)
      - [Precio mínimo](floor-price.md)
      - [Precio máximo opcional](optional-ceiling-price.md)
      - [Ámbito del precio](price-scope.md)
      - [lógica de prioridad de precio](price-priority-logic.md)
      - [Precio del competidor Buy Box](buy-box-competitor-pricing.md)
      - [Precios más bajos de los competidores](lowest-competitor-pricing.md)
   - Ejemplos {#rules-examples}
      - [Definición de una condición](ob-define-condition-example.md)
      - [Ejemplos de reglas de precio](price-rule-examples.md)
- Informes y registros {#reports-logs}
   - [Registros y almacene informes](amazon-logs-reports.md)
   - Almacenar informes {#store-reports}
      - [Análisis de precios competitivo](competitive-price-analysis.md)
      - [Mejoras en la lista](listing-improvements.md)
   - Registros {#logs}
      - [Registro de cambios en la lista](listing-changes-log.md)
      - [Registro de errores de comunicación](communication-errors-log.md)
- Administrar anuncios {#admin-listings}
   - [Administrar anuncios de Amazon](managing-product-listings.md)
   - Por estado/pestaña {#status-tab}
      - [Administrar por estado/ficha](managing-listings-by-tab.md)
      - [Anuncios incompletos](incomplete-listings.md)
      - [Nuevos anuncios de terceros](new-third-party-listings.md)
      - [Listo para la lista](ready-to-list.md)
      - [Anuncios inactivos](inactive-listings.md)
      - [Listas activas](active-listings.md)
      - [Anulaciones](overrides.md)
      - [Anuncios no aptos](ineligible-listings.md)
      - [Anuncios finalizados](ended-listings.md)
   - Por acciones {#actions}
      - [Administrar por acciones](managing-listings-by-action.md)
      - [Crear y asignar productos de catálogo](creating-assigning-catalog-products.md)
      - [Creación y edición de anulaciones](creating-editing-overrides.md)
      - [Crear un SKU de vendedor de alias](create-alias-seller-sku.md)
      - [Editar un ASIN asignado](edit-assigned-asin.md)
      - [Finalización de un anuncio de Amazon](end-listings-manually.md)
      - [Publicar un listado de Amazon](publish-listings-manually.md)
      - [Actualizar información requerida](amazon-manually-update-incomplete-listing.md)
      - [Ver detalles](product-listing-details.md)
- Administrar pedidos {#admin-orders}
   - [Administrar pedidos](managing-orders.md)
   - [Ver pedidos de Amazon](amazon-orders-all.md)
   - [Ver detalles de pedidos de Amazon](amazon-order-details.md)
   - [Tareas comunes de procesamiento de pedidos](common-order-processing.md)
   - [Flujos de trabajo de cumplimiento](fulfillment-workflows.md)
   - [Cancelar pedidos no enviados](cancel-unshipped-order.md)
