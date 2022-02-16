# mysql数据库学习
## 开启与关闭mysql
`开启：net start mysql`

`关闭：net stop mysql`
## 登录mysql
`打开cmd，输入：mysql -uroot -p密码。`
## mysql常用命令
退出：exit

查看：show databases;

使用：use 数据库名字;

创建：create database 数据库名字;

## sql语句分类
DQL：数据查询语言（select查）
**操作表中的数据**

DML：数据操作语言（包括insert增、delete删、upate改）
**操作表中的数据**

DDL：数据定义语言
带有drop删除、alter修改、creat新建语句的都是DDL语句
**主要操作的是表的结构**

TCL：事务控制语言

`事务提交：commit`

`事务回滚：rollback`

DCL：数据控制语言

`授权：grant`

`撤销权限：revote`
## 查询语句
### 查询一个字段
select 字段名 from 表名 
**select与from为关键字，字段名和表名都是标识符**
### 查询两个或者多个字段
select 字段名,字段名 from 表名
**使用字段隔开即可**
### 查询所有字段
select a,b,c... from 表名 **建议**

select * from 表名 **不建议，会拖累java运行效率**


