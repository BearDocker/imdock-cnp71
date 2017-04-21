imdock-cnp7
====================================================

## What's this:

Centos(Nginx + PHP7.1)

  * you can easy install PHP Framework (ex: Laravel)

  * you can use xdebug mode by PHPStorm(2016.2 or latest)

  * this project use management by docker-compose
  
  * you can use this for Laravel-5 PHP Framework

## How to install:

    ~ $ git clone https://github.com/imagine10255/imdock-cnp7.git {your-project-name}
    ~ $ cd {your-project-name}
    
    # change your custom settting
    ~/{your-project-name} $ vim ./docker-compose-yml
    ~/{your-project-name} $ docker-compose up
    
    # open browser, testing your host-ip, see the phpinfo is success! ctrl+c close this
    # now, you can move the your project to website dir
    
    ~/{your-project-name} $ cp ./sites-enable/default.vhost.sample ./sites-enable/default.vhost
    
    # setting your custom nginx config
    ~/{your-project-name} $ vim ./default.vhost
    ~/{your-project-name} $ docker-compose up -d
            
            
## How to and other docker-compose use the same network :

    #if you not have group network, you can create this, and other docker-compose use this network setting
    ~ $ docker network create --driver bridge imdockgroup
    
## How to change setting:

  * You just look at this directory you will understand (cnp7/config/*)
    
  * When the settings are complete, restart the container
    
## PHP Extend:

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

