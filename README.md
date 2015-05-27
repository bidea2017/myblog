记录平时写的一些东西, 以及翻译的一些文章(只用于学习交流的目的).为了方便,有些已经转成了 PDF.


Jetty
-----
  阅读 Jetty 9.2.3 源码的一些笔记, 同时有些地方对比了 Tomcat.

- [给 Jetty 提的 bugs 和建议](https://github.com/ykgarfield/myblog/blob/master/doc/%E7%BB%99%20Jetty%20%E6%8F%90%E7%9A%84%20bug%20%E5%92%8C%E5%BB%BA%E8%AE%AE.md)
- [HttpSessionActivationListener 引发的一些问题(Jetty vs Tomcat)](http://ykgarfield.github.io/Jetty-Source-Read/HttpSessionActivationListener%20%E5%BC%95%E5%8F%91%E7%9A%84%E4%B8%80%E4%BA%9B%E9%97%AE%E9%A2%98_Jetty%20vs%20Tomcat.pdf)
- [Jetty-悲催的文件上传-bug 修补记](http://ykgarfield.github.io/Jetty-Source-Read/Jetty-%E6%82%B2%E5%82%AC%E7%9A%84%E6%96%87%E4%BB%B6%E4%B8%8A%E4%BC%A0-bug%E4%BF%AE%E8%A1%A5%E8%AE%B0.pdf)
- [Jetty 负载均衡配置-使用自带的 BalancerServlet 或 Apache Http Server](http://ykgarfield.github.io/Jetty-Source-Read/Jetty%20%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1%E9%85%8D%E7%BD%AE-%E4%BD%BF%E7%94%A8%E8%87%AA%E5%B8%A6%E7%9A%84%20BalancerServlet%20%E6%88%96%20Apache%20Http%20Server.pdf)
- [Jetty9.3.x 源码配置](http://ykgarfield.github.io/Jetty-Source-Read/Jetty9-3-x-%E6%BA%90%E7%A0%81%E9%85%8D%E7%BD%AE.pdf)


Java-NIO
--------
- [Channel关闭输入,输出流的差异-纠正 Fundamental Networking in Java 一书中的一个错误](http://ykgarfield.github.io/Java-NIO/Channel%E5%85%B3%E9%97%AD%E8%BE%93%E5%85%A5,%E8%BE%93%E5%87%BA%E6%B5%81%E7%9A%84%E5%B7%AE%E5%BC%82-%E7%BA%A0%E6%AD%A3%20Fundamental%20Networking%20in%20Java%20%E4%B8%80%E4%B9%A6%E4%B8%AD%E7%9A%84%E4%B8%80%E4%B8%AA%E9%94%99%E8%AF%AF.pdf)
- [NIO 读事件的处理 1-问题所在](http://ykgarfield.github.io/Java-NIO/NIO%20%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86%201-%E9%97%AE%E9%A2%98%E6%89%80%E5%9C%A8.pdf)
- [NIO 读事件的处理 2-Tomcat 对读事件的处理](http://ykgarfield.github.io/Java-NIO/NIO%20%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86%202-Tomcat%20%E5%AF%B9%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86.pdf)
- [NIO 读事件的处理 3-Jetty 对读事件的处理](http://ykgarfield.github.io/Java-NIO/NIO%20%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86%203-Jetty%20%E5%AF%B9%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86.pdf)
- [NIO 读事件的处理 4-xSocket 对读事件处理](http://ykgarfield.github.io/Java-NIO/NIO%20%E8%AF%BB%E4%BA%8B%E4%BB%B6%E7%9A%84%E5%A4%84%E7%90%86%204-xSocket%20%E5%AF%B9%E8%AF%BB%E4%BA%8B%E4%BB%B6%E5%A4%84%E7%90%86.pdf)
- [Jetty-半包粘包的处理](http://ykgarfield.github.io/Java-NIO/Jetty-%E5%8D%8A%E5%8C%85%E7%B2%98%E5%8C%85%E7%9A%84%E5%A4%84%E7%90%86.pdf)

#### 《Fundamental Networking in Java》翻译过的部分章节
  这本书的英文阅读实在有点难, +_+.翻译过部分的也有些地方不全.

- [第2章 IP基础](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC2%E7%AB%A0%20IP%E5%9F%BA%E7%A1%80.pdf)
- [第3章 TCP基础](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC3%E7%AB%A0%20TCP%E5%9F%BA%E7%A1%80.pdf)
- [第4章 可伸缩的I-O](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC4%E7%AB%A0%20%E5%8F%AF%E4%BC%B8%E7%BC%A9%E7%9A%84I-O.pdf)
- [第5章 可伸缩的TCP](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC5%E7%AB%A0%20%E5%8F%AF%E4%BC%B8%E7%BC%A9%E7%9A%84TCP.pdf)
- [第9章 单播UDP](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC9%E7%AB%A0%20%E5%8D%95%E6%92%ADUDP.pdf)
- [第10章 可伸缩的UDP](http://ykgarfield.github.io/Java-NIO/%E7%AC%AC10%E7%AB%A0%20%E5%8F%AF%E4%BC%B8%E7%BC%A9%E7%9A%84UDP.pdf)


Tomcat
------ 
  阅读了部分源码(基于 8.0.5), 主要是为了与 Jetty 对比.

- [给 Tomcat 提的 bugs 和建议(目前就俩, 囧)](https://github.com/ykgarfield/myblog/blob/master/doc/%E7%BB%99%20Tomcat%20%E6%8F%90%E7%9A%84%20bug%20%E5%92%8C%E5%BB%BA%E8%AE%AE.md)
- [在 Tomcat 源码中调试 WebSocket 的注意事项](http://ykgarfield.github.io/Tomcat-Source-Read/%E5%9C%A8%20Tomcat%20%E6%BA%90%E7%A0%81%E4%B8%AD%E8%B0%83%E8%AF%95%20WebSocket%20%E7%9A%84%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9.pdf)
- [IDEA 和 Eclipse 下调试安全策略的差异以及 SecurityClassLoad 类的作用](http://ykgarfield.github.io/Tomcat-Source-Read/IDEA%20%E5%92%8C%20Eclipse%20%E4%B8%8B%E8%B0%83%E8%AF%95%E5%AE%89%E5%85%A8%E7%AD%96%E7%95%A5%E7%9A%84%E5%B7%AE%E5%BC%82%E4%BB%A5%E5%8F%8A%20SecurityClassLoad%20%E7%B1%BB%E7%9A%84%E4%BD%9C%E7%94%A8.pdf)


Jetty Document 9.2.3.v20140905 中文翻译
----------------------------------
- [第1章 Jetty介绍 ](http://ykgarfield.github.io/jetty-9.2.3.v20140905-zh/introduction.html)
- [第2章 Jetty 使用介绍 ](http://ykgarfield.github.io/jetty-9.2.3.v20140905-zh/quick-start-getting-started.html)
- [第3章 Jetty 配置介绍 ](http://ykgarfield.github.io/jetty-9.2.3.v20140905-zh/quick-start-configure.html)
- [第4章 发布到 Jetty ](http://ykgarfield.github.io/jetty-9.2.3.v20140905-zh/configuring-deployment.html)
- [第5章 配置 Contexts ](http://ykgarfield.github.io/jetty-9.2.3.v20140905-zh/configuring-contexts.html)


Java Concurrency
--------------
- [Java 线程教程(图解挺多)](http://ykgarfield.github.io/JavaConcurrency/Java%E7%BA%BF%E7%A8%8B%E6%95%99%E7%A8%8B.pdf)


Java_WebSocket_Programming
------------------------
  学习了下 WebSocket 的基础知识.

- [第1章 Java WebSocket 基础](http://ykgarfield.github.io/WebSocket/Java_WebSocket_Programming/%E7%AC%AC1%E7%AB%A0-Java%20WebSocket%20%E5%9F%BA%E7%A1%80.pdf)  


Scala In Action
---------------
  简单入了个门.

- [第2章 入门指南](http://ykgarfield.github.io/scala/scala_in_action/%E7%AC%AC2%E7%AB%A0%20%E5%85%A5%E9%97%A8%E6%8C%87%E5%8D%97.pdf)

