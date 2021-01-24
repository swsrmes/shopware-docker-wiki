XDebug needs to be enabled per Virtual Host. To enable it open the swdc configuration file (`$HOME/.config/swdc/env`) and add the following line:

```
VHOST_[FOLDER_NAME_UPPER_CASE]_IMAGE=ghcr.io/shyim/shopware-docker/6/nginx:php74-xdebug
```

After replacing your Folder Name and running `swdc up` XDebug should be activated.

To get XDebug started debugging you need to enable it using the Chrome Extension: https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc . After this you should get a debug request in your IDE.