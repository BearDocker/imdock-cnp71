imdock-cnp7
====================================================

## What's this:

Centos(Nginx + PHP7.1)

  * you can easy install PHP Framework (ex: Laravel)

  * you can use xdebug mode by PHPStorm(2016.2 or latest)

  * this project use management by docker-compose
  
  * you can use this for Laravel-5 PHP Framework

## How to install:

    ~ $ mkdir {project-name}
    ~ $ cd {project-name}
    ~/{project-name} $ git clone https://github.com/imagine10255/imdock-cnp7.git
    ~/{project-name} $ cd imdock-cnp7


#### change your custom settting (container_name: {project-name})

    ~/{project-name}/imdock-cnp7 $ vim ./docker-compose-yml
    ~/{project-name}/imdock-cnp7 $ docker-compose up
    
#### open browser, testing your host-ip, see the phpinfo is success! ctrl+c close this
#### now, you can move the your project to website dir
    
    ~/{project-name}/imdock-cnp7 $ cp ./sites-enable/default.vhost.sample ./sites-enable/default.vhost
    
#### setting your custom nginx config (volumes: ./website:/var/www → ../{project-dir}:/var/www)

    ~/{project-name}/imdock-cnp7 $ vim ./docker-compose-yml
    ~/{project-name}/imdock-cnp7 $ vim ./default.vhost
    ~/{project-name}/imdock-cnp7 $ docker-compose up -d


## Reference architecture:

```txt
{project-name}
├── imdock-cnp7
│   ├── conf/
│   ├── sites-enable/(nginx website setting)
│   ├── sites-module/
│   ├── website(sample phpinfo)
│   ├── Dockerfile
│   └── docker-compose.yml
└── {project-dir}
    └── ...
```
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

