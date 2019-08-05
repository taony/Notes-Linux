# Linux 安装 JDK

## 1、使用root账号登录

使用root账号登录，或者通过sudo命令切换到root账号。

## 2、创建安装目录
切换到usr目录，

```
//切换到 usr 目录
[root@localhost ~]# cd /usr
[root@localhost usr]# 

//创建 java 目录
[root@localhost usr]# mkdir java

```
## 3、复制安装文件到 Java 安装目录

```
[root@localhost usr]# cp /home/centos/Downloads/jdk-8u181-linux-x64.tar.gz /usr/java

[root@localhost usr]# cd java
[root@localhost java]# ls
jdk-8u181-linux-x64.tar.gz
[root@localhost java]# 
```

## 4、解压安装文件

```
[root@localhost java]# tar -zxvf jdk-8u181-linux-x64.tar.gz

[root@localhost java]# ls -l
total 181300
drwxr-xr-x. 7 uucp  143      4096 Jul  7 01:09 jdk1.8.0_181
-rwxr--r--. 1 root root 185646832 Aug 23 04:07 jdk-8u181-linux-x64.tar.gz
```
## 5、编辑配置文件

```
[root@localhost etc]# vi /etc/profile

JAVA_HOME=/usr/java/jdk1.8.0_181
CLASSPATH=$JAVA_HOME/lib/
PATH=$PATH:$JAVA_HOME/bin
export PATH JAVA_HOME CLASSPATH

```

## 6、使文件生效

```
[root@localhost etc]# source /etc/profile

//重启命令：sudo shutdown -r now
```


## 7、验证安装

```
[root@localhost etc]# java -version
java version "1.8.0_181"
Java(TM) SE Runtime Environment (build 1.8.0_181-b13)
Java HotSpot(TM) 64-Bit Server VM (build 25.181-b13, mixed mode)
```


