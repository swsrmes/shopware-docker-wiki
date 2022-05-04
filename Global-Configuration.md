The configuration of swdc will be saved at `$HOME/.config/swdc/env` after each change `swdc up` need to be executed. You can use also `swdc configure` to open the Config.

The default config looks like so
```
# Default domain. Each folder will be a subdomain of this domain.
# After changing this variable, make sure you have deleted the SSL folder to enable the regeneration of the certificates.
# `rm -rf "$HOME/.config/swdc/ssl/"`
DEFAULT_DOMAIN="dev.localhost"

# Default services domain (for adminer, elasticsearch)
DEFAULT_SERVICES_DOMAIN="localhost"

# Use SSL as default
USE_SSL_DEFAULT=false

# Persistent Database?
PERSISTENT_DATABASE=true

# Default MySQL host
DEFAULT_MYSQL_HOST=mysql

# Elasticsearch
ENABLE_ELASTICSEARCH=false

ELASTICSEARCH_IMAGE="blacktop/elasticsearch:7.10"
KIBANA_IMAGE="blacktop/kibana:7.10"

# Redis
ENABLE_REDIS=false

# S3 compatible Server
ENABLE_MINIO=false

# Possible values are 7.1, 7.2, 7.3, 7.4, 8.0, 8.1
PHP_VERSION=7.4

# Possible values are ghcr.io/shyim/shopware-docker/mysql:57, ghcr.io/shyim/shopware-docker/mysql:8 for MySQL configured versions
# Also possible offical images like mysql:X mariadb:X
MYSQL_VERSION=ghcr.io/shyim/shopware-docker/mysql:8

# Expose mysql port to host
EXPOSE_MYSQL_LOCAL=true

# Http port
HTTP_PORT=80

# Https port
HTTPS_PORT=443

# Possible values are adminer / phpmyadmin
DATABASE_TOOL=adminer

# Selenium Server
ENABLE_SELENIUM=false

# Cypres support
ENABLE_CYPRESS=false

# Source code root directory
CODE_DIRECTORY="$HOME/Code"

# Blackfire configurations
ENABLE_BLACKFIRE=false
BLACKFIRE_SERVER_ID=
BLACKFIRE_SERVER_TOKEN=
BLACKFIRE_CLIENT_ID=
BLACKFIRE_CLIENT_TOKEN=

# Varnish
ENABLE_VARNISH=false

# Enable WSL XDebug Tunnel. This is the ugglyst hack ever I did to get something running. PhpStorm Traffic will be fowarded as socket to the nginx container. The socat inside the container will make it available at port 9050 inside the container. XDebug will use that port to connect to PhpStorm
WSL_XDEBUG_TUNNEL=false

# Configure this if you want to move the mysql data into a different directory, default to swdc dir
# MYSQL_DATA_DIR=/var/lib/swdc/mysql
```

# Blackfire

`ENABLE_BLACKFIRE` Enables Blackfire Service other Variables can be obtained from the Blackfire Account
You still need to enable for a Virtual Host Blackfire like

`VHOST_[FOLDER_NAME_UPPER_CASE]_IMAGE=ghcr.io/shyim/shopware-docker/6/nginx:php74-blackfire`