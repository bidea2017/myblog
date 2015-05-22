  下面是在源码阅读过程中遇到的一些问题, 给 Jetty 提的 bugs 和一些建议、疑问.如果你看的版本比较低, 如果遇到的话可以稍微注意下.


##### org.eclipse.jetty.start.Main 重复创建 ClassLoader
详见：https://bugs.eclipse.org/bugs/show_bug.cgi?id=448446 


##### XmlConfiguration#initParser() 方法不应该用 synchronized 修饰
详见：https://bugs.eclipse.org/bugs/show_bug.cgi?id=448225 


##### HttpParser#next(buffer) 为何没有判断 0x7F(127-Delete) 为非法字符
这不是 bug, 因为 HTTP 规范定义有点模糊, 不明确.不过在 9.3.x 版本中会加入这个判断.
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=461350  


##### HttpMethod#lookAheadGet() 方法判断 MOVE 方法的时候没有判断 bytes 长度
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=458209 


##### HttpParser#parseLine() 重复解析 version
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=461466  
这个问题费了一些口舌, +_+.


##### MetaData#addDiscoveredAnnotation() 减小锁的粒度
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=462529 
这个问题作者不打算改,只是为了保持方法的语义明确,不过作者鼓励自个弄个 patch 修正这个问题.修正这个问题也非常简单.


##### ini/xml 文件编码格式如果有问题, 解析出错的时候报告文件信息
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=464441 
配置文件多了,不知道是哪个文件有问题,就比较蛋疼了.


##### AbstractSessionManager#removeEventListener() 方法没有移除 HttpSessionIdListener
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=464989  


##### HttpSessionBinding(Activation)Listener 使用 web.xml 和注解方式导致的行为不一致
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=465074 

##### (不算 bug) JDBCSessionManager#addSession() 是否应该在把 session 保存到数据后调用 session.didActivate() ? 
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=465074 
在上面的 "HttpSessionBinding(Activation)Listener 使用 web.xml 和注解方式导致的行为不一致" 的评论中.


##### JDBCSessionManager.Session#setCookieSet() 方法没有进行同步
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=465162 
 

##### 文件上传 Part.write() 内部使用其它的方式来替代不靠谱的 File.renameTo() 方法
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=466005 


##### 文件上传在 9.2.7 和 9.2.10 版本中的存在的问题
详见 https://bugs.eclipse.org/bugs/show_bug.cgi?id=466009   
