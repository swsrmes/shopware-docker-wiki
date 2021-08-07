In this guide, I will show you how to spawn a second MySQL container. It is possible to spawn anything you want.

Create a new file `$HOME/.config/swdc/services.yml` with

```yml
version: '3.9'
services:
  mysql8:
    image: mysql:8
    environment:
      MYSQL_ROOT_PASSWORD: root
    volumes:
      - mysql8-data:/var/lib/mysql
    command: ["mysqld", "--default-authentication-plugin=mysql_native_password"]
volumes:
  mysql8-data:
```

Run `swdc up` and we have a second MySQL Container