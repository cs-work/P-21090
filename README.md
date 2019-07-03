基于SSM的健身房管理系统、基于Java Web的健身房管理系统
=====

## 需求

编写并实现一个基于Java Web的健身房管理系统, 采用SSM(Spring, SpringMVC, Mybatis)三大框架实现, 能够实现教练管理, 会员管理, 器材管理的功能

### 运行环境

jdk+tomcat8+mysql5.6+Eclispse

### 项目技术

spring, springmvc, mybatis, jsp, jquery, mysql


### 注意事项

1. 运行时需要预先创建数据库, 字符集为utf8mb4, 并导入源码里的sql文件
2. 更改源码包里的jdbcConfig.properties的数据库配置
3. Eclipse导入, 使用tomcat运行


## 讲解

### 技术原理

这个项目采用最原生的项目构建方式, 所有依赖jar包都在lib文件夹下, Eclipse导入即可运行, 比较适合Java Web开发的初学者, 代码整体结构比较清晰, 整体采用MVC架构的方式进行编写

+ Model层: 即dao包下的代码, 注意由于是采用了mybatis来进行数据库的操作, 故改层代码只是接口, 通过mybatis机制与classpath下的userMapper.xml联系起来
+ Controller层: 即controller包下的代码, 采用springmvc的方式进行实现, 设计了所需要的所有请求接口, 并对请求接口进行预处理, 用于调用service层的服务
+ View层: controller层渲染数据到view层, view层采用最基础的jsp进行实现, 没有使用其他的模板引擎

### 数据库设计

部分项目核心数据库表示例如下, 其他参见源码包

用户表设计如下(user)

|字段|类型|备注|
|----|-----|-----|
|id| int(20) | 编号|
|name| varchar(20)| 用户名|
|pwd |varchar(20)| 密码|
|account| varchar(20) |登录名|
|age |int(10) |年龄|
|sex |int(2) |性别 0女 1男|
|tel |varchar(20) |电话|
|address |varchar(20)|地址|
|uclass |int(20) |科目编号|
|uteach |int(20) |教练编号|


### 运行截图

部分运行截图为

![](http://mirror.tarax.cn/P-21090/1.jpg)

![](http://mirror.tarax.cn/P-21090/2.jpg)
![](http://mirror.tarax.cn/P-21090/3.jpg)


项目源码: [点击获取](http://cs-work.com/p/21090)
