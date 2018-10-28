# 1、ls: 查看目录

   

- -a ：全部的文件，连同隐藏档( 开头为 . 的文件) 一起列出来(常用)
- -d ：仅列出目录本身，而不是列出目录内的文件数据(常用)
- -l ：长数据串列出，包含文件的属性与权限等等数据；(常用)


# 2、cd：切换目录

cd是Change Directory的缩写，这是用来变换工作目录的命令。


```
#使用 mkdir 命令创建 runoob 目录
[root@www ~]# mkdir runoob
    
#使用绝对路径切换到 runoob 目录
[root@www ~]# cd /root/runoob/
    
#使用相对路径切换到 runoob 目录
[root@www ~]# cd ./runoob/

# 表示回到自己的家目录，亦即是 /root 这个目录
[root@www runoob]# cd ~
    
# 表示去到目前的上一级目录，亦即是 /root 的上一级目录的意思；
[root@www ~]# cd ..
```

    

# 3、pwd：显示目前的目录

#显示当前目录
    
```
TaonyMacBook:~ taony$ pwd
/Users/taony
```

# 4、mkdir：创建新目录

- 创建一个或多个新目录,mkdir命令后面跟着要创建的目录名称。
```
TaonyMacBook:Documents taony$ mkdir dir_test
TaonyMacBook:Documents taony$ ls -al
total 48
drwx------+  8 taony  staff    256 10 28 00:02 .
drwxr-xr-x+ 37 taony  staff   1184 10 27 23:55 ..
-rw-r--r--@  1 taony  staff   8196  6 13 23:32 .DS_Store
-rw-r--r--   1 taony  staff      0  6  6 00:22 .localized
-rw-r--r--   1 taony  staff  12288  6 13 23:12 .taony.txt.swp
drwxr-xr-x   6 taony  staff    192  6  7 23:45 GitHub
drwxr-xr-x   3 taony  staff     96  6  8 07:48 Xcode
drwxr-xr-x   2 taony  staff     64 10 28 00:02 dir_test
TaonyMacBook:Documents taony$ 
```
- 创建多级目录：mkdir的-p选项允许你一次性创建多层次的目录，而不是一次只创建单独的目录。

```
TaonyMacBook:Documents taony$ mkdir -p dir_test/2th/3th
TaonyMacBook:Documents taony$ ls
GitHub		Xcode		dir_test
TaonyMacBook:Documents taony$ cd dir_test
TaonyMacBook:dir_test taony$ ls
2th
TaonyMacBook:dir_test taony$ cd 2th
TaonyMacBook:2th taony$ ls
3th
```
- 创建多层目录：同时创建多个文件夹，每个文件夹里面分别有一个src文件目录。

```
TaonyMacBook:Documents taony$ mkdir -p dir_test/{a,b,c,d}/src
TaonyMacBook:Documents taony$ 
```
# 5、rmdir：删除目录

```
TaonyMacBook:Documents taony$ mkdir rmdir_test
TaonyMacBook:Documents taony$ ls -l
total 0
drwxr-xr-x  6 taony  staff  192  6  7 23:45 GitHub
drwxr-xr-x  3 taony  staff   96  6  8 07:48 Xcode
drwxr-xr-x  7 taony  staff  224 10 28 00:10 dir_test
drwxr-xr-x  2 taony  staff   64 10 28 00:12 rmdir_test
TaonyMacBook:Documents taony$ rmdir rmdir_test
TaonyMacBook:Documents taony$ ls -l
total 0
drwxr-xr-x  6 taony  staff  192  6  7 23:45 GitHub
drwxr-xr-x  3 taony  staff   96  6  8 07:48 Xcode
drwxr-xr-x  7 taony  staff  224 10 28 00:10 dir_test
TaonyMacBook:Documents taony$ 
```

强制删除非空目录

```
TaonyMacBook:Documents taony$ ls
GitHub		Xcode		dir_test	rmdir_test
TaonyMacBook:Documents taony$ rmdir rmdir_test
rmdir: rmdir_test: Directory not empty
TaonyMacBook:Documents taony$ rm -rf rmdir_test
TaonyMacBook:Documents taony$ ls
GitHub		Xcode		dir_test
TaonyMacBook:Documents taony$
```

# 6、cp: 复制文件或目录

```
TaonyMacBook:Documents taony$ mkdir dir1 dir2
TaonyMacBook:Documents taony$ ls
GitHub	Xcode	dir1	dir2
TaonyMacBook:Documents taony$ cd dir1
TaonyMacBook:dir1 taony$ ls
TaonyMacBook:dir1 taony$ touch dir1.txt
TaonyMacBook:dir1 taony$ cd ..
TaonyMacBook:Documents taony$ cd dir2
TaonyMacBook:dir2 taony$ touch dir2.txt
TaonyMacBook:dir2 taony$ cp dir1 dir2
cp: dir1: No such file or directory
TaonyMacBook:dir2 taony$ cp dir1 dir2
cp: dir1: No such file or directory
TaonyMacBook:dir2 taony$ cp -r dir1 dir2
cp: dir1: No such file or directory
TaonyMacBook:dir2 taony$ ls
dir2.txt
TaonyMacBook:dir2 taony$ cd ..
TaonyMacBook:Documents taony$ ls
GitHub	Xcode	dir1	dir2
TaonyMacBook:Documents taony$ cp -r dir1 dir2
TaonyMacBook:Documents taony$ ls
GitHub	Xcode	dir1	dir2
TaonyMacBook:Documents taony$ cd dir1
TaonyMacBook:dir1 taony$ ls
dir1.txt
TaonyMacBook:dir1 taony$ cd ..
TaonyMacBook:Documents taony$ cd dir2
TaonyMacBook:dir2 taony$ ls
dir1		dir2.txt
```
___
```
复制文件选项：
-a：此选项通常在复制目录时使用，它保留链接、文件属性，并复制目录下的所有内容。其作用等于dpR参数组合。
-d：复制时保留链接。这里所说的链接相当于Windows系统中的快捷方式。
-f：覆盖已经存在的目标文件而不给出提示。
-i：与-f选项相反，在覆盖目标文件之前给出提示，要求用户确认是否覆盖，回答"y"时目标文件将被覆盖。
-p：除复制文件的内容外，还把修改时间和访问权限也复制到新文件中。
-r：若给出的源文件是一个目录文件，此时将复制该目录下所有的子目录和文件。
-l：不复制文件，只是生成链接文件。
```

# 7、rm: 移除文件或目录

(1)移除多个文件目录

```
TaonyMacBook:Documents taony$ ls
GitHub	Xcode	dir1	dir2	dir3
TaonyMacBook:Documents taony$ rm -r dir1 dir2 dir3
TaonyMacBook:Documents taony$ ls
GitHub	Xcode
```
(2) 移除非空文件夹

```
TaonyMacBook:Documents taony$ mkdir dir4
TaonyMacBook:Documents taony$ cd dir4
TaonyMacBook:dir4 taony$ ls
TaonyMacBook:dir4 taony$ touch 1.txt 2.txt
TaonyMacBook:dir4 taony$ cd ..
TaonyMacBook:Documents taony$ ls
GitHub	Xcode	dir4
TaonyMacBook:Documents taony$ rm dir4
rm: dir4: is a directory
TaonyMacBook:Documents taony$ rm -rf dir4
TaonyMacBook:Documents taony$ ls
GitHub	Xcode
```
