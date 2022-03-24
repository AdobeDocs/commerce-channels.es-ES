---
title: Instalar [!DNL Channel Manager]
description: Instale la extensión del administrador de canales.
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Instalación del administrador de canales

Consulte la [requisitos previos](onboard.md#prerequisites) y recopile la información necesaria antes de instalar el Administrador de canales.

## Actualizar la configuración de estabilidad mínima

Antes de instalar la extensión, actualice la variable `minimum-stability` requisitos de `composer.json` para que pueda instalar las versiones anteriores del Administrador de canales con Composer.

Para actualizar la configuración, agregue las siguientes líneas a la `composer.json` archivo.

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## Instalación de la extensión

Las instrucciones de instalación del Administrador de canales dependen de si Adobe Commerce o el Magento Open Source se implementan en las instalaciones o en la infraestructura de la nube.

- Instalar en un [Instancia local](#install-on-an-on-premises-instance).

- Instalar en un [[!DNL Adobe Commerce] en la instancia de infraestructura de nube](#install-adobe-commerce-on-cloud-infrastructure)

Ambos métodos requieren que utilice la Interfaz de Línea de Comandos (CLI).

>[!NOTE]
>
>Para obtener ayuda sobre la instalación [!DNL Commerce] software mediante CLI, consulte [Instalación general de CLI](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}.

### Instalar en una instancia local

Siga estas instrucciones para instalar en plataformas Adobe Commerce y Magento Open Source.

1. Inicie sesión en la [!DNL Commerce] servidor como [usuario con permisos](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target=&quot;_blank&quot;} para escribir en el [!DNL Commerce] sistema de archivos.

1. Coloque el sitio web en [modo de mantenimiento](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target=&quot;_blank&quot;}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. En el [!DNL Commerce] directorio raíz del proyecto, agregue el Administrador de canales a `composer.json`.

   ```bash
    $ composer require magento/channel-manager --no-update
   ```

1. Si se le solicita, introduzca las claves de acceso de su [!DNL Commerce] cuenta.

   Su clave pública es su nombre de usuario; la clave privada es su contraseña.

1. Actualice las dependencias e instale la extensión.

   ```bash
   $ composer update
   ```

   La variable `composer update` actualiza todas las dependencias. Para actualizar solo las dependencias relacionadas con el Administrador de canales, utilice este comando en su lugar: `composer update magento/channel-manager`.

1. Espere a que el Compositor termine de actualizar las dependencias del proyecto y resuelva los errores.

1. Verifique la instalación

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Respuesta de ejemplo:

   ```terminal
   Module is disabled
   ```

1. Registre la extensión de .

   ```bash
   $ bin/magento setup:upgrade
   ```

1. Si se le solicita, vuelva a compilar su [!DNL Commerce] proyecto.

   ```bash
   $ bin/magento setup:di:compile
   ```

1. Compruebe que la extensión esté habilitada:

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Respuesta de ejemplo:

   ```bash
   Module is enabled
   ```

1. Limpie la caché.

   ```bash
   $ bin/magento cache:clean
   ```

1. Deshabilite el modo de mantenimiento.

   ```bash
    $ bin/magento maintenance:disable
   ```

### Instalación en una instancia de infraestructura de nube de Adobe Commerce

Trabaje en una rama de desarrollo al añadir una extensión a la instancia de nube.

Para obtener ayuda sobre el uso de ramas, consulte [Introducción a la creación de ramas](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;} en la documentación para desarrolladores de Adobe Commerce.

Durante la instalación, el nombre de la extensión (`&lt;VendorName>\_&lt;ComponentName>`) se inserta automáticamente en la variable [app/etc/config.php](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html){target=&quot;_blank&quot;}. No es necesario que edite el archivo directamente.

1. En la estación de trabajo local, cambie al directorio raíz del proyecto de Cloud.

1. Crear o comprobar un desarrollo [Rama](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;}.

1. Con el nombre del Compositor, agregue la extensión al `require` de la sección `composer.json` archivo.

   ```bash
   $ composer require magento/channel-manager --no-update
   ```

1. Añadir, confirmar y enviar cambios en el código push: incluye cambios en ambas `composer.lock` y `composer.json` archivo.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Una vez finalizada la compilación e implementación, utilice SSH para iniciar sesión en el entorno remoto y verificar que la extensión se haya instalado correctamente.

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Respuesta de ejemplo:

   ```terminal
   Module is enabled
   ```

1. Una vez finalizada la instalación correctamente, inicie sesión en la [!UICONTROL Admin] a [configuración del conector de Commerce Services](connect.md).

   >[!NOTE]
   >
   >Para obtener instrucciones para actualizar el Administrador de canales a una nueva versión, consulte [Módulos de actualización y extensiones](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target=&quot;_blank&quot;}.


## Resolución de problemas

Utilice la siguiente información para resolver los errores que se producen durante el proceso de instalación del Administrador de canales.

### Claves de Compositor incorrectas

Si la variable [claves de acceso](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} utilizado para autenticarse en el repositorio del Compositor no es válido o no está vinculado al [!DNL MAGE ID] se usa para suscribirse al [!DNL Channel Manager] , aparece el siguiente error.


```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Compruebe la configuración de claves:

1. Busque la ubicación de la variable `auth.json` archivo:

   ```bash
   $ composer config –global home
   ```

1. Consulte la `auth.json` archivo.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Compruebe que las credenciales de auth.json coinciden [las claves asociadas con el ID de MAGE](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} se usa para registrarse en el servicio Administrador de canales.

### Memoria insuficiente para PHP

El siguiente error aparece si el sistema no tiene suficiente memoria asignada para PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilice cualquiera de los siguientes métodos para resolver el problema de memoria:

- [Aumente el límite de memoria para PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target=&quot;_blank&quot;} en el entorno `php.ini` archivo. Además, compruebe que la instancia de Commerce tenga la variable [valores recomendados](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target=&quot;_blank&quot;} para otros ajustes de PHP.

- Especifique el límite de memoria de la línea de comandos.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Por ejemplo:

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Vista que falta

Si aparece un error acerca de una falta `process_catalog_exporter_view` durante la instalación del administrador de canales, intente [actualización de los indexadores](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target=&quot;_blank&quot;}.

```bash
php bin/magento indexer:refresh
```

### Errores de implementación en la nube

Para ver los problemas de implementación de la extensión en la nube, consulte [error de implementación de extensiones](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target=&quot;_blank&quot;}.
