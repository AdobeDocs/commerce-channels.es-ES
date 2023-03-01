---
title: 'Instalar [!DNL Channel Manager]'
description: 'Instalar el[!DNL Channel Manager] Extensión de.'
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 96016b086a2c6567fab66b497892022f172f4bdd
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---


# Instalar [!DNL Channel Manager]

Revise la [requisitos](onboard.md#requirements) y recopile la información necesaria antes de instalar Channel Manager.

## Instalación de la extensión

Las instrucciones de instalación de Channel Manager dependen de si Adobe Commerce o Magento Open Source se implementan de forma local o en la infraestructura en la nube.

- Instalar en un [Instancia local de](#install-on-an-on-premises-instance).

- Instalar en un [[!DNL Adobe Commerce] en instancia de infraestructura en la nube](#install-adobe-commerce-on-cloud-infrastructure)

Ambos métodos requieren que utilice la Interfaz de línea de comandos (CLI).

>[!NOTE]
>
>Para obtener ayuda sobre la instalación [!DNL Commerce] mediante la CLI, consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target="_blank"}.

### Instalación en una instancia local

Siga estas instrucciones para instalar [!DNL Channel Manager] en Adobe Commerce y Magento Open Source a una instancia local.

1. Inicie sesión en [!DNL Commerce] server as a [usuario con permisos](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target="_blank"} para escribir en [!DNL Commerce] sistema de archivos.

1. Coloque el sitio web en [modo de mantenimiento](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target="_blank"}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Desde el [!DNL Commerce] directorio raíz del proyecto, agregue el Administrador de canales a `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Si se le solicita, introduzca las claves de acceso desde su [!DNL Commerce] cuenta.

   Su clave pública es su nombre de usuario; su clave privada es su contraseña.

1. Actualice las dependencias e instale la extensión de.

   ```bash
   composer update magento/channel-manager
   ```

   El `composer update` El comando actualiza solo las dependencias necesarias para [!DNL Channel Manager]. Para actualizar todas las dependencias, utilice este comando: `composer update`.

1. Espere a que el Compositor termine de actualizar las dependencias del proyecto y resuelva los errores.

1. Compruebe la instalación del módulo:

   - Compruebe el estado del módulo.

      ```bash
      bin/magento module:status Magento_SalesChannels
      ```

      Respuesta de ejemplo:

      ```terminal
      Module is enabled
      ```

   - Si el módulo no está habilitado, actívelo.

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. Registre la extensión de.

   ```bash
   bin/magento setup:upgrade
   ```

1. Si se le solicita, vuelva a compilar su [!DNL Commerce] proyecto.

   ```bash
   bin/magento setup:di:compile
   ```

1. Limpie la caché.

   ```bash
   bin/magento cache:clean
   ```

1. Desactive el modo de mantenimiento.

   ```bash
   bin/magento maintenance:disable
   ```

### Instalar en una instancia de Adobe Commerce en la infraestructura de la nube

Trabaje en una rama de desarrollo al añadir una extensión a la instancia de la nube.

Para obtener ayuda sobre el uso de ramas, consulte [Introducción a la creación de ramas](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target="_blank"} en la documentación para desarrolladores de Adobe Commerce.

Durante la instalación, el nombre de la extensión (`magento\channel-manager`) se inserta automáticamente en [app/etc/config.php](https://devdocs.magento.com/cloud/live/sens-data-over.html#configuration-data){target="_blank"} archivo. No es necesario editar el archivo directamente.

1. En la estación de trabajo local, cambie al directorio raíz del proyecto de Cloud.

1. Crear o extraer un desarrollo [ramificación](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target="_blank"}.

1. Utilizando el nombre del compositor, añada la extensión a `require` de la sección `composer.json` archivo.

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Actualice las dependencias e instale la extensión de.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   El `composer update` El comando actualiza solo las dependencias necesarias para [!DNL Channel Manager]. Para actualizar todas las dependencias, utilice este comando: `composer update`.

1. Agregar, confirmar y enviar cambios de código de inserción: incluyen cambios en ambos `composer.lock` y `composer.json` archivo.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Una vez completado el proceso de generación e implementación, utilice SSH para iniciar sesión en el entorno remoto y comprobar que la extensión se ha instalado correctamente.

```bash
   bin/magento module:status Magento_SalesChannels
```

Respuesta de ejemplo:

```terminal
Module is enabled
```

Si el módulo está desactivado, [habilitarlo en su entorno local](https://devdocs.magento.com/cloud/howtos/install-components.html#manage-extensions) e implementar los cambios.


1. Después de instalar correctamente la extensión, inicie sesión en [!UICONTROL Admin] hasta [configuración de Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >Para obtener instrucciones sobre cómo actualizar el Administrador de canales a una nueva versión, consulte [Actualización de módulos y extensiones](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target="_blank"}.


## Solución de problemas

Utilice la siguiente información para resolver los errores que se producen durante el proceso de instalación de Channel Manager.

### Claves de composición incorrectas

Si la variable [claves de acceso](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"} Los archivos utilizados para autenticarse en el repositorio del Compositor no son válidos o no están vinculados al [!DNL MAGE ID] se usa para registrarse en [!DNL Channel Manager] , se muestra el siguiente error.

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Compruebe la configuración de la clave:

1. Buscar la ubicación de `auth.json` archivo:

   ```bash
   $ composer config –global home
   ```

1. Ver el `auth.json` archivo.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Compruebe que las credenciales de auth.json coincidan [las claves asociadas con el ID de MAGE](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"} se utiliza para registrarse en el servicio Channel Manager.

### Memoria insuficiente para PHP

El siguiente error se muestra si el sistema no tiene suficiente memoria asignada para PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilice cualquiera de los siguientes métodos para resolver el problema de memoria:

- [Aumente el límite de memoria para PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target="_blank"} in the environment `php.ini` file. Also, verify that the Commerce instance has the [recommended values](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target="_blank"} para otros ajustes de PHP.

- Especifique el límite de memoria desde la línea de comandos.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Por ejemplo:

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Falta la vista

Si recibe un error sobre una pérdida `process_catalog_exporter_view` durante la instalación de Channel Manager, intente lo siguiente [actualización de los indexadores](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target="_blank"}.

```bash
php bin/magento indexer:refresh
```

### Errores de implementación de Cloud

Para ver los problemas al implementar la extensión en la nube, consulte [error de implementación de extensión](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target="_blank"}.
