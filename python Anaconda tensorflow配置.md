## Python Anaconda 

Anaconda配置python环境非常方便，查阅了很多博客，终于配置成功，记录一下过程，以后配置的时候就不需要查阅太多博客，还各种失败。
本文使用Anaconda3 conda版本4.8.3 +python 3.7.6 tensorflow2.0

### 一、安装Anaconda3

[Anaconda 官网](https://www.anaconda.com/products/individual) 中选择要安装的Anaconda版本，一般是Windows64位，右键此电脑->属性，就可以看到自己的电脑是多少位的。选择python3.7安装，安装好之后，可以选择配置环境变量，否则pip无法运行。
测试一下，如果出现下图所示的版本号，就说明安装成功。

### 二、安装tensorflow

新建一个虚拟环境，打开Anaconda Prompt，输入以下命令行
``` markdown
conda create -n tensorflow python=3.7
```
tensorflow 指的是环境名称，可以更改，后面的python=3.7如果你已经在安装Anaconda时设置了默认3.7的python，就不需要加这句话，直接conda create -n tensorflow即可

创建完之后
``` markdown
conda activate tensorflow    //tensorflow指环境名称
```
