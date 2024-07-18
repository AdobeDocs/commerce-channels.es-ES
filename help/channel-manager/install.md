---
title: 'Instalar [!DNL Channel Manager]'
description: 'Instale la extensión [!DNL Channel Manager].'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 1e74150e6ac88dbabb2e4bbb2fa2f243072eb03f
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# Instalar [!DNL Channel Manager]

Revise los [requisitos](onboard.md#requirements) y recopile la información necesaria antes de instalar Channel Manager.

## Instalación de la extensión

Las instrucciones de instalación de Channel Manager dependen de si Adobe Commerce o Magento Open Source se implementan de forma local o en la infraestructura en la nube.

- Instalar en [instancia local](#install-on-an-on-premises-instance).

- Instalar en [[!DNL Adobe Commerce] instancia de infraestructura en la nube](#install-adobe-commerce-on-cloud-infrastructure)

Ambos métodos requieren que utilice la Interfaz de línea de comandos (CLI).

>[!NOTE]
>
>Para obtener ayuda para instalar el software [!DNL Commerce] mediante la CLI, consulte [Instalar una extensión](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### Instalación en una instancia local

Siga estas instrucciones para instalar [!DNL Channel Manager] en Adobe Commerce y Magento Open Source en una instancia local.

1. Inicie sesión en el servidor [!DNL Commerce] como [usuario con permisos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) para escribir en el sistema de archivos [!DNL Commerce].

1. Ponga su sitio web en [modo de mantenimiento](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Desde el directorio raíz del proyecto [!DNL Commerce], agregue el Administrador de canales a `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Si se le solicita, escriba las claves de acceso de su cuenta de [!DNL Commerce].

   Su clave pública es su nombre de usuario; su clave privada es su contraseña.

1. Actualice las dependencias e instale la extensión de.

   ```bash
   composer update magento/channel-manager
   ```

   El comando `composer update` actualiza solamente las dependencias necesarias para [!DNL Channel Manager]. Para actualizar todas las dependencias, use este comando en su lugar: `composer update`.

1. Espere a que el Compositor termine de actualizar las dependencias del proyecto y resuelva los errores.

1. Compruebe la instalación del módulo:

   - Compruebe el estado del módulo.

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     Respuesta de ejemplo:

     ```
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

1. Si se le solicita, vuelva a compilar el proyecto [!DNL Commerce].

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

Para obtener ayuda sobre el uso de las ramas, consulte [Introducción a la creación de ramas](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) en la _Guía de infraestructura de Commerce en la nube_.

Durante la instalación, el nombre de la extensión (`magento\channel-manager`) se inserta automáticamente en el archivo [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html). No es necesario editar el archivo directamente.

1. En la estación de trabajo local, cambie al directorio raíz del proyecto de Cloud.

1. Cree o desproteja una [rama](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) de desarrollo.

1. Usando el nombre del Compositor, agregue la extensión a la sección `require` del archivo `composer.json`.

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Actualice las dependencias e instale la extensión de.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   El comando `composer update` actualiza solamente las dependencias necesarias para [!DNL Channel Manager]. Para actualizar todas las dependencias, use este comando en su lugar: `composer update`.

1. Agregue, confirme y inserte cambios de código: incluya cambios en los archivos `composer.lock` y `composer.json`.

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

```
Module is enabled
```

Si el módulo está deshabilitado, [actívelo en su entorno local](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) e implemente sus cambios.


1. Después de instalar correctamente la extensión, inicie sesión en [!UICONTROL Admin] para [configurar el conector de servicios de Commerce](connect.md).

   >[!NOTE]
   >
   >Para obtener instrucciones para actualizar el Administrador de canales a una nueva versión, consulte [Actualizar módulos y extensiones](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## Resolución de problemas

Utilice la siguiente información para resolver los errores que se producen durante el proceso de instalación de Channel Manager.

### Claves de composición incorrectas

Si las [claves de acceso](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilizadas para autenticarse en el repositorio de Composer no son válidas o no están vinculadas al [!DNL MAGE ID] utilizado para registrarse en el servicio [!DNL Channel Manager], se mostrará el siguiente error.

```
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Compruebe la configuración de la clave:

1. Buscar la ubicación del archivo `auth.json`:

   ```bash
   $ composer config –global home
   ```

1. Ver el archivo `auth.json`.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Compruebe que las credenciales de auth.json coinciden con [las claves asociadas con el ID de MAGE](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilizadas para registrarse en el servicio de Channel Manager.

### Memoria insuficiente para PHP

El siguiente error se muestra si el sistema no tiene suficiente memoria asignada para PHP.

```
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilice cualquiera de los siguientes métodos para resolver el problema de memoria:

- [Aumente el límite de memoria para PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) en el archivo de entorno `php.ini`. Compruebe también que la instancia de Commerce tiene los [valores recomendados](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) para otras configuraciones de PHP.

- Especifique el límite de memoria desde la línea de comandos.

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  Por ejemplo:

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### Falta la vista

Si aparece un error sobre un(a) `process_catalog_exporter_view` que falta durante la instalación de Channel Manager, intente [actualizar los indexadores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### Errores de implementación de Cloud

Para ver los problemas al implementar la extensión en la nube, consulte [error de implementación de extensión](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
