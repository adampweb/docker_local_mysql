# Private MySQL Database Server

## Introduction

This build in not contain Dockerfile because the [official image](https://hub.docker.com/_/mysql)
is currently enough for me.

## Configuration

I attached an [optimized **my.cnf** config file (created by Fotis Evangelou)](https://gist.github.com/fevangelou/fb72f36bbe333e059b66) to container. Some other secret
configuration options set in an **.env** file (of course this in not a part of this repo for privacy reasons )

## Modifications

* The default image not contain any text editor therefore after create the container
and enter into and install [nano editor](https://www.nano-editor.org/).
* The custom config files permissions my not be correct and must be change to **0444**.

## Networking

This database container available at **172.18.0.4** IP-address or **mysql.dev.home** hostname.