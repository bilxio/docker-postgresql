# docker-postgresql

基于 [bitnami/postgresql](https://github.com/bitnami/bitnami-docker-postgresql/blob/master/13/debian-10/Dockerfile) 增加了以下插件：

- [pgsql-http 1.5.0](https://github.com/pramsey/pgsql-http)


## build

```bash
docker build -t bilxio/postgresql:13 -f 13-debian-10/Dockerfile .
```