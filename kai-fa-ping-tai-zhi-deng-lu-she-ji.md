**背景**

一个企业应用，最基本的功能就是登录了。小到从数据库中获取不可逆密码和账户进行合法性校验，大到有自己独立的AD域，与域中已有的域账户进行合法性校验，更有一些上升到跨系统之间的单点登录。那么在一个企业应用中，有哪些实现的方式呢？

**方式**

**单系统认证**：拦截（框架）+验证（数据库、ldap）

1、利用Java Web中Filter的应用

![](https://upload-images.jianshu.io/upload_images/5700335-5093f8cea2b6087e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/473)

2、利用成熟安全性框架：Spring Security或Apache Shiro



![](https://upload-images.jianshu.io/upload_images/5700335-4ba4c4ec2d162021.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/450)

3、认证操作框架：Spring Ldap（域）、JDBC（数据库）

**跨系统认证**：SSO

1、CAS

![](https://upload-images.jianshu.io/upload_images/5700335-b82ee1be0dbea32f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/544)

根据系统应用的规模，从单系统认证的模式，到跨系统的单点登录认证，通过以上的方式均可实现。

