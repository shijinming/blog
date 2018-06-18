---
title: PYTHON对文件及文件夹的一些操作
date: 2018-06-17 22:54:48
categories:
- Python
- 文件操作
tags: 
- Python
- 文件操作
---
python中对文件、文件夹的操作需要涉及到os模块和shutil模块。

创建文件：
``` python
os.mknod("test.txt")  # 创建空文件
open("test.txt",w)          # 直接打开一个文件，如果文件不存在则创建文件
```
创建目录：
```  python
os.mkdir("file")                  # 创建目录
```
复制文件：
``` python
shutil.copyfile("oldfile","newfile")      # oldfile和newfile都只能是文件
shutil.copy("oldfile","newfile")          #  oldfile只能是文件夹，newfile可以是文件，也可以是目标目录
```
复制文件夹：
``` python
shutil.copytree("olddir","newdir")      # olddir和newdir都只能是目录，且newdir必须不存在
```
重命名文件（目录）
``` python
os.rename("oldname","newname")       # 文件或目录都是使用这条命令
```
移动文件（目录）
``` python
shutil.move("oldpos","newpos")    
```
删除文件
``` python
os.remove("file")
```
删除目录
``` python
os.rmdir("dir")  # 只能删除空目录
shutil.rmtree("dir")   # 空目录、有内容的目录都可以删 
```
转换目录
``` python
os.chdir("path")   # 换路径
```
判断目标
``` python
os.path.exists("goal")    # 判断目标是否存在
os.path.isdir("goal")    # 判断目标是否目录
os.path.isfile("goal")    # 判断目标是否文件   
```
来自 <http://www.cnblogs.com/phoebus0501/archive/2011/01/19/1939646.html> 

