# Hive Metastore Using Docker
This is a repository for a standalone Hive Metastore

Clone this repo: `git clone https://github.com/taeefnajib/Hive-Metastore-Using-Docker.git`

Inside `Hive-Metastore-Using-Docker` directory, take the following steps:
1. Edit conf/metastore-site.xml and change:
    * `fs.s3a.access.key`
    * `fs.s3a.secret.key`
    * `metastore.warehouse.dir`
2. Run the following commands in your terminal (in `Hive-Metastore-Using-Docker` directory):
    ```
    docker network create "hive_internal" 
    docker-compose build
	docker-compose up -d
    ```
The Hive Metastore should be up and running.

By default, the conf/metastore-site.xml file has `XXXXXXXXXXXXXXXXX` for `fs.s3a.access.key`, `XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX` for `fs.s3a.secret.key`, and `s3a://yourbucket/warehouse/` for `metastore.warehouse.dir`. Make sure to replace those.