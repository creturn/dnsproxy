
#DNSproxy DNS代理

此代理是基于别人代码二次开发的，基于的是 http://www.wolfermann.org/dnsproxy.html

对此进行修改实现DNS代理并且获取其中DNS请求的domain域名记录进sqlite3数据库中

----------

##注意事项:

 * 代码中使用了sqlie3所以编译的时候确保装有sqlite3的库
 * 生成Makefile中自行添加 -lsqlite3否则编译肯定不过
 * Linux下编译会提示某些for语句只支持c99 可以根据提示之行添加支持
 

###截图:
![img](https://raw.githubusercontent.com/creturn/dnsproxy/master/screens/screen.png)          