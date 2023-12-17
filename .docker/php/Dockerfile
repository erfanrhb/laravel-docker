FROM php:8.2-fpm
RUN docker-php-ext-install mysqli pdo pdo_mysql


# Install system dependencies
#RUN apt-get update && apt-get install -y \
#    curl\



#RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

RUN apt-get update
RUN apt-get install -y build-essential

RUN apt-get install -y libpng-dev

RUN apt-get install -y libjpeg62-turbo-dev

RUN apt-get install -y libfreetype6-dev

RUN apt-get install -y git

RUN docker-php-ext-install bcmath

RUN docker-php-ext-install bcmath


RUN docker-php-ext-install imagemagick


RUN docker-php-ext-install gd

#if you need gd and soap uncomment these two line.
#RUN apk add zlib-dev libpng-dev libxml2 libxml2-dev
#RUN docker-php-ext-install gd soap

COPY --from=composer /usr/bin/composer /usr/bin/composer

ENV COMPOSER_ALLOW_SUPERUSER 1
