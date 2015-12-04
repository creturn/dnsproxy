
#DNSproxy DNS代理

此代理是基于别人代码二次开发的，基于的是 http://www.wolfermann.org/dnsproxy.html

对此进行修改实现DNS代理并且获取其中DNS请求的domain域名记录进sqlite3数据库中

----------

##使用场景:
 * 反向DNS代理，例如公司网络不稳定自己常用来进行反向代理谷歌8.8.8.8
 * 家里路由主DNS指向自己的代理，可以定期分析些数据，指不定中招后也能分析些异常行为
 * 盲注中想把数据通过DNS带出来
 * 绕过防火墙通过DNS把数据带出来
 * 等等...
 
##配置文件:
 * 配置文件（dns.conf, dnsproxy.conf 两个一样）中的配置项说明
 * authoritative 主DNSIP
 * authoritative-port 主DNS端口
 * chroot /var/empty   配置chroot目录哪怕user是root也只能在此目录操作
 * user creturn  用什么用户来启用此进程
 
##注意事项:

 * 代码中使用了sqlie3所以编译的时候确保装有sqlite3的库
 * 生成Makefile中自行添加 -lsqlite3否则编译肯定不过
 * Linux下编译会提示某些for语句只支持c99 可以根据提示之行添加支持


###截图:
![img](https://raw.githubusercontent.com/creturn/dnsproxy/master/screens/screen.png)          