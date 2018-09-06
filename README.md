# docker-base
Base NGINX, PHP, Panera and Friends

This image contains

+ NGINX
+ php-fpm 7
+ MySql
+ NodeJs 10.9
+ ELK (Elasticsearch, Logstash and Kibana)

This container is for a PHP projects..


## Requirements

Obviosly you need [Docker](https://www.docker.com/products/docker-desktop)

## How to build the image?

You should only run 

```$ ./develop build```

Then, you need start docker image

```$ ./develop start```

And, how stop the image?

```$ ./develop stop```

## How to run services?

+ Composer
    ```$ ./develop composer [command]```

+ phpunit
    ```$ ./develop test ```

+ npm
    ```$ ./develop npm [command] ```

+ ng (This is a test mode)
    ```$ ./develop ng [command] ```
