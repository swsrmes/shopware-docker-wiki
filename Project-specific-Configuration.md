* You can override the image, hosts and the used SSL certificate
* **FOLDER_NAME** has to be in uppercase. Example for image: Folder name is: **sw5**, VHOST_**SW5**_IMAGE

* VHOST_**FOLDER_NAME**_IMAGE
  * Allows changing the image that is used for this directory.
  * Files are mount to /var/www/html, the image should expose a web service at port 80
* VHOST_**FOLDER_NAME**_HOSTS
  * This can be a list of hosts comma separated. The first host will be used for the Installation
* VHOST_**FOLDER_NAME**_CERT_NAME
  * This can be used to define another SSL certificate for this vhost.
  * Example: `shop`. You will need following files  `~/.config/swdc/ssl/shop.crt` and `~/.config/swdc/ssl/shop.key`