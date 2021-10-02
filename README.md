# Private MySQL Database Server

## Introduction

~~This build in not contain Dockerfile because the [official image](https://hub.docker.com/_/mysql)
is currently enough for me.~~

**UPDATE:** I extended this environment with customized [Nginx](https://github.com/adampweb/docker_local_nginx) and [PHP-FPM](https://github.com/adampweb/docker_local_php) container configurations 
for using [phpMyAdmin](https://www.phpmyadmin.net/) DBMS.

## Configuration

I attached an [optimized **my.cnf** config file (created by Fotis Evangelou)](https://gist.github.com/fevangelou/fb72f36bbe333e059b66) to container. Some other secret
configuration options set in an **.env** file (of course this in not a part of this repo for privacy reasons )

## Modifications

* The default image not contain any text editor therefore after create the container
and enter into and install [nano editor](https://www.nano-editor.org/).
* The custom config files permissions my not be correct and must be change to **0444**.

## Networking

This database container available at **172.18.0.4** IP-address or **db.dev.home** domain. The user interface (Nginx container) available at the **phpmyadmin.dev.home** domain.

## Usage

The phpMyAdmin user interface is accessible by phpmyadmin.dev.home private domain.
![phpMyAdmin graphical user interface](https://upload.wikimedia.org/wikipedia/commons/1/13/PhpMyAdmin-main-en.png)