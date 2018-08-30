# docker-base
Base NGINX, PHP, Symfony and Friends

This image contains

+ NGINX
+ php-fpm 7
+ MySql
+ NodeJs 10.9
+ ELK (Elasticsearch, Logstash and Kibana)

This container is for a PHP projects, if you see some files or directories named `symfony` don't worry, is only for deploy image.

Some features like logs is focus in Symfony but it does not matter, the images work very well!

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
