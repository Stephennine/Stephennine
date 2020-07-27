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
会出现如下的界面


然后，安装tensorflow，输入
``` markdown
conda install tensorflow   
```
现在装的有CPU和GPU版本，要使用GPU，还要安装cuda和cudnn
安装好之后，打开Anaconda Navigator，点击Environment ，切换到tensorflow环境，再到Home页面，install一下jupter Notebook，安装完之后打开，输入
``` markdown
import tensorflow as tf
```
如果成功，则不会报“No Module Name ‘tensorflow’”，否则就检查一下是否是环境没有切换，或者下载tensorflow时有问题。

### 三、Pycharm配置
安装好Pycharm后，点击 File->Setting->Project->Project Interpreter,点击主界面右边的一齿轮，点击出来的Add，然后选择Anaconda下刚刚配置好的文件夹下的python执行文件，就可以将导入好的包导入到pycharm中，非常方便，然后就可以使用了。
Pycharm可以灵活切换Anaconda中的环境，不想用tensorflow时，就转换回base下的python，如果有其它环境，导入即可，各个环境相互独立，满足不同需求。


    
