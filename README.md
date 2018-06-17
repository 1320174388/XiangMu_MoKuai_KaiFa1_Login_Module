Login_Module : 用户登录模块目录
===============

> 模块基于ThinkPHP5.1目录开发，以项目开发基础目录为标准

## 目录结构

~~~
├─login_module           模块目录
│  ├─config              配置目录
│  │  ├─tableName.php    数据表配置文件
│  │  ├─wx_config.php    小程序配置文件
│  │  └─ ...             更多配置
│  ├─working_version     工作版本目录
│  │  ├─v1               版本1目录
│  │  │  ├─controller    控制器目录
│  │  │  ├─dao           数据持久层目录
│  │  │  ├─library       自定义类目目录
│  │  │  ├─model         模型目录
│  │  │  └─service       逻辑层目录
│  │  └─ ...             更多版本目录      
│  │ common.php          模块函数文件
│  └─mysql_query_sql.php 可执行文件，创建数据表
├─login_route_api.php    对应模块的路由文件
├─README.md              模块说明文件
~~~

<br/>

### 注意：用户登录模块的路由文件，禁止更改，后期如果优化，只能优化代码执行效率，不能更改路由访问地址以及数据库表结构。

<br/>

## 模块使用说明：

### `wx_config.php 配置文件，需要修改对应小程序的 AppID 及 AppSecret(秘钥)`

### `tableName.php 配置文件，需要修改对应项目的数据表名`

### `login_route_api.php 文件，保存到项目 `route` 目录中，路由自动生效。`

### `mysql_query_sql.php 可执行文件，需要修改对应项目的数据库及表名。`

### `打开命令行执行命令： php mysql_query_sql.php 自动生成模块数据表`

<br/>

## v1版本接口说明：

### `1、用户登录接口`

#### 请求方式：`POST` 

#### 路由地址：`/:v/login_module/login_init/:code`

#### 返回数据：`{"errNum":0,"retMsg":"登录成功","retData":{"token":"用户标识"}}`

#### 返回数据：`{"errNum":1,"retMsg":"请检查Code是否失效","retData":false}`

#### 返回数据：`{"errNum":1,"retMsg":"错误信息","retData":false}`
