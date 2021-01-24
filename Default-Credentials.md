## Which images and tags are available?

* [shopware/shopware-classic-nginx](https://hub.docker.com/r/shyim/shopware-classic-nginx/tags)
* [shopware/shopware-platform-nginx](https://hub.docker.com/r/shyim/shopware-platform-nginx/tags)
* [shopware/shopware-classic-apache](https://hub.docker.com/r/shyim/shopware-classic-apache/tags)
* [shopware/shopware-platform-apache](https://hub.docker.com/r/shyim/shopware-platform-apache/tags)
* [shopware/shopware-mysql](https://hub.docker.com/r/shyim/shopware-mysql/tags)
* [shopware/shopware-cli](https://hub.docker.com/r/shyim/shopware-cli/tags)

## Can I use PSH in this Setup?

* You can use `swdc shell` to enter the cli container
* Switch to your project `cd project`
* And run `./psh.phar command`

## How can I access the shop?

* You can use http://**FOLDERNAME**.dev.localhost
* Or use `swdc open [Folder Name]`

## Can I use it on Windows / Mac?

I use it regulary on Windows. I don't know so far no Mac Users

## What are the passwords?

### SMTP

MailDev: http://mail.localhost  
Host: smtp  
Port: 25  
no Login  
no Encryption  
no authetification

### MySQL

Host: mysql  
User: root  
Password: root  
PhpMyAdmin / Adminer: http://db.localhost

## ElasticSearch

Access es directly: http://es.localhost  
Access cerebro: http://cerebro.localhost

### Shopware 5

User: demo  
Password: demo

### Shopware 6

User: admin  
Password: shopware

### Minio (S3)

Host: minio 
Key: AKIAIOSFODNN7EXAMPLE  
Secret-Key: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY  
Bucket can be created on page http://localhost:9000/minio/