imdock
====================================================

## What's this:

Centos(Nginx + PHP5.6, PHP7.1), Mysql, Redis, Postgres, Mailcatcher, Mailhog

  * you can easy install PHP Framework (ex: Laravel)

  * you can use xdebug mode by PHPStorm(2016.2 or latest)

  * this project use management by docker-compose
  
  * you can use this for Laravel-5 PHP Framework
  
## How to choose the version:
 
  * if you use Docker Toolbox, You must choose Mysql (no volume), Because MariaDB can not use the mapping to mount the data
    
  * if you use Docker for windows, You must choose MariaDB (volume)
      
## How to install:

    imagi@DESKTOP-JJ9BJ2B ~/imdock $ git clone https://github.com/imagine10255/imdock.git

    imagi@DESKTOP-JJ9BJ2B ~/imdock $ cp ./cnp56/sites-enable/default.vhost ./sites-enable/mysite.vhost
    
    imagi@DESKTOP-JJ9BJ2B ~/imdock $ sh im.sh 
    
![imdock](https://github.com/imagine10255/imdock/blob/master/images/im.sh.jpg)


## How to change setting:

  * You just look at this directory you will understand (cnp56/config/* or cnp7/config/*)
    
  * When the settings are complete, restart the container
    
## PHP Extend:
- [x] PHP5.6
  - [x] mbstring
  - [x] mcrypt
  - [x] php-dom, php-domxml, php-wddx, php-xsl
  - [x] php-mysqli, php_database
  - [ ] mongodb
  - [ ] redis
  - [ ] pgsql
  - [x] php-mssql
  - [x] php56w-pdo_sqlite, php56w-sqlite3
  - [ ] apcu
  - [x] gd
  - [ ] imap  
  - [x] imagick
  - [x] zend-opcache
  - [x] memcache
  - [x] xdebug
  
- [x] PHP7
  - [x] mbstring
  - [x] mcrypt
  - [x] php-dom, php-domxml, php-wddx, php-xslxml, xmlrpc
  - [x] php-mysqli, php_database
  - [x] mongodb
  - [x] redis
  - [x] pgsql
  - [ ] php-mssql  
  - [x] php71w-pdo_sqlite, php71w-sqlite3
  - [x] apcu
  - [x] gd
  - [x] imap
  - [ ] imagick
  - [x] zend-opcache
  - [ ] memcache
  - [ ] xdebug

