---
title: 如何在Jupyter Notebook中使用Tensorflow
date: 2018-06-17 23:10:49
categories:
- Python
- 环境配置
tags:
- Python
- 环境配置
- Tensorflow
---
1. 打开终端
2. 运行下面的命令来启用TensorFlow source activate tensorflow
3. 现在我们已经进入了TensorFlow的环境，我们要在这个环境中安装iPython和jupyter，运行下面的命令conda install ipython以及conda install jupyter
4. 下面的步骤基本上按照Using a virtualenv in an IPython notebook中的进行，只是多加了一点内容。首先运行下面的命令，ipython kernelspec install-self --user,我这里得到的结果是Installed kernelspec python3 in /Users/charliebrummitt/Library/Jupyter/kernels/python3
5. 运行下边的命令mkdir -p ~/.ipython/kernels 
然后运行下边的命令，使用你选择的名字来代替<kernel_name>（我使用的tfkernel），并且使用第4步中得到的路径(例如，~/.local/share/jupyter/kernels/pythonX)来替换下方命令中的第一个路径。mv ~/.local/share/jupyter/kernels/pythonX ~/.ipython/kernels/<kernel_name>
6. 现在，打开Jupyter Notebook，选择Kernel -> Change kernel，你将看到一个新的kernel。但是，新的kernel与你之前的kernel拥有相同点名字，运行下边的命令，给你的新kernel起一个不同的名字。cd ~/.ipython/kernels/tfkernel/。接着，运行vim kernel.json来编辑kernel.json文件，将"display_name"中的默认值Python 3替换为你的新名字，然后保存，并退出。

来自 <http://blog.csdn.net/xue_wenyuan/article/details/51545845> 
