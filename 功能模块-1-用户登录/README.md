Login_Module : 用户登录模块目录
===============

> 模块基于ThinkPHP5.1目录开发，以项目开发基础目录为标准

## 目录结构

~~~
├─login_module           模块目录
│  ├─config              配置目录
│  │  ├─wx_config.php    配置文件
│  │  └─ ...             更多配置
│  ├─working_version     工作版本目录
│  │  ├─v1               版本1目录
│  │  │  ├─controller    控制器目录
│  │  │  ├─dao           数据持久层目录
│  │  │  ├─library       自定义类目目录
│  │  │  ├─model         模型目录
│  │  │  └─service       逻辑层目录
│  │  └─ ...             更多版本目录      
│  └─common.php          模块函数文件
├─login_route_api.php    对应模块的路由文件
├─mysql_query_sql.php    可执行文件，创建数据表
├─README.md              模块说明文件
~~~

### 模块使用说明：

*   config.php 配置文件，需要修改对应小程序的 AppID 及 AppSecret(秘钥)
