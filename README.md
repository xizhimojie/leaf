此站点用java编写，用时将近一个星期，还是颇费了一番力气，项目代码写的不算好，也没什么单元测试.请轻拍. 虽然功能简单， 但还是有些亮点:

1. 技术选型简单，Servlet3.0 + DBUtils + Mysql, 数据源druid, 用Servlet3实现的restful.
2. 考虑到快速建站，配置文件分离，支持图片分离（支持七牛存储接口).
3. 多说插件支持，申请多说帐号，配置文件写入帐号即可.
4. markdown语法支持.支持Github风格的Markdown.



演示站点:

    http://www.xizhimojie.com(已废弃, 此站点已改用jekyll.)

================================================================
Quick Start
================================================================

0.  请确保你的环境已经安装JDK7+和maven,mysql，因为需要你自己手动build.


1. 进入~\src\main\webapp\WEB-INF，编辑db_server.properties

    数据库地址
    	url=jdbc:mysql://127.0.0.1:3306/xizhimojie  
	数据库用户名  
	username=root  
	数据库密码  
	password=123456  
	网址  
	website=www.xizhimojie.com  
	站点名称  
	sitename=细枝末节  
	多说插件,配置下面帐号,账号申请：http://duoshuo.com  
	duoshuo=  
	七牛云存储token,配置下面三个参数,申请指南:http://developer.qiniu.com/  
    	ACCESS_KEY=  
	SECRET_KEY=  
	QINIU_URL=  

2. 导入数据库脚本\~blog\src\main\webapp\WEB-INF\init.sql

3. 在项目根目录下面执行maven命令 mvn clean compile war:war

4. 在target目录下面把安装包放到tomcat/ROOT下面，启动tomcat

5. 后台地址为/login, 默认密码为admin/admin, 请及时修改

