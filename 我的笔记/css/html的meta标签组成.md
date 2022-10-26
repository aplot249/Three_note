# html的meta标签组成
**name属性**
----------

> name属性主要用于描述网页，与之对应的属性值为content，content中的内容主要是便于搜索引擎机器人查找信息和分类信息用的。meta标签的name属性语法格式是：`<meta name="参数"content="具体的参数值">`  
> 其中name属性主要有以下几种参数:

Keywords(关键字)

*   说明：keywords用来告诉搜索引擎你网页的关键字是什么
*   举例：`<meta name="keywords" content="science,education,culture,politics,ecnomics,relationships,entertaiment,human">`

description(网站内容描述)

*   说明：description用来告诉搜索引擎你的网站主要内容。
*   举例：`<meta name="description" content="Thispageisaboutthemeaningofscience,education,culture.">`

robots(机器人向导)

*   说明：robots用来告诉搜索机器人哪些页面需要索引，哪些页面不需要索引。content的参数有all,none,index,noindex,follow,nofollow。默认是all。
*   举例：`<meta name="robots"content="none">`

author(作者)

*   说明：标注网页的作者
*   举例：`<metaname="author"content="root,root@xxxx.com">`

**http-equiv属性**
----------------

http-equiv顾名思义，相当于http的文件头作用，它可以向浏览器传回一些有用的信息，以帮助正确和精确地显示网页内容，与之对应的属性值为content，content中的内容其实就是各个参数的变量值。

meta标签的http-equiv属性语法格式是：

<metahttp-equiv=”参数”content=”参数变量值”>；

其中http-equiv属性主要有以下几种参数：

A、Expires(期限)

说明：可以用于设定网页的到期时间。一旦网页过期，必须到服务器上重新传输。

用法：<metahttp-equiv=”expires”content=”Fri,12Jan200118:18:18GMT”>

注意：必须使用GMT的时间格式。

B、Pragma(cache模式)

说明：禁止浏览器从本地计算机的缓存中访问页面内容。

用法：<metahttp-equiv=”Pragma”content=”no-cache”>

注意：这样设定，访问者将无法脱机浏览。

C、Refresh(刷新)

说明：自动刷新并指向新页面。

用法：<metahttp-equiv=”Refresh”content=”2;URL=[http://www.jb51.net">(注意后面的引号，分别在秒数的前面和网址的后面)](http://www.jb51.xn--net%22%3E%28%2C%29-4y73afvkww60adpaha362agvzusa876oh8le55agn2chjzdjad8170al27bwc4nnaf/)

注意：其中的2是指停留2秒钟后自动刷新到URL网址。

D、Set-Cookie(cookie设定)

说明：如果网页过期，那么存盘的cookie将被删除。

用法：<metahttp-equiv=”Set-Cookie”content=”cookievalue=xxx;expires=Friday,12-Jan-200118:18:18GMT；path=/“>

注意：必须使用GMT的时间格式。

E、Window-target(显示窗口的设定)

说明：强制页面在当前窗口以独立页面显示。

用法：<metahttp-equiv=”Window-target”content=”\_top”>

注意：用来防止别人在框架里调用自己的页面。

F、content-Type(显示字符集的设定)

说明：设定页面使用的字符集。

用法：<metahttp-equiv=”content-Type”content=”text/html;charset=gb2312”>

G、content-Language（显示语言的设定）

用法：<metahttp-equiv=”Content-Language”content=”zh-cn”/>

H、Cache-Control指定请求和响应遵循的缓存机制。  
Cache-Control指定请求和响应遵循的缓存机制。在请求消息或响应消息中设置Cache-Control并不会修改另一个消息处理过程中的缓存处理过程。请求时的缓存指令包括no-cache、no-store、max-age、max-stale、min-fresh、on

ly-if-cached，响应消息中的指令包括public、private、no-cache、no-store、no-transform、must-revalidate、proxy-revalidate、max-age。各个消息中的指令含义如下  
Public指示响应可被任何缓存区缓存  
Private指示对于单个用户的整个或部分响应消息，不能被共享缓存处理。这允许服务器仅仅描述当用户的部分响应消息，此响应消息对于其他用户的请求无效  
no-cache指示请求或响应消息不能缓存  
no-store用于防止重要的信息被无意的发布。在请求消息中发送将使得请求和响应消息都不使用缓存。  
max-age指示客户机可以接收生存期不大于指定时间（以秒为单位）的响应  
min-fresh指示客户机可以接收响应时间小于当前时间加上指定时间的响应  
max-stale指示客户机可以接收超出超时期间的响应消息。如果指定max-stale消息的值，那么客户机可以接收超出超时期指定值之内的响应消息。