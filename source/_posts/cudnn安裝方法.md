---
title: cudnn安裝方法
date: 2018-06-18 00:05:25
categories:
- Python
- 环境配置
tags:
- Python
- Tensorflow
- 环境配置
---
``` bash
$ sudo cp cuda/include/cudnn.h /usr/local/cuda/include 
$ sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64 
$ sudo chmod a+r /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*
```
来自 <http://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html> 

