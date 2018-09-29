# Linux 配置安装 Apache Tomcat

## 1、下载Apache Tomcat 文件



## 2、创建文件安装目录

```
[root@localhost etc]# cd ~
[root@localhost ~]# cd /usr
[root@localhost usr]# mkdir tomcat
```

## 3、复制并解压文件

```
[root@localhost usr]# cp /home/centos/Downloads/apache-tomcat-8.5.33.tar.gz /usr/tomcat

[root@localhost usr]# tar zxvf apache-tomcat-8.5.33.tar.gz

[root@localhost tomcat]# rm apache-tomcat-8.5.33.tar.gz
rm: remove regular file `apache-tomcat-8.5.33.tar.gz'? y
[root@localhost tomcat]# ls
apache-tomcat-8.5.33
[root@localhost tomcat]# cd apache*
[root@localhost apache-tomcat-8.5.33]# 

```

## 4、配置文件


## 5、启动Tomcat

```
[root@localhost bin]# ./startup.sh
Using CATALINA_BASE:   /usr/tomcat/apache-tomcat-8.5.33
Using CATALINA_HOME:   /usr/tomcat/apache-tomcat-8.5.33
Using CATALINA_TMPDIR: /usr/tomcat/apache-tomcat-8.5.33/temp
Using JRE_HOME:        /usr/java/jdk1.8.0_181
Using CLASSPATH:       /usr/tomcat/apache-tomcat-8.5.33/bin/bootstrap.jar:/usr/tomcat/apache-tomcat-8.5.33/bin/tomcat-juli.jar
Tomcat started.
```
## 5、关闭Tomcat

```
[root@localhost bin]# ./shutdown.sh

Using CATALINA_BASE:   /usr/tomcat/apache-tomcat-8.5.33
Using CATALINA_HOME:   /usr/tomcat/apache-tomcat-8.5.33
Using CATALINA_TMPDIR: /usr/tomcat/apache-tomcat-8.5.33/temp
Using JRE_HOME:        /usr/java/jdk1.8.0_181
Using CLASSPATH:       /usr/tomcat/apache-tomcat-8.5.33/bin/bootstrap.jar:/usr/tomcat/apache-tomcat-8.5.33/bin/tomcat-juli.jar

```
