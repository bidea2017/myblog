##### ����ͷ����,���µ� ArrayIndexOutOfBoundsException
  
  ���� `server.xml` �е� `Connector` �� `maxHttpHeaderSize` ����,�����������Ϊһ����С��ֵ,���������,�ᵼ�� Tomcat ���� `ArrayIndexOutOfBoundsException`:

```java
28-Jan-2015 16:08:01.870 SEVERE [http-nio-8080-exec-1] org.apache.coyote.http11.AbstractHttp11Processor.endRequest Error finishing response
java.lang.ArrayIndexOutOfBoundsException: 24
        at org.apache.coyote.http11.AbstractOutputBuffer.sendStatus(AbstractOutputBuffer.java:445)
        at org.apache.coyote.http11.AbstractHttp11Processor.prepareResponse(AbstractHttp11Processor.java:1554)
        at org.apache.coyote.http11.AbstractHttp11Processor.action(AbstractHttp11Processor.java:739)
        at org.apache.coyote.Response.action(Response.java:179)
```

  ������������ https://issues.apache.org/bugzilla/show_bug.cgi?id=57509.


#### ��鵽�ظ��� websocket �˵����Ƶ�ʱ���׳�����ϸ����Ϣ: �������������˵�����

  û�뵽����ĸĽ���ʽ�ᱻ������Ϊһ�� path(���߷��ʼ�Ҫȫ��, �º�ſ���, ��), ��� https://bz.apache.org/bugzilla/show_bug.cgi?id=57676.



