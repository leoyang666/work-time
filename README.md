**项目说明** 
- 基于人人开源构建，采用SpringBoot、MyBatis、Shiro框架 
**step1
- 普通用户login 后进入系统，可以增删改查，自己在项目中的工作时间
- 管理员用户可以查看统计工时并用用图形化展示。
**step2
- ......

<br> 

**项目结构** 
```
renren-security
├─renren-common     公共模块
│ 
├─renren-admin      管理后台
│    ├─db  数据库SQL脚本
│    │ 
│    ├─modules  模块
│    │    ├─job 定时任务
│    │    ├─oss 文件存储
│    │    └─sys 系统管理(核心)
│    │ 
│    └─resources 
│        ├─mapper   MyBatis文件
│        ├─statics  静态资源
│        ├─template 系统页面
│        │    ├─modules      模块页面
│        │    ├─index.html   AdminLTE主题风格（默认主题）
│        │    └─index1.html  Layui主题风格
│        └─application.yml   全局配置文件
│       
│ 
├─renren-api        API服务
│ 
├─renren-generator  代码生成器
│        └─resources 
│           ├─mapper   MyBatis文件
│           ├─template 代码生成器模板（可增加或修改相应模板）
│           ├─application.yml    全局配置文件
│           └─generator.properties   代码生成器，配置文件
│
```

<br>

 **技术选型：** 
- 核心框架：Spring Boot 2.1
- 安全框架：Apache Shiro 1.4
- 视图框架：Spring MVC 5.0
- 持久层框架：MyBatis 3.5
- 定时器：Quartz 2.3
- 数据库连接池：Druid 1.1
- 日志管理：SLF4J 1.7、Log4j
- 页面交互：Vue2.x

<br>

 **软件需求** 
- JDK1.8
- MySQL5.5+
- Maven3.0+

<br>

 **本地部署**
- 通过git下载源码
- idea、eclipse需安装lombok插件，不然会提示找不到entity的get set方法
- 创建数据库renren_security，数据库编码为UTF-8
- 执行db/mysql.sql文件，初始化数据【按需导入表结构及数据】
- 修改application-dev.yml文件，更新MySQL账号和密码
- 在renren-security目录下，执行mvn clean install
<br>

- Eclipse、IDEA运行AdminApplication.java，则可启动项目【renren-admin】
- renren-admin访问路径：http://localhost:8080/renren-admin
- swagger文档路径：http://localhost:8080/renren-admin/swagger/index.html
- swagger注解路径：http://localhost:8080/renren-admin/swagger-ui.html
- 账号密码：admin/admin

<br>

- Eclipse、IDEA运行ApiApplication.java，则可启动项目【renren-api】
- renren-api访问路径：http://localhost:8081/renren-api/swagger-ui.html

<br>

- Eclipse、IDEA运行GeneratorApplication.java，则可启动项目【renren-generator】
- renren-generator访问路径：http://localhost:8082/renren-generator


<br>

 **集群部署**
- 集群部署，需要安装redis，并配置redis信息
- 需要配置【renren.redis.open=true】，表示开启redis缓存
- 需要配置【renren.cluster=true】，表示开启集群环境

<br>

 **项目演示**
- 演示地址：http://demo.open.renren.io/renren-security
- 账号密码：admin/admin

<br>

**如何交流、反馈、参与贡献？** 
- 开发文档：https://www.renren.io/guide/security
- 官方社区：https://www.renren.io/community
- gitee仓库：https://gitee.com/renrenio/renren-security
- github仓库：https://github.com/renrenio/renren-security
- [人人开源](https://www.renren.io)：https://www.renren.io   
- 官方QQ群：324780204、145799952
- 如需关注项目最新动态，请Watch、Star项目，同时也是对项目最好的支持
- 技术讨论、二次开发等咨询、问题和建议，请移步到官方社区，我会在第一时间进行解答和回复！
- 微信扫码并关注【人人开源】，获得项目最新动态及更新提醒<br>
![输入图片说明](http://cdn.renren.io/47c26201804031918312618.jpg "在这里输入图片标题")
<br>
<br>

**接口文档效果图：** 
![输入图片说明](http://cdn.renren.io/img/c8dae596146248d8b4d0639738c2932b "在这里输入图片标题")

<br>

**Layui主题风格：**
![输入图片说明](http://cdn.renren.io/img/1013aa91fe8542b7b05d82bc9444433a "在这里输入图片标题")

<br>

**AdminLTE主题风格：**
![输入图片说明](http://cdn.renren.io/img/f9762bc6574545ce908e271995efcf1c "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/a1b8bf1ea3db4844a8652a9cf84048cc "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/e542060605f94b3ebec699b0afffc22d "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/c94be5b4bf0d4387b18e119c91b1a986 "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/ae8c683a01c74d8dbc52d62547efda31 "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/ca38bcf3717c427d82dd67d86b744e18 "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/4862ec46a9ad469b90c30788c4707e35 "在这里输入图片标题")
![输入图片说明](http://cdn.renren.io/img/5d8e7243d30a4421b90f15394b6d1ccd "在这里输入图片标题")

<br>

![捐赠](http://cdn.renren.io/donate.jpg "捐赠") 