# 1、ls: 查看目录

   

- -a ：全部的文件，连同隐藏档( 开头为 . 的文件) 一起列出来(常用)
- -d ：仅列出目录本身，而不是列出目录内的文件数据(常用)
- -l ：长数据串列出，包含文件的属性与权限等等数据；(常用)


# 2、cd：切换目录

cd是Change Directory的缩写，这是用来变换工作目录的命令。

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
    

# 3、pwd：显示目前的目录

    #显示当前目录



# 4、mkdir：创建一个新的目录


# 5、rmdir：删除一个空的目录


# 6、cp: 复制文件或目录


# 7、rm: 移除文件或目录