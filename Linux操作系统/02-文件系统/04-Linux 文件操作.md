## 1、创建文件

touch命令有两个功能：一是用于把已存在文件的时间标签更新为系统当前的时间（默认方式），它们的数据将原封不动地保留下来；二是用来创建新的空文件。

```
TaonyMacBook:Documents taony$ mkdir file-test
TaonyMacBook:Documents taony$ cd file-test
TaonyMacBook:file-test taony$ touch 1.txt 2.txt 3.doc
TaonyMacBook:file-test taony$ ls -l
total 0
-rw-r--r--  1 taony  staff  0 10 28 00:57 1.txt
-rw-r--r--  1 taony  staff  0 10 28 00:57 2.txt
-rw-r--r--  1 taony  staff  0 10 28 00:57 3.doc
TaonyMacBook:file-test taony$ touch 3.doc
TaonyMacBook:file-test taony$ ls -al
total 0
drwxr-xr-x  5 taony  staff  160 10 28 00:57 .
drwx------+ 9 taony  staff  288 10 28 00:57 ..
-rw-r--r--  1 taony  staff    0 10 28 00:57 1.txt
-rw-r--r--  1 taony  staff    0 10 28 00:57 2.txt
-rw-r--r--  1 taony  staff    0 10 28 01:00 3.doc
```

## 2、复制文件


```
语法
cp [options] source dest
或
cp [options] source... directory

参数说明：
-a：此选项通常在复制目录时使用，它保留链接、文件属性，并复制目录下的所有内容。其作用等于dpR参数组合。
-d：复制时保留链接。这里所说的链接相当于Windows系统中的快捷方式。
-f：覆盖已经存在的目标文件而不给出提示。
-i：与-f选项相反，在覆盖目标文件之前给出提示，要求用户确认是否覆盖，回答"y"时目标文件将被覆盖。
-p：除复制文件的内容外，还把修改时间和访问权限也复制到新文件中。
-r：若给出的源文件是一个目录文件，此时将复制该目录下所有的子目录和文件。
-l：不复制文件，只是生成链接文件。
```

```
TaonyMacBook:cp_test taony$ cp dir1/* dir2

TaonyMacBook:dir1 taony$ cp 1.txt ../dir2/1.txt
TaonyMacBook:dir1 taony$ cp -i 1.txt ../dir2/1.txt
overwrite ../dir2/1.txt? (y/n [n]) y
```

## 3、移动文件
Linux mv命令用来为文件或目录改名、或将文件或目录移入其它位置。


```
语法
mv [options] source dest
mv [options] source... directory

参数说明：
-i: 若指定目录已有同名文件，则先询问是否覆盖旧文件;
-f: 在mv操作要覆盖某已有的目标文件时不给任何指示;
```

1、移动文件
```
TaonyMacBook:cp_test taony$ cd dir1
TaonyMacBook:dir1 taony$ ls
1.txt	2.txt	3.doc
TaonyMacBook:dir1 taony$ mv 1.txt 5.d
TaonyMacBook:dir1 taony$ ls
2.txt	3.doc	5.d
```
2、移动文件夹
```
TaonyMacBook:dir2 taony$ ls
1.txt	2.txt	3.txt
TaonyMacBook:dir2 taony$ cd ..
TaonyMacBook:cp_test taony$ mv dir1 dir2
TaonyMacBook:cp_test taony$ ls
dir2
```

## 4、删除文件

Linux rm 命令用于删除文件或者目录。
```
语法
rm [options] name...

参数：
-i 删除前逐一询问确认。
-f 即使原档案属性设为唯读，亦直接删除，无需逐一确认。
-r 将目录及以下之档案亦逐一删除。
```
删除文件可以直接使用rm命令，若删除目录则必须配合选项"-r"

