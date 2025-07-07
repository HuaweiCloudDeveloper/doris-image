# Doris部署指南

## ‌一、环境准备

### 更新系统

```bash
yum -y update  
yum -y upgrade
```

## ‌二、下载安装包
```bash
cd /opt
wget https://apache-doris-releases.oss-accelerate.aliyuncs.com/apache-doris-2.1.10-bin-arm64.tar.gz
# 解压
tar -zxf apache-doris-2.1.10-bin-arm64.tar.gz 
mv apache-doris-2.1.10-bin-arm64 doris-2.1.10
```
## 安装 Doris

### 配置 FE
FE 的配置文件为 apache-doris/fe/conf/fe.conf。下面是一些需要关注的核心配置。除了 JAVA_HOME, 需要手动增加，并且指向你的 JDK8 运行环境。其它配置，可以使用默认值，即可支持单机快速体验。
```bash
# 增加 JAVA_HOME 配置，指向 JDK8 的运行环境。假如我们 JDK8 位于 /home/doris/jdk8, 则设置如下
JAVA_HOME=/home/doris/jdk8

# FE 监听 IP 的 CIDR 网段。默认设置为空，有 Apache Doris 启动时自动选择一个可用网段。如有多个网段，需要指定一个网段，可以类似设置 priority_networks=192.168.0.0/24
# priority_networks =

# FE 元数据存放的目录，默认是在 DORIS_HOME 下的 doris-meta 目录。已经创建，可以更改为你的元数据存储路径。
# meta_dir = ${DORIS_HOME}/doris-meta
```

### 启动 FE
在 apache-doris/fe 下，运行下面命令启动 FE。
```bash 
# 将 FE 启动成后台运行模式，这样确保退出终端后，进程依旧运行。
server1:apache-doris/fe doris$ ./bin/start_fe.sh --daemon
```

### 配置 BE
BE 的配置文件为 apache-doris/be/conf/be.conf。下面是一些需要关注的核心配置。除了 JAVA_HOME, 需要手动增加，并且指向你的 JDK8 运行环境。其它配置，可以使用默认值，即可支持我们的快速体验。
```bash

# 增加 JAVA_HOME 配置，指向 JDK8 的运行环境。假如我们 JDK8 位于 /home/doris/jdk8, 则设置如下
JAVA_HOME=/home/doris/jdk8

# BE 监听 IP 的 CIDR 网段。默认设置为空，有 Apache Doris 启动时自动选择一个可用网段。如有多个网段，需要指定一个网段，可以类似设置 priority_networks=192.168.0.0/24
# priority_networks =

# BE 数据存放的目录，默认是在 DORIS_HOME 下的 storage 下，默认已经创建，可以更改为你的数据存储路径
# storage_root_path = ${DORIS_HOME}/storage
```

### 启动 BE

在 apache-doris/be 下，运行下面命令启动 BE。

```shell
# 将 BE 启动成后台运行模式，这样确保退出终端后，进程依旧运行。
server1:apache-doris/be doris$ ./bin/start_be.sh --daemon
```
参考：[Doris快速体验](https://doris.incubator.apache.org/zh-CN/docs/2.0/gettingStarted/quick-start)

