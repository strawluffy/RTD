**************
开始sphinx之旅
**************


安装部署sphinx
================

windows 安装方式
----------------

安装部署python
~~~~~~~~~~~~~~~~

   直接从官方网站上下载最新版本的python进行安装，本文使用python2.7.6版本。

安装pip
~~~~~~~~~~
   
   下载 `get-pip.py <https://bootstrap.pypa.io/get-pip.py>`_ 文件，并执行下面的命令::

   > python get-pip.py

   这样pip就安装成功了。


安装sphinx
~~~~~~~~~~~~~~~

   之后新建一个你自己的工程目录，之后进入目录，并在这里面执行建立你的sphinx工程命令：sphinx-quickstart::

   >mkdir example
   >cd example
   >sphinx-quickstart

   之后根据提示的信息填写，基本的信息如：工程目录的名称，项目名称，版本起始数字等等。


linux 安装方式
----------------



.. note::
   
   This tutorial should be read side-by-side with the Sphinc source
   for this document because otherwise
   you will see only the rendered output and not the code that
   generated it.  Excepting the example above, we will not in general
   be showing the liuteral rest in this document that generates the
   rendered output.

工程目录列表介绍
=================

   新建成的目录结构如下::

      example
      --Makefile
      --_build
      --_static
      --__templates
      --conf.py
      --index.rst


   解释一下上面的这些文件的作用：

   #. Makefile 编译过代码的开发人员应该非常熟悉这个文件，如果不熟悉，那么可以将它看作是一个包含指令的文件，在使用 make 命令时，可以使用这些指令来构建文档输出。
   #. _build 这是触发特定输出后用来存放所生成的文件的目录。
   #. _static：所有不属于源代码（如图像）一部分的文件均存放于此处，稍后会在构建目录中将它们链接在一起。
   #. _templates: 用于存储一些模板文件。
   #. conf.py：这是一个 Python 文件，用于存放 Sphinx 的配置值，包括在终端执行 sphinx-quickstart 时选中的那些值。
   #. index.rst：文档项目的 root 目录。如果将文档划分为其他文件，该目录会连接这些文件。





编写REST文件规则
=================

#. 文字样式

   斜体：在斜体字的左右分别加上一个星号：*斜体*

   粗体：在粗体字的左右分别加上两个星号：**粗体**

#. 插入程序代码
   
   需要在段落最后添加两个冒号，也可以在空行上添加，但是此时冒号是被忽略的：

   程序::

    #!/usr/bin/evn python

    print "hello,world"

   需要注意的是，上面的程序需要缩进，否则不会被认为是程序。

   可以 用 .. code-block:: 追加各种语法高亮声明:

   .. code-block:: python   
    :linenos:

    #!/usr/bin/evn python

    print "hello,world"


参考文献： :file:`http://jwch.sdut.edu.cn/book/rst.html`
