---
user-guide-title: Guía del usuario de Amazon Sales Channel
user-guide-description: Genere ventas a través de Amazon integrando Adobe Commerce o un Magento Open Source con su [!DNL Amazon Seller Central] cuenta.
breadcrumb-title: Canal de ventas de Amazon
role: Admin, User
feature: Sales Channels
recommendations: noDisplay
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# Canal de ventas de Amazon - [!DNL channel manager] para Adobe Commerce {#amazon}

- [Guía del usuario de Amazon Sales Channel](guide-overview.md)
- [Introducción al canal de ventas de Amazon](overview.md)
- Primeros pasos {#getting-started}
   - [Acerca de Amazon Marketplace](about-amazon-marketplace.md)
   - [Amazon y el catálogo de Commerce](about-listings-and-catalog.md)
   - [Prácticas recomendadas y limitaciones](amazon-best-practices.md)
   - [Instalación de la extensión](install.md)
- Incorporación {#onboarding}
   - [Incorporar el canal de ventas de Amazon](amazon-onboarding-home.md)
   - [Tareas previas a la configuración](amazon-pre-setup-tasks.md)
   - [Crear [!DNL Commerce] atributos para Amazon](ob-creating-magento-attributes.md)
   - [Compruebe la clave de API de Amazon](amazon-verify-api-key.md)
   - [Integración de tienda](store-integration.md)
   - [Crear regla de listado](ob-create-listing-rule.md)
   - [Configuración de tienda predeterminada](default-store-settings.md)
- Administrar el canal de ventas {#manage}
   - [Página de inicio](amazon-sales-channel-home.md)
   - [tiendas Amazon](managing-stores.md)
   - [Controles de Workspace](workspace-controls.md)
   - [Aprendizaje y preparación](learning-preparation.md)
   - Atributos {#attributes}
      - [Ver atributos](attributes-view.md)
      - [Administrar atributos](managing-attributes.md)
      - [Crear y editar atributos](creating-attributes.md)
      - [Ver asignación de atributos](amazon-matching-attributes-values.md)
   - [Configuración de administración del canal de ventas](sales-channel-settings.md)
   - [Tablero de la tienda Amazon](amazon-store-dashboard.md)
   - [Configuración de tienda](ob-store-review.md)
- Configuración de anuncio {#listing-settings}
   - [Ver configuración de listado](listing-settings.md)
   - [Acciones de lista de productos](product-listing-actions.md)
   - [Anuncios de terceros](third-party-listing-settings.md)
   - [Precio de venta](listing-price.md)
   - [(B2B) precios empresariales](business-pricing.md)
   - [Existencias/cantidad](stock-quantity.md)
   - [Cumplido por](fulfilled-by.md)
   - [Búsqueda en catálogo](catalog-search.md)
   - [Condición de lista de productos](product-listing-condition.md)
   - [Productos renovados](renewed-products.md)
- [Configuración de pedidos](order-settings.md)
- [Configuración de integración de tienda](store-integration-settings.md)
- Reglas de precios y listados {#rules}
   - [Reglas de listado](listing-rules.md)
   - Reglas de precios {#pricing-rules}
      - [Administrar precios](pricing-products.md)
      - [Añadir nueva regla de precios](add-pricing-rule.md)
      - [Configuración general de regla de precio](pricing-rule-general-settings.md)
      - [Condiciones de regla de precio](pricing-rule-conditions.md)
      - [Acciones de regla de precio](pricing-rule-actions.md)
      - [Regla de precio estándar](standard-price-rules.md)
      - [Regla de reasignación de precios inteligente](intelligent-repricing-rules.md)
      - [Variaciones condicionales del competidor](competitor-conditional-variances.md)
      - [Ajuste de precio](price-adjustment.md)
      - [Precio mínimo](floor-price.md)
      - [Precio máximo opcional](optional-ceiling-price.md)
      - [Alcance del precio](price-scope.md)
      - [Lógica de prioridad de precios](price-priority-logic.md)
      - [Precios de competidor Buy Box](buy-box-competitor-pricing.md)
      - [Precios más bajos para competidores](lowest-competitor-pricing.md)
   - Ejemplos {#rules-examples}
      - [Definición de una condición](ob-define-condition-example.md)
      - [Ejemplos de reglas de precios](price-rule-examples.md)
- Informes y registros {#reports-logs}
   - [Registros e informes de tienda](amazon-logs-reports.md)
   - Almacenar informes {#store-reports}
      - [Análisis de precios competitivos](competitive-price-analysis.md)
      - [Mejoras de anuncios](listing-improvements.md)
   - Registros {#logs}
      - [Registro de cambios de lista](listing-changes-log.md)
      - [Registro de errores de comunicación](communication-errors-log.md)
- Administrar anuncios {#admin-listings}
   - [Administrar listados de Amazon](managing-product-listings.md)
   - Por estado/ficha {#status-tab}
      - [Administrar por estado/pestaña](managing-listings-by-tab.md)
      - [Anuncios incompletos](incomplete-listings.md)
      - [Nuevos anuncios de terceros](new-third-party-listings.md)
      - [Listo para la lista](ready-to-list.md)
      - [Anuncios inactivos](inactive-listings.md)
      - [Anuncios activos](active-listings.md)
      - [Invalidaciones](overrides.md)
      - [Anuncios no aptos](ineligible-listings.md)
      - [Anuncios finalizados](ended-listings.md)
   - Por acciones {#actions}
      - [Administrar por acciones](managing-listings-by-action.md)
      - [Creación y asignación de productos de catálogo](creating-assigning-catalog-products.md)
      - [Crear y editar invalidaciones](creating-editing-overrides.md)
      - [Crear un SKU de vendedor de alias](create-alias-seller-sku.md)
      - [Editar un ASIN asignado](edit-assigned-asin.md)
      - [Finalizar un anuncio de Amazon](end-listings-manually.md)
      - [Publicar un anuncio de Amazon](publish-listings-manually.md)
      - [Actualizar información necesaria](amazon-manually-update-incomplete-listing.md)
      - [Ver detalles](product-listing-details.md)
- Administrar pedidos {#admin-orders}
   - [Administrar pedidos](managing-orders.md)
   - [Ver pedidos de Amazon](amazon-orders-all.md)
   - [Ver detalles del pedido de Amazon](amazon-order-details.md)
   - [Tareas comunes de procesamiento de pedidos](common-order-processing.md)
   - [Flujos de trabajo de cumplimiento](fulfillment-workflows.md)
   - [Cancelar pedidos no enviados](cancel-unshipped-order.md)
- [Notas de versión](release-notes.md)
