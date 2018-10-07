# docker-sample
## php-nginx-mysqlのdocker-sample
nginx部分をApacheに変えればそのまま使えるはず…

## 構成
    ./
    ├── contents
    │   └── {pj-source-path}
    ├── docker-compose.yml
    ├── mysql
    │   └── {import-sql}
    ├── nginx
    │   ├── Dockerfile
    │   ├── default.conf
    │   └── nginx.conf
    └── php
        └── Dockerfile

## 解説
- docker-compose.yml
    - 読んで

- contents-{pj-source-path}
    - PJのソースファイル配置先

- mysql-{import-sql}
    - DBにインサートするdump(SQL)ファイル置き場

- nginx/*
    - nginxで使用するconfファイルとDockerfile置き場（~~Dockerfileはcompose側でimage直指定でもOK~~）

- php/*
    - Dockerfile置き場（~~Dockerfileは（ry~~）

## 使い方
1. `git clone {docker-sample URL}`
1. `docker-compose up -d`

## 停止方法
    docker-compose stop

## 起動方法
    docker-compose start

## 停止後に削除
    docker-compose down
