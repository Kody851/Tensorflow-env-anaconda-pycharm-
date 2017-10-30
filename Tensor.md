[1]()、安装Anaconda(电脑为win7 64bit)

   下载：[https://www.continuum.io/downloads，我用的是历史版本Anaconda3 4.2.0](https://www.continuum.io/downloads，我用的是历史版本Anaconda3%204.2.0)（支持Python 3.5.3）。这是因为最新的Anaconda3 4.3.1默认安装的是python3.6.0, 而Tensorflow 对python3.6的支持还不够好。另外，目前Tensorflow还不支持windows系统下的python2.7。

安装完以后，从开始菜单打开Anaconda Prompt，输入python，若显示python版本信息，则安装成功。

接着，输入清华的仓库镜像，更新包下载速度更快：

conda config--add channels <https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/>回车

conda config--set show_channel_urls yes回车

2、配置Anaconda

打开Anaconda Prompt

依次点击：开始--所有程序--Anaconda这个窗口和doc窗口一样的，输入命令就可以控制和配置python，最常用的是conda命令，这个pip的用法一样，此软件都集成了，你可以直接用，点开的话如下图：

![http://upload-images.jianshu.io/upload_images/1888029-943f43b447a8eee5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image001.png)

**然后你可以使用conda命令进行一些包的安装和更新**

conda list

列出所有的已安装的packages

conda install name

name是需要安装packages的名字，比如，我安装numpy包，输入上面的命令就是：

conda install numpy

 

3、安装TensorFlow

继续打开Anaconda Prompt，输入：

condacreate -n tensorflow python=3.5

会出现安装信息，点回车进行确认，开始安装。

这时可以在开始菜单中搜索 anaconda navigator，点击运行；点击左侧的 Environments，可以看到 “tensorflow”的环境已经被创建了

安装完以后，输入：

activatetensorflow

激活后，我选择安装的是CPU版本，输入：

pipinstall --ignore-installed –upgrade <https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.0-cp35-cp35m-win_amd64.whl>回车

安装失败的话多试几次

 

3、测试

打开anaconda navigator，

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image003.jpg)

将application选为tensorflow，下方的spyder点install进行安装，之后点击Launch打开，输入import tensorflow as tf，没有报错，则tensorflow安装成功！

可输入下面的测试代码：

[#-*- coding: utf-8 -*-]()

importtensorflow as tf

sess =tf.InteractiveSession()

x = tf.Variable([1.0,2.0])

a =tf.constant([3.0, 3.0])

\# 使用初始化器 initializer op 的 run() 方法初始化 ‘x‘ 

x.initializer.run()

 

\# 增加一个减法 sub op, 从 ‘x‘ 减去 ‘a‘. 运行减法 op, 输出结果 

sub = tf.sub(x,a)

sub.eval()

\# ==> [-2.-1.]  

 

4、关闭

当你不用 TensorFlow 的时候,关闭环境:

  deactivate

 