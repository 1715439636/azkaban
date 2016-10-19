Azkaban 3 [![Build Status](http://img.shields.io/travis/azkaban/azkaban.svg?style=flat)](https://travis-ci.org/azkaban/azkaban)
========

从源代码编译
--------------------

从源代码编译Azkaban，执行下面命令：

```
./gradlew distTar
```

上面的命令把所有的Azkaban下的包打包为.zip.tar格式，如果在window下，你可以执行下面的命令打包为zip格式：

```
./gradlew distZip
```

If not building for the first time, it's good to clean first:

如果不是第一次编译，你最好clean一下：

```
./gradlew clean
```

文档
-------------

Azkaban文档, 请去[Azkaban Project Site](http://azkaban.github.io). 文档的源码在 [gh-pages branch](https://github.com/azkaban/azkaban/tree/gh-pages)可以找到

需要帮助的，请到Azkaban Google小组: [Azkaban Group](https://groups.google.com/forum/?fromgroups#!forum/azkaban-dev)
