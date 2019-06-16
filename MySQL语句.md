# MySQL

标签（空格分隔）： 数据库

---

# # 库操作

## 创建数据库

```
create database <数据库名>;
```

## 查看已经创建的数据库信息

```
show create database oldboy\G;
```

## 创建数据库指定字符集

```
mysql> create database oldgirl CHARACTER SET gbk COLLATE gbk_chinese_ci;

mysql>create database abc character set utf8 collate utf8_general_ci;
```

## 查看字符集和校对规则

```sql
show character set;
```

## 创建不同字符集格式的数据库命令

```
create database oldboy; 

create database oldboy_gbk DEFAULT CHARACTER SET gbk COLLATE gbk_chinese_ci; #<==创建gbk字符集数据库

create database oldboy_utf8 DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;<==创建utf8字符集数据库
```

## 查看数据库

```
show databases like '%boy%';
```

## 查看当前所在数据库

```
mysql> select database();
+------------+
| database() |
+------------+
| NULL       |
+------------+
1 row in set (0.02 sec)
```

## 进入某个库

```
mysql> use mysql;
Database changed
```

---

# 表结构操作

## 查看一个库中的表

```
mysql> show tables;
+---------------------------+
| Tables_in_mysql           |
+---------------------------+
| columns_priv              |
| db                        |
| event                     |
| func                      |
```

## 创建表

```sql
create table 表名(
字段名1 类型,
字段名2 类型,
字段名3 类型
);
create table student(
id int(4) not null,
name char(20) not null,
age tinyint(2) NOT NULL default '0',
dept varchar(16) default NULL
);

CREATE TABLE `test` (
`id` int(4) NOT NULL AUTO_INCREMENT,
`name` char(20) NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=UTF8;


CREATE TABLE `stu` (
`id` int(11) NOT NULL AUTO_INCREMENT COMMENT '学生学号',
`name` varchar(50) NOT NULL COMMENT '学生姓名',
`age` tinyint(3) unsigned DEFAULT NULL COMMENT '学生年龄',
`gender` enum('m','f') DEFAULT NULL COMMENT '性别',
`birthday` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT '入学时间',
PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

## 创建一个表与之前的表结构相同

```sql
create table student_0 like student;
```

## 创建一个备份表

```sql
create table t1_1 as select * from t1;
```

## 查看已创建表的语句

```
mysql> show create table student\G; 
*************************** 1. row ***************************
       Table: student
Create Table: CREATE TABLE `student` (
  `id` int(4) NOT NULL,
  `name` char(20) NOT NULL,
  `age` tinyint(2) NOT NULL DEFAULT '0',
  `dept` varchar(16) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8
1 row in set (0.00 sec)
```

## 查看表结构

```
mysql> desc student;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(4)      | NO   |     | NULL    |       |
| name  | char(20)    | NO   |     | NULL    |       |
| age   | tinyint(2)  | NO   |     | 0       |       |
| dept  | varchar(16) | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
4 rows in set (0.00 sec)
```

## 生产场景创建的表

某sns产品生产正式建表语句

```
use sns;
set names gbk;
CREATE TABLE `subject_comment_manager` (
  `subject_comment_manager_id` bigint(12) NOT NULL auto_increment COMMENT '主键',
  `subject_type` tinyint(2) NOT NULL COMMENT '素材类型',
  `subject_primary_key` varchar(255) NOT NULL COMMENT '素材的主键',
  `subject_title` varchar(255) NOT NULL COMMENT '素材的名称',
  `edit_user_nick` varchar(64) default NULL COMMENT '修改人',
  `edit_user_time` timestamp NULL default NULL COMMENT '修改时间',
  `edit_comment` varchar(255) default NULL COMMENT '修改的理由',
  `state` tinyint(1) NOT NULL default '1' COMMENT '0代表关闭，1代表正常',
  PRIMARY KEY  (`subject_comment_manager_id`),
  KEY `IDX_PRIMARYKEY` (`subject_primary_key`(32)), #<==括号内的32表示对前32个字符做前缀索引。
  KEY `IDX_SUBJECT_TITLE` (`subject_title`(32))
  KEY `index_nick_type` (`edit_user_nick`(32),`subject_type`)#<==联合索引，此行为新加的，用于给大家讲解的。实际表语句内没有此行。
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;
```

## 增加字段

```
alter table 表名 add字段 类型 其他;

CREATE TABLE `test` (
  `id` int(4) NOT NULL AUTO_INCREMENT,
  `name` char(20) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;



CREATE TABLE `test` (
  `id` int(4) NOT NULL AUTO_INCREMENT,
  `name` char(20) NOT NULL,
  PRIMARY KEY (`id`)
) engine=innodb default charset=utf8;



alter table test add sex char(4);    #←增加性别列sex


alter table test add age int(4) after name;   在name字段后面添加age字段

alter table test add qq varchar(15) first;    在表最前面
```

## 增加1个字段

```
ALTER TABLE `etiantian` ADD `FIRSTPHOTO_URL` varchar(255) default NULL COMMENT '第一张图片URL'
```

## 增2个字段

```
ALTER TABLE `basic` ADD `adhtml_top`  varchar(1024) default NULL COMMENT '顶部广告html' ,  ADD `adhtml_right` varchar(1024) default NULL COMMENT '右侧广告html' ;
```

## 修改字段属性

```
mysql> alter table test modify age char(4) after name;         
Query OK, 6 rows affected (0.00 sec)
Records: 6  Duplicates: 0  Warnings: 0
```

## 修改字段名称及属性

```
mysql> alter table test change age oldboyage char(4) after name;            
Query OK, 6 rows affected (0.01 sec)
Records: 6  Duplicates: 0  Warnings: 0

ALTER TABLE student CHANGE telnum tnum CHAR(11)
```

## 修改表名

```
mysql> rename table test to oldboy;
Query OK, 0 rows affected (0.00 sec)

mysql> show tables;                
+------------------+
| Tables_in_oldboy |
+------------------+
| course           |
| oldboy           |
| sc               |
| student          |
| test1            |
+------------------+
5 rows in set (0.00 sec)

mysql> alter table oldboy rename to test;
Query OK, 0 rows affected (0.00 sec)

mysql> show tables;                      
+------------------+
| Tables_in_oldboy |
+------------------+
| course           |
| sc               |
| student          |
| test             |
| test1            |
+------------------+
5 rows in set (0.00 sec)
```

## 复制表结构

```
create table stu like student;
```

## 复制表结构及数据（\***）

```
CREATE TABLE city1 SELECT * FROM city;
```

# 表内容操作

## 插入数据

```
insert into 表名(字段名1,字段名2,...) values(值1,值2,...);

INSERT INTO student(name,age,gender,tnum) VALUES('alex',10,'f','110');


create table test(
id int(4) not null auto_increment,
name char(20) not null,
primary key(id)
);

mysql> insert into test(id,name) values(1,'oldboy');
Query OK, 1 row affected (0.00 sec)

mysql> select * from test;
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
+----+--------+
1 row in set (0.00 sec)

mysql> insert into test(name) values('oldgirl');
Query OK, 1 row affected (0.02 sec)

mysql> select * from test;                      
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
+----+---------+
2 rows in set (0.00 sec)


mysql> insert into test values(3,'inca');       
Query OK, 1 row affected (0.00 sec)

mysql> select * from test;               
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
+----+---------+
3 rows in set (0.00 sec)
```

## 批量插入数据

```
mysql> insert into test values(4,'zuma'),(5,'kaka');
Query OK, 2 rows affected (0.00 sec)
Records: 2  Duplicates: 0  Warnings: 0

mysql> select * from test;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
5 rows in set (0.00 sec)


INSERT INTO `test` VALUES (1,'oldboy'),(2,'oldgirl'),(3,'inca'),(4,'zuma'),(5,'kaka');


INSERT INTO student(name,age,gender,tnum) VALUES('alex',15,'f','11634'),('alex1',16,'m','123425');
```

## 一个表中的数据插入另一个表

```sql
insert into student_0 select * from student;
```

## 清空表中所有数据

```sql
mysql> truncate table test;
Query OK, 0 rows affected (0.00 sec)

mysql> select * from test; 
Empty set (0.00 sec)

mysql> insert into test values(1,'oldboy'),(2,'oldgirl'),(3,'inca'),(4,'zuma'),(5,'kaka');
Query OK, 5 rows affected (0.00 sec)
Records: 5  Duplicates: 0  Warnings: 0

mysql> select * from test;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
5 rows in set (0.00 sec)
```

补充强调：我们平时登录网站发帖子，发博文，实质上都是调用web网站的程序连接MySQL数据库，通过上述的insert语句把帖子博文数据存入数据库的。

## 查询

```sql
mysql> select id,name from oldboy.test;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
```

```
mysql> select * from test limit 2;     
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
+----+---------+
2 rows in set (0.00 sec)

mysql> select * from test limit 3;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
+----+---------+
3 rows in set (0.00 sec)

mysql> select * from test limit 1,3;
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
+----+---------+
3 rows in set (0.00 sec)
```

```
mysql> select * from test where name='oldboy';
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
+----+--------+


mysql> select * from test where id=5;
+----+------+
| id | name |
+----+------+
|  5 | kaka |
+----+------+
1 row in set (0.00 sec)

mysql> select * from test where name='oldgirl';
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
+----+---------+
1 row in set (0.00 sec)

mysql> desc test;
+-------+----------+------+-----+---------+----------------+
| Field | Type     | Null | Key | Default | Extra          |
+-------+----------+------+-----+---------+----------------+
| id    | int(4)   | NO   | PRI | NULL    | auto_increment |
| name  | char(20) | NO   |     | NULL    |                |
+-------+----------+------+-----+---------+----------------+
2 rows in set (0.00 sec)

mysql> select * from test where id>3 and name='oldgirl';
Empty set (0.00 sec)

mysql> select * from test where id<3 and name='oldgirl'; 
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
+----+---------+
1 row in set (0.00 sec)

mysql> select * from test where id>3 or name='oldgirl'; 
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
3 rows in set (0.00 sec)


mysql> select * from test where id>3 or name='oldgirl' order by id desc;
+----+---------+
| id | name    |
+----+---------+
|  5 | kaka    |
|  4 | zuma    |
|  2 | oldgirl |
+----+---------+
3 rows in set (0.00 sec)
```

 小结
一：查看表test中所有数据
(1)直接查询库下面表的数据
select * from oldboy.test;  #方法1：没有进入oldboy数据库的情况
select id from oldboy.test;   #查看id列的方法
select name from oldboy.test;   #查看name列的方法
(2)进入指定库查询表的数据
use oldboy;     #方法1：已经进入oldboy数据库的情况
select * from test;
(3)查看MySQL数据库的用户与主机
select user,host from mysql.user;  #仅查看用户与主机
select user,host,password from mysql.user;    #查看用户与主机与密码
二：根据指定条件查询表的部分信息
例子1：查看test表中的前2条信息
select * from test limit 2;
例子2：查看第1条记录后的两条记录
select * from test limit 1,2;
例子3：指定固定的条件查数据
select * from test where id = 1;  #查看指定行的记录，整型一般不需要加引号，不然会导致不经过索引。
select * from test where name='oldgirl';  #查询字符串的话要加引号
select * from test where id=2 and name='oldgirl';  #多个条件查询
例子4：指定固定条件范围查数据
select * from test where id>2 and id<5;      #多个条件，and取交集
select * from test where id>2 or id<5;   #多个条件都成立，也就是显示id>2和id<5的所有条件都会显示出来
三：其他查询功能
(1)按照id号进行正向排序
select * from test order by id asc;
(2)按照id号进行倒序排序
select * from test order by id desc;

select count(name) from city where CountryCode='CHN';

```
SELECT * FROM city;
SELECT NAME,Population FROM city;
SELECT * FROM city WHERE CountryCode='CHN';

SELECT * FROM city WHERE CountryCode='CHN' AND Population>5000000;

SELECT * FROM city WHERE CountryCode='CHN' ORDER BY Population DESC LIMIT 3 ;

SELECT * FROM city WHERE District='zhejiang' ORDER BY Population DESC LIMIT 3;

SELECT * FROM city WHERE CountryCode='CHN' AND District LIKE 'shan%';

SELECT * FROM city WHERE Population >5000000 OR Population<100;

SELECT * FROM city WHERE Population >5000000 
UNION
SELECT * FROM city WHERE Population <100;
```

## 多表联查

```
mysql> select country.name from city,country where city.population<100 and country.code=city.countrycode;
+----------+
| name     |
+----------+
| Pitcairn |
+----------+
1 row in set (0.00 sec)

mysql> select co.name from city as ci,country as co where ci.population<100 and co.code=ci.countrycode;
+----------+
| name     |
+----------+
| Pitcairn |
+----------+
1 row in set (0.00 sec)
```

## 排序

```
select * from city where countrycode='chn' order by population desc;
```

## 限制limit

```
mysql> select * from city where countrycode='chn' order by population desc limit 10;
+------+--------------------+-------------+--------------+------------+
| ID   | Name               | CountryCode | District     | Population |
+------+--------------------+-------------+--------------+------------+
| 1890 | Shanghai           | CHN         | Shanghai     |    9696300 |
| 1891 | Peking             | CHN         | Peking       |    7472000 |
| 1892 | Chongqing          | CHN         | Chongqing    |    6351600 |
| 1893 | Tianjin            | CHN         | Tianjin      |    5286800 |
| 1894 | Wuhan              | CHN         | Hubei        |    4344600 |
| 1895 | Harbin             | CHN         | Heilongjiang |    4289800 |
| 1896 | Shenyang           | CHN         | Liaoning     |    4265200 |
| 1897 | Kanton [Guangzhou] | CHN         | Guangdong    |    4256300 |
| 1898 | Chengdu            | CHN         | Sichuan      |    3361500 |
| 1899 | Nanking [Nanjing]  | CHN         | Jiangsu      |    2870300 |
+------+--------------------+-------------+--------------+------------+
10 rows in set (0.01 sec)


select * from city where countrycode='chn' order by population desc limit 10 offset 10;

SELECT * FROM city WHERE CountryCode='USA' ORDER BY Population;
SELECT * FROM city WHERE CountryCode='USA' ORDER BY Population DESC;



#跳过10行显示三行
SELECT * FROM city WHERE CountryCode='USA' ORDER BY Population DESC LIMIT 10,3;

SELECT * FROM city WHERE CountryCode='USA' ORDER BY Population DESC LIMIT 3 OFFSET 10;
```

in语句

```
select name,population,countrycode from city where population in (2000000,3000000,4000000);

between  and
select name,population,countrycode from city where population between 1000000 and 1000001;
```

## 分组聚合  group by

group by + 聚合函数（最大值、最小值等）

先分组聚合再筛选

```
select countrycode ,sum(population) from city group by countrycode having countrycode='CHN';
```

先筛选在分组聚合

```
select countrycode ,sum(population) from city where countrycode='CHN' group by countrycode;
```

```
SELECT CountryCode,SUM(Population) FROM city WHERE CountryCode='CHN' GROUP BY CountryCode


SELECT CountryCode,SUM(Population) FROM city GROUP BY CountryCode;

SELECT CountryCode,District,SUM(Population) AS sp FROM city 
WHERE CountryCode='CHN' 
GROUP BY District
ORDER BY sp DESC;
```

## union  结果集合并  用来代替or

按行合并

## union all  合并

```
CREATE TABLE ma(
maid INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
mname VARCHAR(30) NOT NULL, 
bumen VARCHAR(20) NOT NULL
);

INSERT INTO ma(mname,bumen) 
VALUES
('wuxingge','linux'),
('alexsb','python'),
('tanboyu','java'),
('qiangge','bdata');


#统计每个部门的员工+经理数量

SELECT t.bumen ,SUM(t.c) FROM 
(
SELECT  bumen, COUNT(NAME) AS c  FROM stu1 
GROUP BY bumen 
UNION ALL
SELECT bumen,COUNT(mname) AS c FROM ma
GROUP BY bumen
)t
GROUP BY t.bumen;
```

练习题

```
select name,population,countrycode from city where countrycode='CHN' union select name,population,countrycode from city where population >10000000;
```

```
#创建表
CREATE TABLE stu1(id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,name VARCHAR(20),age INT,gender ENUM('m','f'),xueke ENUM('linux','python','java','bdata'),telnum VARCHAR(10),gongzi int);

#插入数据
INSERT INTO 
stu1(id,name,age,gender,xueke,telnum,gongzi)
VALUES
(1,'guosiyu',10,'f','linux',110,10000),
(2,'yuhuafei',20,'m','linux',120,10010),
(3,'zhangjianfeng',19,'m','linux',119,10020),
(4,'lijiayang',18,'m','linux',123,10030),
(5,'changxueyuan',17,'m','linux',132,10040),
(6,'sunwukong',200,'m','python',211,1000),
(7,'zhubajie',201,'f','python',122,2000),
(8,'bailongma',123,'f','java',345,3000),
(9,'zhangfei',40,'m','java',456,5000),
(10,'guanyu',50,'m','bdata',789,6000);
```

```
#2、由于guosiyu表现不好，扣工资1000
update stu1 set gongzi=gongzi-1000 WHERE name='guosiyu';

#3、将yuhuafei姓名修改为yudaye
update stu1 set name='yudaye' WHERE name='yuhuafei';

#4、添加状态列state
ALTER TABLE stu1 ADD state ENUM('1','0') DEFAULT '1';

#5、查询所有员工的姓名及工资情况
select name,gongzi from stu1;

#6、查询年龄超过100岁的员工
select name from stu1 where age>100;

#7、查询工资低于5000的员工信息
select name,age from stu1 WHERE gongzi<5000;

#8、查询姓名以zhang开头的员工信息
SELECT * from stu1 where name like 'zhang%';

#9、查询linux学科中员工信息，并以工资升序排列
select * from stu1 WHERE xueke='linux' ORDER BY gongzi;


#10、统计不同学科的总工资(sum())
SELECT xueke,sum(gongzi) from stu1 GROUP BY xueke;


#----------扩展--------
#注：函数介绍
#avg()    求平均数
#max()    求最大值
#min()    求最小值
#count()  统计个数
#----------------

#11、统计不同学科的平均工资(avg())
SELECT xueke,AVG(gongzi) from stu1 GROUP BY xueke;


#12、统计不同学科的最高工资(max())
SELECT xueke,MAX(gongzi) from stu1 GROUP BY xueke;


#13、统计不同学科的最低工资(min())的员工
SELECT xueke,name,min(gongzi) from stu1  GROUP BY xueke;


#14、统计男、女性别的员工数量(count())
SELECT gender,count(gender) from stu1 GROUP BY gender;


#15、统计各个学科的员工数量(count())
SELECT xueke,count(xueke) from stu1 GROUP BY xueke;
```

# 多表连接查询

## 传统连接

where A.ID=B.ID
select ci.name,ci.countrycode,ci.population,co.name from city as ci,country as co where ci.countrycode=co.code and ci.population<100;

```
SELECT ma.`mname`,stu1.`name`,stu1.`gongzi` FROM stu1,ma WHERE stu1.`bumen`=ma.`bumen` AND stu1.`name`='guosiyu';
```

```
SELECT city.`Name`,country.`Name`,city.`Population` FROM city,country WHERE city.`CountryCode`=country.`Code` AND city.`Population`<100;
```

## join 连接

```
SELECT ma.`mname`,stu1.`name`,stu1.`gongzi` FROM stu1 
JOIN ma
ON stu1.`bumen`=ma.`bumen`
WHERE stu1.`name`='guosiyu';
```

```
#查询人口数量最多的城市名、所在国家、大洲
SELECT city.`Name`,country.`Name`,country.`Continent`,
MAX(city.`Population`)
FROM city
JOIN country
ON city.`CountryCode`=country.`Code`;
```

```
#查询亚洲，人口数量超过500w的城市名，所在国家名字
SELECT country.`Name`,city.`Name`,city.`Population` AS cp
FROM city
JOIN country
ON city.`CountryCode`=country.`Code`
WHERE city.`Population`>5000000 AND country.`Continent`='asia'
ORDER BY cp DESC;
```

```
#统计亚洲，城市人口数量超过500w的城市的数量
SELECT country.name,COUNT(city.name)
FROM city
JOIN country
ON city.`CountryCode`=country.`Code`
WHERE city.`Population`>5000000 AND country.`Continent`='asia'
GROUP BY country.`Name`
```

Acc_bill:账单表
Acct_id      bill_id     bill_sts     bill_mon

Acc_bill_dtl:账单明细表
Bill_id      fee_item_id       amount       rax_rate

账单月是2018.4月的整月账单数据

```
Select  *   from  Acc_bill    where bill_mon=’2018-4’;
```

账单编号是2001020的账单总金额

```
select bill_id,sum(amount) from Acc_bill_dtl where Bill_id=’20010120’;
```

账单月是2018.4月的税率有几种类型，并按照税率大小倒序排列

```
select a. bill_mon,count(b.tax_rate) from a
Join b
On a.bill_id=b.bill_id
Where a.bill_mon=’2018-4’
Group by a.bill_mon
Order by b.tax_rate desc;
```

## 内连接

```
select A.xx ,B.xxxx from A join B on A.xxx=B.xxx where 
```

自动连接 （natural join）
两个表有相同的字段countrycode

```
select name,countrycode,language,population from city natural join countrylanguage where population > 1000000 order by population;
```

```
mysql> desc city;
+-------------+----------+------+-----+---------+----------------+
| Field       | Type     | Null | Key | Default | Extra          |
+-------------+----------+------+-----+---------+----------------+
| ID          | int(11)  | NO   | PRI | NULL    | auto_increment |
| Name        | char(35) | NO   |     |         |                |
| CountryCode | char(3)  | NO   | MUL |         |                |
| District    | char(20) | NO   |     |         |                |
| Population  | int(11)  | NO   |     | 0       |                |
+-------------+----------+------+-----+---------+----------------+
5 rows in set (0.01 sec)

mysql> desc countrylanguage;
+-------------+---------------+------+-----+---------+-------+
| Field       | Type          | Null | Key | Default | Extra |
+-------------+---------------+------+-----+---------+-------+
| CountryCode | char(3)       | NO   | PRI |         |       |
| Language    | char(30)      | NO   | PRI |         |       |
| IsOfficial  | enum('T','F') | NO   |     | F       |       |
| Percentage  | float(4,1)    | NO   |     | 0.0     |       |
+-------------+---------------+------+-----+---------+-------+
4 rows in set (0.00 sec)
```

```
Select s.snmae,c.cname,sc.score  from sJoin scOn s.sno=sc.snoJoin cOn sc.cno=c.cnoWhere c.cname=’xxxx’ and sc.score>85;
```

 join
上海市属于哪个国家

```
select ci.name,ci.countrycode,co.name from city as ci,country as co where ci.countrycode=co.code and ci.name='shanghai';

select ci.name,ci.countrycode,co.name from city as ci join country as co on ci.countrycode=co.code and ci.name='shanghai';
```

## 外连接

### left join

```
select A.xx ,B.xxxx from A left join B on A.xxx=B.xxx and xxx>60
```

```
select ci.name,ci.countrycode,co.name from city as ci left join country as co on ci.countrycode=co.code and ci.name='shanghai';
```

### right join

## 子查询

```
# 查找linux部门低于平均工资的员工姓名

SELECT NAME,gongzi  FROM stu1
WHERE xueke='linux'
AND gongzi<(SELECT AVG(gongzi)
FROM stu1 
WHERE xueke='linux');
```

```
select name from country where code= (select countrycode from city where population > 10000000);

select chnt.name,chnt.population from (select name,countrycode,population from city where countrycode='CHN') chnt limit 10;

select chnt.name,chnt.population from (select name,countrycode,population from city where countrycode='CHN') chnt where chnt.population>5000000  limit 10;
```

# 使用explain查看select语句的执行计划

```
mysql> explain select * from test where name='oldboy'\G
*************************** 1. row ***************************
           id: 1
  select_type: SIMPLE
        table: test
         type: ALL
possible_keys: NULL
          key: NULL
      key_len: NULL
          ref: NULL
         rows: 5
        Extra: Using where
1 row in set (0.00 sec)

mysql> alter table test add index ind_name(name(8));
Query OK, 0 rows affected (0.01 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> explain select * from test where name='oldboy'\G
*************************** 1. row ***************************
           id: 1
  select_type: SIMPLE
        table: test
         type: ref
possible_keys: ind_name
          key: ind_name
      key_len: 24
          ref: const
         rows: 1
        Extra: Using where
1 row in set (0.00 sec)
```

# 更新数据

```
update 表名 set 字段=新值,… where 条件（一定要注意条件）
```

```
mysql> select * from test;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
5 rows in set (0.00 sec)

mysql> update test set name='gongli' where name='oldgirl';
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from test;                                
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
|  2 | gongli |
|  3 | inca   |
|  4 | zuma   |
|  5 | kaka   |
+----+--------+
5 rows in set (0.00 sec)
```

## 防止误操作MySQL数据库一例

在mysql命令加上选项-U后，当发出没有WHERE或LIMIT关键字的UPDATE或DELETE时，mysql程序就会拒绝执行

mysql -S /data/3306/mysql.sock -uroot -poldboy -U

# 删除数据

 一行一行的删除

```
mysql> delete from test where id=3;
Query OK, 1 row affected (0.00 sec)

mysql> select * from test;         
+----+--------+
| id | name   |
+----+--------+
|  1 | gongli |
|  2 | gongli |
|  4 | gongli |
|  5 | gongli |
+----+--------+
4 rows in set (0.00 sec)
```

全部删除数据

```
mysql> truncate table test;
Query OK, 0 rows affected (0.00 sec)
```

> 适用场景：drop table 可以先 truncate table  ，然后 drop table

# 删除数据(2)

通过状态删除表中的数据（update代替delete）

```
alter table student add status int default 1;

mysql> select * from test where state=1;
+----+---------+-------+
| id | name    | state |
+----+---------+-------+
|  1 | oldboy  |     1 |
|  2 | oldgirl |     1 |
|  3 | inca    |     1 |
|  4 | zuma    |     1 |
|  5 | kaka    |     1 |
+----+---------+-------+
5 rows in set (0.00 sec)


mysql> update test set state=0 where id=2;
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from test where state=1;
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | oldboy |     1 |
|  3 | inca   |     1 |
|  4 | zuma   |     1 |
|  5 | kaka   |     1 |
+----+--------+-------+
4 rows in set (0.00 sec)
```

逻辑删除数据实例

```
mysql> alter table test add state tinyint(2);
Query OK, 4 rows affected (0.03 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from test where state=1;     
Empty set (0.00 sec)

mysql> desc test;
+-------+------------+------+-----+---------+----------------+
| Field | Type       | Null | Key | Default | Extra          |
+-------+------------+------+-----+---------+----------------+
| id    | int(4)     | NO   | PRI | NULL    | auto_increment |
| name  | char(20)   | NO   | MUL | NULL    |                |
| state | tinyint(2) | YES  |     | NULL    |                |
+-------+------------+------+-----+---------+----------------+
3 rows in set (0.00 sec)

mysql> select * from test;
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |  NULL |
|  2 | gongli |  NULL |
|  4 | gongli |  NULL |
|  5 | gongli |  NULL |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> update test set state='1';    
Query OK, 4 rows affected (0.00 sec)
Rows matched: 4  Changed: 4  Warnings: 0

mysql> select * from test;       
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  4 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> select * from test where state=1;
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  4 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> update test set state='0' where id=4;
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from test where state=1;    
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
3 rows in set (0.00 sec)
```

---

# 用户相关

---

# 权限相关

---

# 索引

## 创建索引

```
ALTER TABLE student ADD INDEX idx_name(name);

CREATE INDEX idx_age ON student(age);
```

## 查看索引

```
SHOW INDEX FROM student;
```

## 删除索引

```
ALTER TABLE student drop INDEX idx_age;
```

---

---
