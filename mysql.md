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

查看数据库的表名：show tables;

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

### 条件查询
select 字段名 from 表名 while 条件

条件分为：
< = <= >= != is null(为null)

and:并且 or:或者 in:包含，相当于多个or not:取非  between .. and .. 两个值之间 and优先级比or高

like:模糊查询 支持%和下划线查询 %匹配任意多个字符 下划线，一个下划线匹配一个字符 如果查询中含有_或者%使用转义\在前面

### 排序
例子：select ename,sal from emp order by sal;(默认升序)

select ename,sal from emp order by sal asc;(指定升序);

select ename,sal from emp order by sal desc;(指定降序);

多个字段排序：select ename,sal from emp order by sal asc,ename asc;当前一个相等时才执行下一个进行排序，否则按照第一个排序。

按照列排序：select ename,sal from emp order by 2;第二列排序。

执行顺序：1、from 2、where 3、select 4、order by(排序总在最后执行)

### 数据处理函数（单行处理函数）
case .. when .. then .. when .. then else .. end 模拟if函数。
