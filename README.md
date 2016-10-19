Azkaban 3 [![Build Status](http://img.shields.io/travis/azkaban/azkaban.svg?style=flat)](https://travis-ci.org/azkaban/azkaban)
========

从源代码编译
--------------------
azkaban使用gradle编译，如果你当前环境下没有gradle，你可以到[github.com/gradle/gradle](github.com/gradle/gradle)下载源码编译或者下载发布的二进制包

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

以下根据azkaban文档翻译，[文档地址](http://azkaban.github.io/azkaban/docs/latest/#solo-setup)

介绍
------------
Azkaban是一个在LinkedIn开发用来跑Hadoop作业的一款批处理作业调度框架，Azkaban通过作业的依赖关系解决了作业顺序和提供了更加方便的Web用户界面来维持和跟踪你的作业

特性
------------
* 兼容所有版本的 Hadoop
* 基于 Web 的易用 UI
* 简单的 Web 和 HTTP 工作流上传
* 项目工作空间
* 工作流调度
* 模块化和插件化
* 支持认证和授权
* 可跟踪用户行为
* 失败和成功时的邮件提醒
* SLA 警告和自动终止
* 失败作业的重试

概述
------------
Azkaban是由LinkedIn实现的为了解决hadoop作业依赖问题一个批处理调度平台。如果需要我们的作业按照顺序执行，从作业中ETL（抽取extract、转换transform、加载load）数据来分析产品，那么Azkaban将是一个很好的选择。

随着hadoop用户数量的增长，从最初的单个服务器的解决方案，Azkaban已经演变成更加健壮的解决方案。

Azkaban包含了3个关键的组件

* 关系型数据库服务器 (MySQL)
* Azkaban Web服务器 （AzkabanWebServer）
* Azkaban 执行服务器 （AzkabanExecutorServer）

![](https://github.com/silence940109/azkaban/blob/master/image/azkaban2overviewdesign.png)

###关系型数据库（MySQL）
Azkaban使用MySQL来存储他本身的状态信息，同样的AzkabanWebServer
和AzkabanExecutorServer也使用数据库。

####AzkabanWebServer怎么要使用数据库？
web服务器使用数据库有如下原因：

* 工程管理




