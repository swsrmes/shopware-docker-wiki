## Todo make new

The configuration of swdc will be saved at `$HOME/.config/swdc/env` after each change `swdc up` need to be executed.

# DEFAULT_DOMAIN

This defines the sub part of your Domains in default `dev.localhost`. After changing this variable, make sure you have deleted the SSL folder to enable the regeneration of the certificates.
`rm -rf "$HOME/.config/swdc/ssl/"`

# USE_SSL_DEFAULT

The build commands will use https for the Installation URL

# PERSISTENT_DATABASE

When you set this to false on any `swdc down` all databases are gone. This is very helpful when you don't need your Database state as it has a better performance

# CACHE_VOLUMES

Creates volume for the cache folder

# ENABLE_ELASTICSEARCH

Toggles the Elasticsearch Service

# ENABLE_REDIS

Toggles the Redis Service

# ENABLE_MINIO

Toggles the Minio Server (Local S3)

# PHP_VERSION

This defines the default PHP Version for all installations

# MYSQL_VERSION

This defines the MySQL Server Version

# EXPOSE_MYSQL_LOCAL

Exposes the MySQL Server to localhost. It needs to be enabled for MySQL GUI Applications as example

# DATABASE_TOOL

Allows to choose between adminer and phpmyadmin

# ENABLE_SELENIUM

Starts a Selenium Server (Needed for Shopware 5 Browser Tests)

# ENABLE_CYPRESS

Adds the Cypress services (Needed for Shopware 6 Browser Tests)

# CODE_DIRECTORY

Allow changing the default `~/Code` folder to somewhere else

# Blackfire

`ENABLE_BLACKFIRE` Enables Blackfire Service other Variables can be obtained from the Blackfire Account
You need still to enable for a Virtual Host Blackfire like

`VHOST_[FOLDER_NAME_UPPER_CASE]_IMAGE=ghcr.io/shyim/shopware-docker/6/nginx:php74-blackfire`

# WSL_XDEBUG_TUNNEL

This enables a hacky way to get XDebug Running on Windows with WSL2

## Custom Configuration for Virtual Hosts

* You can override the image, hosts and the used ssl certificate
* **FOLDER_NAME** has to be in uppercase. Example for image: Folder name is: **sw5**, VHOST_**SW5**_IMAGE

* VHOST_**FOLDER_NAME**_IMAGE
  * Allows changing the image that is used for this directory.
  * Files are mount to /var/www/html, the image should expose a webservice at port 80
* VHOST_**FOLDER_NAME**_HOSTS
  * This can be an list of hosts comma seperated. The first host will be used for the Installation
* VHOST_**FOLDER_NAME**_CERT_NAME
  * This can be used to define another ssl certificate for this vhost.
  * Example: `shop`. You will need following files  `~/.config/swdc/ssl/shop.crt` and `~/.config/swdc/ssl/shop.key`