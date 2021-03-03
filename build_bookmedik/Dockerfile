FROM php:7.4-apache
MAINTAINER Juan Antonio Reifs Ramirez "initiategnat9@gmail.com"

RUN apt-get update && apt-get install -y git && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/evilnapsis/bookmedik /var/www/html
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

ADD Database.php /var/www/html/core/controller

EXPOSE 80

ENV DATABASE_SERVER=book_sql MYSQL_ROOT_PASSWORD=root MYSQL_USER=book_user MYSQL_PASSWORD=book_passwd MYSQL_DATABASE=bookmedik
