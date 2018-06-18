---
title: 远程连接Jupyter Notebook配置
date: 2018-06-17 23:08:23
categories:
- Python
- 环境配置
tags:
- Python
- 环境配置
---
Step-1: 在远程服务器上，启动jupyter notebooks服务：
``` bash
jupyter notebook --no-browser --port=8889
```
Step-2: 在本地机器的Terminal中启动SSH：
``` bash
ssh -N -f -L localhost:8888:localhost:8889 remote_user@remote_host
```
其中： -N 告诉SSH没有命令要被远程执行； -f 告诉SSH在后台执行； -L 是指定port forwarding的配置，远端端口是8889，本地的端口号的8888。remote_user@remote_host 用实际的远程帐户和远程地址替换


Step-3: 打开浏览器，输入地址：http://localhost:8888/

来自 <http://blog.csdn.net/patrick75/article/details/51473884> 
