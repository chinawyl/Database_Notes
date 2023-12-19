# 一、安装Zookeeper

### 1.上传安装包 

zookeeper-3.4.6.tar.gz	

### 2.解压

```shell
tar -zxvf zookeeper-3.4.6.tar.gz -C /usr/local/
```

### 3.创建数据存放目录

```shell
cd /usr/local/zookeeper-3.4.6/
mkdir data
```

### 4.修改配置文件名称并配置

```shell
cd config

mv zoo_sample.cfg zoo.cfg
```

### 5.配置数据存放目录

```shell
dataDir=/usr/local/zookeeper-3.4.6/data
```

### 6.启动Zookeeper

```shell
bin/zkServer.sh start

bin/zkServer.sh status
```

# 二、安装Mycat-web

### 1.上传安装包 

Mycat-web.tar.gz

### 2.解压

```shell
tar -zxvf Mycat-web.tar.gz -C /usr/local/
```

### 3.目录介绍

  ```tex
  etc         ----> jetty配置文件
  lib         ----> 依赖jar包
  mycat-web   ----> mycat-web项目
  start.jar   ----> 启动jar
  start.sh    ----> linux启动脚本
  ```

### 4.启动

```shell
sh start.sh
```

### 5.访问

http://192.168.200.210:8082/mycat	

> 备注: 
>
> 如果Zookeeper与Mycat-web不在同一台服务器上 , 需要设置Zookeeper的地址 ; 在**/usr/local/mycat-web/mycat-web/WEB-INF/classes/mycat.properties**文件中配置 : 
>
> ![001-不同服务器配置zookeeper](./images/001-不同服务器配置zookeeper.png)
