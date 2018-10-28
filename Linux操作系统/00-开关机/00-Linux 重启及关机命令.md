# Linux 重启及关机命令

## 1、关机

```
--立即关机
[root@localhost ~]# halt

--立即关机
[root@localhost ~]# poweroff

--立即关机
[root@localhost ~]# shutdown -h now

--10分钟后关机
[root@localhost ~]# shutdown -h 10

--定时关机
[root@localhost ~]# shutdown -h 20:30 "shutdown ..."

Broadcast message from centos@localhost.localdomain
	(/dev/pts/0) at 16:37 ...

The system is going down for halt in 233 minutes!
shutdown ... 



```

## 2、重启
```
-- 立即重启
[root@localhost ~]# reboot

-- 立即重启
[root@localhost ~]# shutdown -r now

-- 定时重启
[root@localhost ~]# shutdown -r 10

-- 定时重启
[root@localhost ~]# shutdown -r 20:30

```

## 3、取消关机
```
[root@localhost ~]# shutdown -r now
shutdown: Another shutdown is already running
[root@localhost ~]# shutdown -c
```