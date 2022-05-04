## Custom Config in the Global configuration

Some configurations must be done directly in the `.config/swdc/env` file like used image, hosts etc.

**FOLDER_NAME** has to be in uppercase. Example for image: Folder name is: **sw5**, VHOST_**SW5**_IMAGE

* VHOST_**FOLDER_NAME**_IMAGE
  * Allows changing the image that is used for this directory.
  * Files are mount to `/var/www/html`, the image should expose a web service at port 80
  * Possible default values can be found [here](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2F6%2Fnginx)
* VHOST_**FOLDER_NAME**_HOSTS
  * This can be a list of hosts comma separated. The first host will be used for the Installation
* VHOST_**FOLDER_NAME**_CERT_NAME
  * This can be used to define another SSL certificate for this vhost.
  * Example: `shop`. You will need following files  `~/.config/swdc/ssl/shop.crt` and `~/.config/swdc/ssl/shop.key`

### Enabling Blackfire

If you have enabled Blackfire in the Global Configuration, you have to enable it too for the actual project like:
```
VHOST_[FOLDER_NAME_UPPER_CASE]_IMAGE=ghcr.io/shyim/shopware-docker/6/nginx:php74-blackfire
```
in the `.config/swdc/env` file

### Enabling XDebug
XDebug needs to be enabled per Virtual Host. To enable it, open the SWDC configuration file (`$HOME/.config/swdc/env`) and add the following line:

```
VHOST_[FOLDER_NAME_UPPER_CASE]_IMAGE=ghcr.io/shyim/shopware-docker/6/nginx:php74-xdebug
```

After replacing your Folder Name and running `swdc up` XDebug should be activated.

To get XDebug started debugging, you need to enable it using the Chrome Extension: https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc. After this, you should get a debug request in your IDE.