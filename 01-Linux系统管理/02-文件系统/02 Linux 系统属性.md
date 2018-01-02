
# 1、文件属性显示 TODO

```
[root@localhost /]# ls
bin   dev  home  lib64       media  opt   root  selinux  sys  usr
boot  etc  lib   lost+found  mnt    proc  sbin  srv      tmp  var


```
#2、文件属性

文件的属性共包含七列：

-文件权限

连接数

文件所有者

文件所属用户组

文件大小

文件最后被修改日期

文件名


## 2.1、第一列：文件的类型与权限

文件的类型与权限共有四组

第一组：第一个字符代表这个文件是“目录、文件或链接文件等”

[d]：表示目录
[-]：表示文件
[l]：表示链接文件（linkfile）
[b]：表示设备文件里面的可供存储的接口设备
[c]：表示设备文件里面的串行端口设备

第二组：文件所有者的权限

第三组：同用户组的权限

第四组：其他非本用户组的权限

