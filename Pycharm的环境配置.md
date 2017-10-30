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

输出结果：

F:\Anaconda\envs\tensorflow\python.exe F:/pycharm/PycharmProjects/new0/tf_test.py
2017-10-30 22:35:27.953239: W c:\tf_jenkins\home\workspace\release-win\device\cpu\os\windows\tensorflow\core\platform\cpu_feature_guard.cc:45] The TensorFlow library wasn't compiled to use SSE instructions, but these are available on your machine and could speed up CPU computations.
2017-10-30 22:35:27.954240: W c:\tf_jenkins\home\workspace\release-win\device\cpu\os\windows\tensorflow\core\platform\cpu_feature_guard.cc:45] The TensorFlow library wasn't compiled to use SSE2 instructions, but these are available on your machine and could speed up CPU computations.
2017-10-30 22:35:27.954240: W c:\tf_jenkins\home\workspace\release-win\device\cpu\os\windows\tensorflow\core\platform\cpu_feature_guard.cc:45] The TensorFlow library wasn't compiled to use SSE3 instructions, but these are available on your machine and could speed up CPU computations.
2017-10-30 22:35:27.954240: W c:\tf_jenkins\home\workspace\release-win\device\cpu\os\windows\tensorflow\core\platform\cpu_feature_guard.cc:45] The TensorFlow library wasn't compiled to use SSE4.1 instructions, but these are available on your machine and could speed up CPU computations.
2017-10-30 22:35:27.955240: W c:\tf_jenkins\home\workspace\release-win\device\cpu\os\windows\tensorflow\core\platform\cpu_feature_guard.cc:45] The TensorFlow library wasn't compiled to use SSE4.2 instructions, but these are available on your machine and could speed up CPU computations.
b'Hello, TensorFlow!'

Process finished with exit code 0