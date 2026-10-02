# Apache2 Directories
Apache contains various directories each having its own specific function to perform
## List of various directories with its purpose

|Purpose|	Directory|
|-------|----------|
|Apache configuration|	/etc/apache2/|
|Main config	|/etc/apache2/apache2.conf|
|Virtual hosts	|/etc/apache2/sites-available/|
|Enabled virtual hosts	|/etc/apache2/sites-enabled/|
|Apache modules	|/etc/apache2/mods-available/|
|Enabled modules	|/etc/apache2/mods-enabled/|
|Document root|	/var/www/html/|
|Logs|	/var/log/apache2/|
|Runtime| files	/var/run/apache2/ or /run/apache2/|


## Apache configuration
 ```/etc/apache2/``` The main directory containing almost all Apache configuration files and subdirectories.



## Main config

``/etc/apache2/apache2.conf``

The primary Apache configuration file. It defines global settings such as timeouts, permissions, logging, modules, and configuration includes.

## Virtual hosts

``/etc/apache2/sites-available/``

Contains configuration files for websites/virtual hosts that can be enabled. Example: example.com.conf.

## Enabled virtual hosts

``/etc/apache2/sites-enabled/``

Contains symbolic links to the virtual hosts that are currently enabled. Apache loads these configurations.

## Available modules

``/etc/apache2/mods-available/``

Contains configuration files for Apache modules that are installed and available to use.

## Enabled modules

``/etc/apache2/mods-enabled/``

Contains symbolic links to modules from mods-available/ that are currently enabled.

## Document root

``/var/www/html/``

The default directory from which Apache serves website files such as index.html, PHP files, CSS, JavaScript, images, etc.

## Logs

``/var/log/apache2/``

Contains Apache log files, commonly access.log and error.log.

## Runtime files
``/run/apache2/ or /var/run/apache2/``

Temporary runtime information such as the Apache PID file and other files needed while Apache is running.
