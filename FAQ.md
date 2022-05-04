## Which images and tags are available?

### Shopware 6
* [ghcr.io/shyim/shopware-docker/6/nginx](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2F6%2Fnginx)
* [ghcr.io/shyim/shopware-docker/6/apache](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2F6%2Fapache)

### Shopware 5
* [ghcr.io/shyim/shopware-docker/5/nginx](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2F5%2Fnginx)
* [ghcr.io/shyim/shopware-docker/5/apache](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2F5%2Fapache)

### Others

* [ghcr.io/shyim/shopware-docker/cli](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2Fcli)
* [ghcr.io/shyim/shopware-docker/mysql](https://github.com/shyim/shopware-docker/pkgs/container/shopware-docker%2Fmysql)

## Can I use PSH in this Setup?

* You can use `swdc shell` to enter the cli container
* Switch to your project `cd project`
* And run `./psh.phar command`

## How can I access the shop?

* You can use http://**FOLDERNAME**.dev.localhost
* Or use `swdc open [Folder Name]`
