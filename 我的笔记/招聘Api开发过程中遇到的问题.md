# 招聘Api开发过程中遇到的问题
1、**Django解决扩展用户表时,后台Admin显示密码为明文的问题**

[https://blog.51cto.com/xsboke/2362570#:~:text=Django%E8%A7%A3%E5%86%B3%E5%BD%93%E6%89%A9%E5%B1%95%E7%94%A8%E6%88%B7%E8%A1%A8%E6%97%B6%2C%E7%94%A8%E6%88%B7%E7%BB%A7%E6%89%BFAbstractUser%E5%90%8E%2C%E5%90%8E%E5%8F%B0Admin%E4%BC%9A%E6%98%BE%E7%A4%BA%E5%AF%86%E7%A0%81%E4%B8%BA%E6%98%8E%E6%96%87%E7%9A%84%E9%97%AE%E9%A2%98%20%E5%85%88%E7%9C%8B%E9%A1%B9%E7%9B%AE%E5%88%97%E8%A1%A8%201%E3%80%81%E4%BB%8A%E5%A4%A9%E5%9C%A8%E5%86%99%E4%B8%80%E4%B8%AA%E6%89%A9%E5%B1%95Django%E9%BB%98%E8%AE%A4%E7%9A%84%E7%94%A8%E6%88%B7%E8%A1%A8%E5%8A%9F%E8%83%BD%E6%97%B6%2C%E9%81%87%E5%88%B0%E4%BA%86%E4%B8%80%E4%B8%AA%E9%97%AE%E9%A2%98.,%E5%85%88%E7%BB%99%E5%A4%A7%E5%AE%B6%E7%9C%8B%E4%B8%80%E4%B8%8B%E6%88%91%E5%86%99%E7%9A%84%EF%BC%8C%E6%89%A9%E5%B1%95%E7%94%A8%E6%88%B7%E8%A1%A8%E7%9A%84models%20%5Bapps.users.models%5D%20%EF%BC%8C%E6%88%91%E6%98%AF%E9%80%9A%E8%BF%87%E7%BB%A7%E6%89%BFAbstractUser%E8%BF%9B%E8%A1%8C%E6%89%A9%E5%B1%95%E7%9A%84%20%28%E8%BF%98%E6%9C%89%E4%B8%80%E7%A7%8D%E6%96%B9%E5%BC%8F%E6%98%AF%E5%BC%95%E5%85%A5User%E8%A1%A8%2C%E9%80%9A%E8%BF%87%E5%A4%96%E9%94%AE%E7%9A%84%E5%BD%A2%E5%BC%8F%E8%BF%9B%E8%A1%8C%E6%89%A9%E5%B1%95%29.](https://blog.51cto.com/xsboke/2362570#:~:text=Django%E8%A7%A3%E5%86%B3%E5%BD%93%E6%89%A9%E5%B1%95%E7%94%A8%E6%88%B7%E8%A1%A8%E6%97%B6%2C%E7%94%A8%E6%88%B7%E7%BB%A7%E6%89%BFAbstractUser%E5%90%8E%2C%E5%90%8E%E5%8F%B0Admin%E4%BC%9A%E6%98%BE%E7%A4%BA%E5%AF%86%E7%A0%81%E4%B8%BA%E6%98%8E%E6%96%87%E7%9A%84%E9%97%AE%E9%A2%98%20%E5%85%88%E7%9C%8B%E9%A1%B9%E7%9B%AE%E5%88%97%E8%A1%A8%201%E3%80%81%E4%BB%8A%E5%A4%A9%E5%9C%A8%E5%86%99%E4%B8%80%E4%B8%AA%E6%89%A9%E5%B1%95Django%E9%BB%98%E8%AE%A4%E7%9A%84%E7%94%A8%E6%88%B7%E8%A1%A8%E5%8A%9F%E8%83%BD%E6%97%B6%2C%E9%81%87%E5%88%B0%E4%BA%86%E4%B8%80%E4%B8%AA%E9%97%AE%E9%A2%98.,%E5%85%88%E7%BB%99%E5%A4%A7%E5%AE%B6%E7%9C%8B%E4%B8%80%E4%B8%8B%E6%88%91%E5%86%99%E7%9A%84%EF%BC%8C%E6%89%A9%E5%B1%95%E7%94%A8%E6%88%B7%E8%A1%A8%E7%9A%84models%20%5Bapps.users.models%5D%20%EF%BC%8C%E6%88%91%E6%98%AF%E9%80%9A%E8%BF%87%E7%BB%A7%E6%89%BFAbstractUser%E8%BF%9B%E8%A1%8C%E6%89%A9%E5%B1%95%E7%9A%84%20%28%E8%BF%98%E6%9C%89%E4%B8%80%E7%A7%8D%E6%96%B9%E5%BC%8F%E6%98%AF%E5%BC%95%E5%85%A5User%E8%A1%A8%2C%E9%80%9A%E8%BF%87%E5%A4%96%E9%94%AE%E7%9A%84%E5%BD%A2%E5%BC%8F%E8%BF%9B%E8%A1%8C%E6%89%A9%E5%B1%95%29.)

2、django admin 怎么通过url显示图片

[https://www.codetd.com/article/2872125](https://www.codetd.com/article/2872125)

3、取消粒子 SIMPLEUI\_LOGIN\_PARTICLES = False

4、**Django 中使用 utf8mb4 支持 emoji 表情**

[**https://www.chenshaowen.com/blog/using-utf8mb4-in-django-to-support-emoji-expression.html**](https://www.chenshaowen.com/blog/using-utf8mb4-in-django-to-support-emoji-expression.html)

[**https://www.jianshu.com/p/0fb464ca644f**](https://www.jianshu.com/p/0fb464ca644f)

[**https://blog.csdn.net/qq\_24369959/article/details/115161587**](https://blog.csdn.net/qq_24369959/article/details/115161587)

**5、Django admin - 如何在用户编辑中隐藏某些字段**

[**https://www.coder.work/article/6270539**](https://www.coder.work/article/6270539)

**6、微信小程序双向数据绑定**

[https://blog.csdn.net/weixin\_48458705/article/details/114643302](https://blog.csdn.net/weixin_48458705/article/details/114643302)

7、wx.request 缺少 PATCH 方法

[https://developers.weixin.qq.com/community/develop/doc/0008648f00097075d0e7b339351400](https://developers.weixin.qq.com/community/develop/doc/0008648f00097075d0e7b339351400)

8、**python 日期函数date、datetime 以及各种形式转换**

[https://blog.csdn.net/weixin\_35834894/article/details/108930202](https://blog.csdn.net/weixin_35834894/article/details/108930202)

9、[**微信小程序使用wxParse解析html**](https://www.cnblogs.com/llkbk/p/7910454.html)

[https://www.cnblogs.com/llkbk/p/7910454.html](https://www.cnblogs.com/llkbk/p/7910454.html)

10、[django simpleUI 富文本编辑](https://cn.bing.com/search?q=django%20simpleUI%20%20%E5%AF%8C%E6%96%87%E6%9C%AC%E7%BC%96%E8%BE%91%E5%99%A8&qs=n&form=QBRE&=%25eManage%20Your%20Search%20History%25E&sp=-1&pq=django%20simpleui%20%E5%AF%8C%E6%96%87%E6%9C%AC%E7%BC%96%E8%BE%91%E5%99%A8&sc=0-22&sk=&cvid=45B27B29C57B425DB1943745BFA410CD&ghsh=0&ghacc=0&ghpl=)器

[https://imyshare.com/article/17/](https://imyshare.com/article/17/)

11、**微信小程序构建npm找不到miniprogram文件**

https://blog.csdn.net/weixin\_44835957/article/details/115349614