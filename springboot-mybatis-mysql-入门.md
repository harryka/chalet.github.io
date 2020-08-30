# SpringBoot微服务开发入门

## Spring Boot 简介
### Spring Boot VSCode配置
### Spring Boot创建
### VSCode创建完成后修改SpringBoot依赖

## Mybatis简介

### Mybatis使用

### Mybatis generator功能和使用

## Mysql简介

## Docker部署Mysql
### 部署命令
```
docker pull mysql:5.7
docker run -p 33060:3306 --name harry-mysql -e MYSQL_ROOT_PASSWORD=12345678 -d mysql:5.7
mysql -u root -p12345678 < /config_script/createdb.sql
docker exec -it harry-mysql-01 sh -c "mysql -u root -p12345678 < /config_script/createdb.sql"
```
### 测试mysql链接
vscode中安装MySQL插件-- MySQL management tool
在Explorer的MYSQL项目中点击加号，根据向导添加数据源，其中端口号把3306改成33060
在MYSQL中就显示出默认的database了

### 创建数据库

sql语句创建表时，VARCHAR需要制定长度，否则语法检查不过

## lombok简介

## lombok使用



## 参考资料
- [docker hub mysql](https://hub.docker.com/_/mysql)
- [lombok Home Page](https://projectlombok.org/)