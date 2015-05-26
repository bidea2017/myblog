##### 请求头过大,导致的 ArrayIndexOutOfBoundsException
  
  设置 `server.xml` 中的 `Connector` 的 `maxHttpHeaderSize` 属性,将其故意设置为一个较小的值,作出请求后,会导致 Tomcat 引发 `ArrayIndexOutOfBoundsException`:

```java
28-Jan-2015 16:08:01.870 SEVERE [http-nio-8080-exec-1] org.apache.coyote.http11.AbstractHttp11Processor.endRequest Error finishing response
java.lang.ArrayIndexOutOfBoundsException: 24
        at org.apache.coyote.http11.AbstractOutputBuffer.sendStatus(AbstractOutputBuffer.java:445)
        at org.apache.coyote.http11.AbstractHttp11Processor.prepareResponse(AbstractHttp11Processor.java:1554)
        at org.apache.coyote.http11.AbstractHttp11Processor.action(AbstractHttp11Processor.java:739)
        at org.apache.coyote.Response.action(Response.java:179)
```

  此问题可以详见 https://issues.apache.org/bugzilla/show_bug.cgi?id=57509.


#### 检查到重复的 websocket 端点名称的时候抛出更详细的信息: 具体是哪两个端点重名

  没想到提出的改进方式会被作者作为一个 path(作者发邮件要全名, 事后才看到, 囧), 详见 https://bz.apache.org/bugzilla/show_bug.cgi?id=57676.



