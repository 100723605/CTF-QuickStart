<a name="iibxb"></a>
# 什么才是伪协议？
伪协议不是因特网上真实存在的协议。而是为关联应用程序使用的<br />真实存在：http:// https:// ftp://<br />伪协议：tencent:// (qq) data:// (用base64在浏览器输出二进制文件) javascript://

我们可以试试在浏览器url栏中输入一下 **javascript:alert('cxcx');**<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/35135677/1690088479916-a208c735-298a-478e-b7b3-ae3e66c0bdd2.png#averageHue=%23959190&clientId=u3c395e30-0695-4&from=paste&height=211&id=u61873b87&originHeight=211&originWidth=924&originalType=binary&ratio=1&rotation=0&showTitle=false&size=25355&status=done&style=none&taskId=u7aabe175-9971-4930-9284-ecd94204e9f&title=&width=924)<br />可以看到有一个弹窗，并且内容是我们输入的字符串。它是把JavaScript后面的代码当成JavaScript代码执行，并且把结果返回给界面。


<a name="MVyAI"></a>
# 那么什么是JavaScript伪协议？

这个特殊协议是把**JavaScript：URL，URL**会被当成JavaScript代码进行执行，由JavaScript解释器运行。如果有多个语句，必须用分号分隔。

例如
```php
javascript:window.open("about:blank");alert("cxcx");
```
它会创建一个新的窗口，但是alert函数的执行还是会在之前的窗口执行。因为这是一个分隔符。执行完第一个执行第二个。



参考[https://www.cnblogs.com/forforever/p/12711197.html](https://www.cnblogs.com/forforever/p/12711197.html)
