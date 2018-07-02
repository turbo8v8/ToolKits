# 装机必备列表

重装系统、换电脑、新虚拟机，一揽子解决，省的用到的时候再费时去弄。

## 命令行工具

1. ssh——这个真的不必说
1. zlib——压缩和解压缩工具
1. tree——以树形方式查看目录结构
1. curl——文件传输？还没试，期望能解决文件传输不便的问题。。。


## 不必说系列

1. **Git**：[https://git-scm.com/](https://git-scm.com/)
  - 图形化界面Git代码版本管理工具：https://www.sourcetreeapp.com/ 习惯了命令行不用也可。
1. **NodeJS**：[https://nodejs.org/en/](https://nodejs.org/en/)
1. **Python**：[https://www.python.org/](https://www.python.org/)
  - python3【配合pyenv多版本】
  - （Gzipped source tarball 和XZ compressed source tarball这两个选一个即可【不同的压缩方式而已】）
1. **VSCode**：[https://git-scm.com/](https://git-scm.com/)
1. **PostMan**：[https://www.getpostman.com/](https://www.getpostman.com/) 

## IDE或其他文本编辑器

1. PyCharm： https://www.jetbrains.com/pycharm/download/#section=linux
1. Sublime Text： http://www.sublimetext.com/

## 服务器常用

### PostgreSQL

``` shell
PostgreSQL 安装配置，简单版：
./configure
make
su   #切换到root用户
make install
adduser postgres #创建postgres账号专门给数据库用
mkdir /usr/local/pgsql/data
chown postgres /usr/local/pgsql/data #修改拥有者成数据库账号
su - postgres  #切换到postgres账号
/usr/local/pgsql/bin/initdb -D /usr/local/pgsql/data
初始化数据库详解：http://www.postgres.cn/docs/9.5/creating-cluster.html
/usr/local/pgsql/bin/postgres -D /usr/local/pgsql/data >logfile 2>&1 &
/usr/local/pgsql/bin/createdb test
/usr/local/pgsql/bin/psql test
修改配置文件之前设定的data目录下的postgresql.conf  设为监听特定地址、端口
修改配置文件之前设定的data目录下的pg_hba.conf  允许指定客户端通过指定方式接入
安装pgAdmin图形化工具：https://www.postgresql.org/ftp/pgadmin/pgadmin4/v1.4/windows/
```

### MongoDB

### Redis 

- 官网 http://redis.io/

### Nginx

- 官网：http://nginx.org/

``` shell
官网的安装方法就很好使，centos7安装很顺利没遇到任何问题。
To set up the yum repository for RHEL/CentOS, create the file named /etc/yum.repos.d/nginx.repo with the following contents:

[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/OS/OSRELEASE/$basearch/
gpgcheck=0
enabled=1
Replace “OS” with “rhel” or “centos”, depending on the distribution used, and “OSRELEASE” with “6” or “7”, for 6.x or 7.x versions, respectively.

还可以直接下载压缩包安装
https://www.cnblogs.com/taiyonghai/p/6728707.html

配置文件详解 https://my.oschina.net/hansonwang99/blog/1835408

解决Nginx出现403 forbidden (13: Permission denied)
https://blog.csdn.net/onlysunnyboy/article/details/75270533
```