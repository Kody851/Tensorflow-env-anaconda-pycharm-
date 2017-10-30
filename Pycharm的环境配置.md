# Pycharm的环境配置

## 1、安装

安装专业版，然后百度“激活码”即可。

## 2、配置TF

* 设置好pycharm下解释器interpreter的路径

file》》setting》》Project helloworld 》》Project Interpreter

路径选择F:\Anaconda\envs\tensorflow\python.exe 点击OK

即Anaconda环境下的tensorflow。

* 测试一下

  新建工程，解释器选择上述。

  进入一个交互式 TensorFlow 会话.

  ```
  import tensorflow as tf
  hello = tf.constant('Hello, TensorFlow!')
  sess = tf.Session()
  print(sess.run(hello))
  ```