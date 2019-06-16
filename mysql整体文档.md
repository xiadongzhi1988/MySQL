本文作者: **wuXing**
# MySQL
[https://dev.mysql.com/doc/refman/5.7/en/](https://dev.mysql.com/doc/refman/5.7/en/)

https://bugs.mysql.com/


MySQL必会面试题100道
http://blog.51cto.com/oldboy/1959255


[https://db-engines.com/en/ranking](https://db-engines.com/en/ranking)





1. ** 数据库简介**
1. ** 关系型数据库**

关系型数据库的特点
二维表
典型产品Oracle传统企业，MySQL是互联网企业
数据存取是通过SQL
最大特点，数据安全性方面强（ACID）

people
| 姓名   | 性别   | 年龄   | 住址   |
|:----|:----:|:----|:----:|:----|:----:|:----|:----:|
| M   | 男   | 25   | ID   |
| ……   | ……   | ……   | ……   |


address
| 住址   | 国家   | 城市   | 街道   |
|:----|:----:|:----|:----:|:----|:----:|:----|:----:|
| ID   | 中国   | 北京   | 朝阳区北苑路108号   |
| ……   | ……   | ……   | ……   |









1. ** oracle**
1.  Oracle数据库版本介绍

7--8i--9i--10g—11g--12c



2.  Oracle的市场应用

市场份额第一，趋势递减
市场空间，传统企业
传统企业也在互联网化




2. ** mariadb**

https://mariadb.com/kb/en/library/documentation/



TokuDB存储引擎  -----------  zabbix



3. ** sql server**

微软和sysbase合作开发的产品，后来自己开发,windows平台
传统行业在用


4. ** DB2**

市场占有量小

目前只有：国有银行（人行、中国银行、工商银行等）、中国移动应用


5. ** mysql**

MySQL数据库版本介绍
  5.0--5.1--5.5--5.6--5.7--8.0
MySQL的市场应用
  中、大型互联网公司
  市场空间：互联网领域第一
  趋势明显
  同源产品：MariaDB、perconaDB






2. ** 非关系型数据库（nosql）**

NoSQL，Not Only SQL
不是否定关系型数据库，而是作为补充，现在也有部分替代的趋势
关注高性能，高并发，灵活性，忽略和上述无关的功能
典型产品：Redis（持久化缓存，两个半天）、MongoDB（最接近关系型数据的NoSQL）、Memcached
管理不适用SQL管理，而是用一些特殊的API或数据接口


6. **NoSQL的分类、特点、典型产品**

一些开源的NoSQL体系，如Facebook的Cassandra，Apache的Hbase, Redis，mongodb等
1、键值（Key-Value）存储数据库
使用哈希表。可以通过key来添加、查询或者删除数据，很高的性能和扩展性
典型产品：Memcache（新浪：Memcache持久化）、Redis（数据类型更丰富）、BerkeleyDB
2、列存储（column-oriented）数据库
典型产品：Cassandra（大网站在用），HBase
3、面向文档（Document-oriented）的数据库
典型产品：MongoDB（介于关系型数据库和非关系型数据库直接的产品），CouchDB
4、面向图形（Graphic）的数据库
典型产品：Neo4J，InfoGrid










7. ** memcache**

小结：
1、key-value型数据库
2、纯内存数据库
3、持久化产品memcachedb（sina开发）

8. ** redis**

官方文档：
http://www.redis.io/documentation
redis特点：
1、支持内存缓存，这个功能相当于memcached
2、支持持久化存储，这个功能相当于memcachedb，ttserver
3、数据类型更丰富，比其他key-value库功能更强
4、支持主从集群，分布式集群
5、支持队列等特殊功能
应用：缓存从存取memcached更改存取redis


9. ** nosql非关系型数据库小结**

1、nosql不是否定关系型数据库，而是作为关系型数据库的一个重要补充
2、nosql为了灵活及高性能、高并发而生，忽略影响性能、高并发的功能
3、nosql典型产品memcached（纯内存），redis（持久化缓存），mongodb
4、nosql没有标准的查询语言，通常使用REST式的数据接口或者查询API





3. ** 为什么选择MySQL数据库**

大多数使用Linux操作系统的大中小互联网网站都在使用MySQL数据库，
从大型的BAT（百度、阿里、腾讯）门户，到电商平台，分类门户等无一例外
都使用MySQL数据库
原因一下几点：
1、性能卓越，服务稳定，很少出现异常宕机；
2、开放源代码且无版权制约，自主性及使用成本低；
3、历史悠久，社区及用户非常活跃，遇到问题可以寻求帮助；
4、体积小，安装使用简单，易于维护，安装维护成本低；
5、品牌口碑效应，使企业无需考虑就直接使用，LAMP, LNMP流行架构；
6、支持多种操作系统，提供多种API接口，支持多种开发语言，特别对流行的
php语言有很好的支持

4. ** MySQL的分类与升级**

分类:社区版，商业版。 Alpha，Beta，RC,  GA版
区别：
1、商业版组织管理与测试环节控制更严格，稳定性方面，比社区版更稳定
2、MySQL成熟产品，商业版与社区版之间性能方面相差不大
3、商业版不遵守GPL协议，社区版遵守GPL协议可以免费试用
4、商业版可以购买相关服务，享受7X24小时技术支持以及打补丁等服务，
但是用户必须为此支付服务费用
5、社区版维护只能靠社区提供，无法像商业版获得故障及补丁服务

Alpha版：
一般只在开发的公司内部运行，不对外公开
Beta版:
完成功能的开发和所有的测试工作之后的产品，不会存在较大的功能或性能BUG
RC版：
生产环境发布之前的一个小版本或称候选版，是根据Beta版测试结果，收集到的BUG
或缺陷之处等收集到的信息，进行修复和完善之后的一版产品
GA：
软件产品正式发布的版本















5. **  MySQL的产品路线**

第一条：3.26--5.1版本
正宗后代
Centos5、6中默认有5.1版本
Centos7中默认是MariaDB

第二条：5.4--5.7 ，8.0版本
借鉴社区好的贡献，进一步开发的版本
主流版本：5.5 5.6 5.7

第三条：MySQL Cluster 6.0 版本&更高
类似于Oracle RAC，硬件要求高。
一般各大网站没有人用




6. ** 生产环境如何选择MySQL版本**

选择社区版的稳定GA版本
选择发布后6个月以上的GA版
要选择前后几个月没有大的BUG修复的版本，而不是大量修复BUG的几种版本
最好向后较长时间没有更新发布的版本
考虑开发人员开发程序使用的版本是否兼容你选的版本
优先企业非核心业务采用新版本的数据库GA版本软件
作为内部开发测试数据库环境，跑大概3-6个月时间
向DBA高手请教，或者在技术氛围好的群里和大家一起交流，使用真正的
高手们用过的好用的GA版本产品
经过上述工序后，若没有重要的功能BUG或性能瓶颈，则可以开始考虑
作为任何业务数据服务的后端数据软件









7. ** MySQL数据库的多种安装方法**

1.RPM、Yum：安装方便、安装速度快，无法定制
2.二进制：不需要安装，解压即可使用，不能定制功能
3.编译安装：可定制，安装慢。
  5.5之前：./configure make makeinstall
  5.5之后：cmake gmake
4.先编译，然后制作rpm，制作yum库，然后yum安装。
  简单、速度快、可定制，比较复杂制作时间长
企业选择安装方式
  中小企业：以上方式都可以，运维偏向编译，dba偏向选择二进制。
  大型企业：可以选择4





2. ** mysql发展史**

1979年，报表工具Unireg出现。
1985 年，以瑞典David Axmark为首，成立了一家公司（AB前身），IASM引擎出现。
1990年，提供SQL支持。
1999-2000年，MySQLAB公司成立，并公布源码，开源化。
2000年4月BDB引擎出现，支持事务。
2008年1月16号MySQL被Sun公司收购。
2009年04月20日Oracle收购Sun公司，MySQL转入Oracle 门下


3. ** mysql安装配置(5.6)**
8. ** 安装依赖**

yum groupinstall "Compatibility Libraries" "Development Tools"
yum install -y gcc gcc-c++ automake autoconf git make
yum -y install cmake bison-devel ncurses-devel libaio-devel

9. ** 获取mysql软件包**

http://repo.mysql.com/yum/mysql-5.6-community/el/6/x86_64/mysql-community-server-5.6.36-2.el6.x86_64.rpm

wget https://downloads.mysql.com/archives/get/file/mysql-5.6.34.tar.gz
wget https://downloads.mysql.com/archives/get/file/mysql-5.6.36.tar.gz
10. ** 配置编译选项**

https://dev.mysql.com/doc/refman/5.6/en/source-configuration-options.html


```bash
cmake . -DCMAKE_INSTALL_PREFIX=/application/mysql-5.6.34 \
-DMYSQL_DATADIR=/application/mysql-5.6.34/data \
-DMYSQL_UNIX_ADDR=/application/mysql-5.6.34/tmp/mysql.sock \
-DDEFAULT_CHARSET=utf8 \
-DDEFAULT_COLLATION=utf8_general_ci \
-DWITH_EXTRA_CHARSETS=all \
-DWITH_INNOBASE_STORAGE_ENGINE=1 \
-DWITH_FEDERATED_STORAGE_ENGINE=1 \
-DWITH_BLACKHOLE_STORAGE_ENGINE=1 \
-DWITHOUT_EXAMPLE_STORAGE_ENGINE=1 \
-DWITH_ZLIB=bundled \
-DWITH_SSL=bundled \
-DENABLED_LOCAL_INFILE=1 \
-DWITH_EMBEDDED_SERVER=1 \
-DENABLE_DOWNLOADS=1 \
-DWITH_DEBUG=0
```



11. 编译 && 安装
```bash
make && make install
```

12. 安装后操作
```bash
useradd -s /sbin/nologin mysql -M
ln -s /application/mysql-5.6.34  /application/mysql
chown -R mysql.mysql /application/mysql/data
/application/mysql/scripts/mysql_install_db --user=mysql --basedir=/application/mysql --datadir=/application/mysql/data
/bin/cp /application/mysql/support-files/my-default.cnf /etc/my.cnf
/bin/cp /application/mysql/support-files/mysql.server /etc/init.d/mysqld
echo 'export PATH=/application/mysql/bin:$PATH' >> /etc/profile
. /etc/profile
chkconfig --add mysqld
```


启动错误
Starting MySQL.Logging to '/application/mysql-5.6.36/data/db01.err'.
171113 13:07:01 mysqld_safe Directory '/application/mysql-5.6.36/tmp' for UNIX socket file don't exists.
 ERROR! The server quit without updating PID file (/application/mysql-5.6.36/data/db01.pid).

mkdir /application/mysql-5.6.36/tmp
chown -R mysql.mysql /application/mysql-5.6.36/tmp



4. ** mysql安装配置（5.7）**
13. ** #安装**
10. ** #二进制安装**

依赖
yum install libaio-devel perl-Module-*

tar xf mysql-5.7.17-linux-glibc2.5-x86_64.tar.gz
mv mysql-5.7.17-linux-glibc2.5-x86_64 /application/mysql-5.7.17
ln -s /application/mysql-5.7.17 /application/mysql
11. ** 源码编译安装**
3.  依赖

yum groupinstall "Compatibility Libraries" "Development Tools"
yum install -y gcc gcc-c++ automake autoconf git make
yum -y install cmake bison-devel ncurses-devel libaio-devel

#软件包存放目录
cd /server/tools
wget https://downloads.mysql.com/archives/get/file/mysql-5.7.20.tar.gz
wget https://downloads.mysql.com/archives/get/file/mysql-boost-5.7.20.tar.gz

tar xf mysql-5.7.20.tar.gz
tar xf mysql-boost-5.7.20.tar.gz



4.  配置编译选项

https://blog.csdn.net/caimouse/article/details/73123178

Boost库是为C++语言标准库提供扩展的一些C++程序库的总称，由Boost社区组织开发、维护。
字符串和文本处理库
容器库
迭代器库
算法库
函数对象和高阶编程库
泛型编程库
模板元编程
预处理元编程库
并发编程库
数学和数字库
排错和测试库
数据结构库
图像处理库
输入输出库
跨语言混合编程库
内存管理库
解析库
编程接口库
综合类库
编译器问题的变通方案库










cmake . -DCMAKE_INSTALL_PREFIX=/application/mysql-5.7.20 \
-DMYSQL_DATADIR=/application/mysql-5.7.20/data \
-DMYSQL_UNIX_ADDR=/application/mysql-5.7.20/tmp/mysql.sock \
-DDOWNLOAD_BOOST=1 \
-DWITH_BOOST=/server/tools/mysql-5.7.20/boost \
-DSYSCONFDIR=/etc \
-DDEFAULT_CHARSET=utf8mb4 \
-DDEFAULT_COLLATION=utf8mb4_general_ci \
-DWITH_EXTRA_CHARSETS=all \
-DWITH_INNOBASE_STORAGE_ENGINE=1 \
-DWITH_FEDERATED_STORAGE_ENGINE=1 \
-DWITH_BLACKHOLE_STORAGE_ENGINE=1 \
-DWITHOUT_EXAMPLE_STORAGE_ENGINE=1 \
-DWITH_MYISAM_STORAGE_ENGINE=1 \
-DWITH_ZLIB=bundled \
-DWITH_SSL=bundled \
-DENABLED_LOCAL_INFILE=1 \
-DWITH_EMBEDDED_SERVER=1 \
-DENABLE_DOWNLOADS=1 \
-DWITH_DEBUG=0



5.  #编译 && 安装

内存建议> 2GB
make && make install

编译过程中的问题（编译到73% 内存消耗殆尽）
c++: internal compiler error: Killed (program cc1plus) Please submit a full bug report


14. ** #授权**

chown -R mysql.mysql /application/mysql-5.7.17



15. ** #初始化**

/application/mysql-5.7.17/bin/mysqld --initialize --user=mysql --basedir=/application/mysql-5.7.17 --datadir=/application/mysql-5.7.17/data

记录初始密码（一定要记录!!!）
A temporary password is generated for root@localhost: );xf/h%lm6iR
16. ** #拷贝配置文件和启动文件**

cp /application/mysql-5.7.17/support-files/my-default.cnf /etc/my.cnf
cp /application/mysql-5.7.17/support-files/mysql.server /etc/init.d/mysqld
17. ** #修改启动文件内容(二进制安装需要修改)**

sed 's#/usr/local#/application#g' /application/mysql-5.7.17/bin/mysqld_safe /etc/init.d/mysqld -i
18. ** #启动**

/etc/init.d/mysqld start

[root@f85ea4ee6872 ~]# /etc/init.d/mysqld start
Starting MySQL.Logging to '/application/mysql-5.7.17/data/f85ea4ee6872.err'.
2017-11-14T04:39:18.059486Z mysqld_safe Directory '/application/mysql-5.7.17/tmp' for UNIX socket file don't exists.
 ERROR! The server quit without updating PID file (/application/mysql-5.7.17/data/f85ea4ee6872.pid).

mkdir -p /application/mysql-5.7.17/tmp
chown -R mysql.mysql /application/mysql-5.7.17/tmp


19. ** #修改root密码**

mysqladmin -uroot -p password '123456'






mysql> select user,host,password from mysql.user;
ERROR 1054 (42S22): Unknown column 'password' in 'field list'
mysql> select user,host from mysql.user;
+-----------+-----------+
| user      | host      |
+-----------+-----------+
| mysql.sys | localhost |
| root      | localhost |
+-----------+-----------+
2 rows in set (0.01 sec)














5. **体系结构原理**

MySQL是一个典型的C/S服务架构

20. ** mysql自带的客户端程序**

mysql
mysqladmin
mysqldump
21. ** mysqld服务端程序  **

二进制的程序，一个后台的守护进程
单进程多线程的服务结构
![图片](https://images-cdn.shimo.im/WKpxrQxI7eIAvoo8/image.image/png!thumbnail)




| 环境变量   | 描述   |
|:----|:----|
| AUTHENTICATION_LDAP_CLIENT_LOG   | 客户端LDAP身份验证日志记录级别。   |
| AUTHENTICATION_PAM_LOG   | [PAM](https://dev.mysql.com/doc/refman/5.7/en/pam-pluggable-authentication.html#pam-pluggable-authentication-debugging) 身份验证插件调试日志记录设置。   |
| CC   | C编译器的名称（用于运行**CMake**）。   |
| CXX   | C ++编译器的名称（用于运行**CMake**）。   |
| CC   | C编译器的名称（用于运行**CMake**）。   |
| DBI_USER   | Perl DBI的默认用户名。   |
| DBI_TRACE   | Perl DBI的跟踪选项。   |
| HOME   | [mysql](https://dev.mysql.com/doc/refman/5.7/en/mysql.html)历史文件的默认路径是 $HOME/.mysql_history。   |
| LD_RUN_PATH   | 用于指定的位置libmysqlclient.so。   |
| LIBMYSQL_ENABLE_CLEARTEXT_PLUGIN   | 启用mysql_clear_password身份验证插件; 请参见[第6.4.1.6节“客户端明文可插入认证”](https://dev.mysql.com/doc/refman/5.7/en/cleartext-pluggable-authentication.html)。   |
| LIBMYSQL_PLUGIN_DIR   | 查找客户端插件的目录。   |
| LIBMYSQL_PLUGINS   | 客户端插件预加载。   |
| MYSQL_DEBUG   | 调试时调试跟踪选项。   |
| MYSQL_GROUP_SUFFIX   | 选项组后缀值（如指定 [--defaults-group-suffix](https://dev.mysql.com/doc/refman/5.7/en/option-file-options.html#option_general_defaults-group-suffix)）。   |
| MYSQL_HISTFILE   | [mysql](https://dev.mysql.com/doc/refman/5.7/en/mysql.html)历史文件的路径。如果设置了此变量，则其值将覆盖默认值 $HOME/.mysql_history。   |
| MYSQL_HISTIGNORE   | 模式指定[mysql](https://dev.mysql.com/doc/refman/5.7/en/mysql.html)不应该记录的语句$HOME/.mysql_history，或者 syslog是否 [--syslog](https://dev.mysql.com/doc/refman/5.7/en/mysql-command-options.html#option_mysql_syslog)给出。   |
| MYSQL_HOME   | 服务器特定my.cnf文件所在目录的路径 。   |
| MYSQL_HOST   | [mysql](https://dev.mysql.com/doc/refman/5.7/en/mysql.html)命令行客户端使用的默认主机名。   |
| MYSQL_OPENSSL_UDF_DH_BITS_THRESHOLD   | 最大密钥长度 [CREATE_DH_PARAMETERS()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-dh-parameters)。请参见 [第12.19.2节“MySQL Enterprise Encryption用法和示例”](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-usage.html)。   |
| MYSQL_OPENSSL_UDF_DSA_BITS_THRESHOLD   | 最大DSA密钥长度 [CREATE_ASYMMETRIC_PRIV_KEY()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-asymmetric-priv-key)。请参见[第12.19.2节“MySQL Enterprise Encryption用法和示例”](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-usage.html)。   |
| MYSQL_OPENSSL_UDF_RSA_BITS_THRESHOLD   | 最大RSA密钥长度 [CREATE_ASYMMETRIC_PRIV_KEY()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-asymmetric-priv-key)。请参见[第12.19.2节“MySQL Enterprise Encryption用法和示例”](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-usage.html)。   |
| MYSQL_PS1   | 要在[mysql](https://dev.mysql.com/doc/refman/5.7/en/mysql.html)命令行客户端中使用的命令提示符。   |
| MYSQL_PWD   | 连接[mysqld](https://dev.mysql.com/doc/refman/5.7/en/mysqld.html)时的默认密码。使用它是不安全的。请参见 [第6.1.2.1节“密码安全的最终用户指南”](https://dev.mysql.com/doc/refman/5.7/en/password-security-user.html)。   |
| MYSQL_TCP_PORT   | 默认的TCP / IP端口号。   |
| MYSQL_TEST_LOGIN_FILE   | .mylogin.cnf登录路径文件的名称。   |
| MYSQL_TEST_TRACE_CRASH   | 测试协议跟踪插件是否会崩溃客户端。见下表注释。   |
| MYSQL_TEST_TRACE_DEBUG   | 测试协议跟踪插件是否产生输出。见下表注释。   |
| MYSQL_UNIX_PORT   | 默认的Unix套接字文件名; 用于连接 localhost。   |
| MYSQLX_TCP_PORT   | X Plugin默认的TCP / IP端口号。   |
| MYSQLX_UNIX_PORT   | X Plugin默认的Unix套接字文件名; 用于连接localhost。   |
| PATH   | 用于shell来查找MySQL程序。   |
| PKG_CONFIG_PATH   | 的位置mysqlclient.pc **pkg配置**文件。见下表注释。   |
| TMPDIR   | 创建临时文件的目录。   |
| TZ   | 这应该设置为您当地的时区。请参见 [第B.6.3.7节“时区问题”](https://dev.mysql.com/doc/refman/5.7/en/timezone-problems.html)。   |
| UMASK   | 创建文件时的用户文件创建模式。见下表注释。   |
| UMASK_DIR   | 创建目录时的用户目录创建模式。见下表注释。   |
| USER   | 连接到[mysqld](https://dev.mysql.com/doc/refman/5.7/en/mysqld.html)时Windows上的默认用户名 。   |





22. ** MySQL的连接方式**

网络连接（TCP/IP）
mysql -uroot -poldboy123 -h 10.0.0.51
套接字（socket）
mysql -uroot -poldboy123 -S /tmp/mysql.sock

查看二进制文件内容
strings /application/mysql/bin/mysql |grep mysql.sock



6. ** MySQL的多实例**
23. **多实例是什么**

一台机器上开启多个不同的服务端口（如：3306,3307）
运行多个MySQL服务进程，这些实例公用一套MySQL安装程序，
使用不同的my.cnf配置文件，启动程序，数据文件。
在提供服务时，多实例MySQL在逻辑上看来是各自独立的，
多个实例的自身是根据配置文件对应的设定值，来取得服务器的
相关硬件资源的多少。很多服务都可以有多个实例，
例如：nginx，apache，haproxy，memcache等等

24. **多实例的作用与问题**

1、有效利用服务器资源，充分利用剩余的资源提供更多的服务
2、节约服务器资源，需要主从同步等技术时，多实例就再好不过了
3、资源互抢问题，当某个服务实例并发很高或者慢查询时，
整个实例会消耗更多的内存、CPU、磁盘IO资源

25. **多实例生产场景应用**

1、资金紧张型公司的选择
2、并发访问不是特别大的业务
3、门户网站应用MySQL多实例的场景

26. **配置方案**

1、多个配置文件，多个启动程序（比较好，推荐）
2、单一配置文件，多个启动程序（官方推荐，耦合性太高，不好）

单机运行1~4个数据库实例







27. ** mysql多实例启动脚本**

/data/3306/mysql
#!/bin/sh
################################################
#this scripts is created by wuxingge at 2018-03-31
#wuxingge QQ:1226032602
#site:http://www.oldboyedu.com
#oldboy trainning QQ group: 208160987 226199307  44246017
################################################
#init
port=3306
mysql_user="root"
CmdPath="/application/mysql/bin"
mysql_sock="/data/${port}/mysql.sock"
mysqld_pid_file_path=/data/3306/mysql.pid
start(){
    if [ ! -e "$mysql_sock" ];then
      printf "Starting MySQL...\n"
        /bin/sh ${CmdPath}/mysqld_safe --defaults-file=/data/${port}/my.cnf --user=root 2>&1 > /dev/null &
        sleep 3
    else
        printf "MySQL is running...\n"
        exit 1
    fi
}
stop(){
    if [ ! -e "$mysql_sock" ];then
        printf "MySQL is stopped...\n"
        exit 1
    else
        printf "Stoping MySQL...\n"
        mysqld_pid=`cat "$mysqld_pid_file_path"`
         if (kill -0 $mysqld_pid 2>/dev/null)
           then
             kill $mysqld_pid
             sleep 2
         fi
    fi
}

restart(){
    printf "Restarting MySQL...\n"
    stop
    sleep 2
    start
}

case "$1" in
    start)
        start
    ;;
    stop)
        stop
    ;;
    restart)
        restart
    ;;
    *)
        printf "Usage: /data/${port}/mysql {start|stop|restart}\n"
esac












28. ** 主配置文件my.cnf**

/etc/my.cnf
......

log_bin = /application/mysqlbinlog/mysql-bin
binlog_cache_size = 4M
max_binlog_cache_size = 2G
max_binlog_size = 1G
expire_logs_days = 7
binlog-ignore-db = mysql
replicate-ignore-db = mysql
skip-name-resolve
......


[client]
port            = 3306
socket          = /data/3306/mysql.sock

[mysql]
no-auto-rehash

[mysqld]
user    = mysql
port    = 3306
socket  = /data/3306/mysql.sock
basedir = /application/mysql
datadir = /data/3306/data
open_files_limit    = 1024
back_log = 600
max_connections = 800
max_connect_errors = 3000
table_open_cache = 614
external-locking = FALSE
max_allowed_packet =8M
sort_buffer_size = 1M
join_buffer_size = 1M
thread_cache_size = 100
thread_concurrency = 2
query_cache_size = 2M
query_cache_limit = 1M
query_cache_min_res_unit = 2k
#default_table_type = InnoDB
thread_stack = 192K
#transaction_isolation = READ-COMMITTED
tmp_table_size = 2M
max_heap_table_size = 2M
#long_query_time = 1
#log_long_format
#log-error = /data/3306/error.log
#log-slow-queries = /data/3306/slow.log
pid-file = /data/3306/mysql.pid
#log-bin = /data/3306/mysql-bin
relay-log = /data/3306/relay-bin
relay-log-info-file = /data/3306/relay-log.info
binlog_cache_size = 1M
max_binlog_cache_size = 1M
max_binlog_size = 2M
expire_logs_days = 7
key_buffer_size = 16M
read_buffer_size = 1M
read_rnd_buffer_size = 1M
bulk_insert_buffer_size = 1M
lower_case_table_names = 1
skip-name-resolve
slave-skip-errors = 1032,1062
replicate-ignore-db=mysql
server-id = 6
innodb_additional_mem_pool_size = 4M
innodb_buffer_pool_size = 32M
#innodb_data_file_path = ibdata1:128M:autoextend
innodb_file_io_threads = 4
innodb_thread_concurrency = 8
innodb_flush_log_at_trx_commit = 2
innodb_log_buffer_size = 2M
innodb_log_file_size = 4M
innodb_log_files_in_group = 3
innodb_max_dirty_pages_pct = 90
innodb_lock_wait_timeout = 120
innodb_file_per_table = 0
[mysqldump]
quick
max_allowed_packet = 2M

[mysqld_safe]
log-error=/data/3306/mysql_3306.err
pid-file=/data/3306/mysql.pid


29. ** 数据目录授权**

chown -R mysql.mysql /data/3306

30. ** mysql实例初始化**

/application/mysql/scripts/mysql_install_db --user=mysql --basedir=/application/mysql/ --datadir=/data/3306/data/














7. ** my.cnf**

https://dev.mysql.com/doc/refman/5.6/en/server-default-changes.html
https://dev.mysql.com/doc/refman/5.6/en/mysqld-option-tables.html
[mysqld]
basedir=/application/mysql
datadir=/application/mysql/data
socket=/tmp/mysql.sock
log-error=/var/log/mysql.log
log_bin=/data/mysql/mysql-bin
binlog_format=row
skip_name_resolve=1
server_id=3306
port=3306

[mysql]
user=root
password=oldboy123
[mysqladmin]
user=root
password=oldboy123

/etc/my.cnf
[server]
basedir=/application/mysql
datadir=/application/mysql/data
socket=/tmp/mysql.sock
log-error=/var/log/mysql.log
log_bin=/data/mysql/mysql-bin
binlog_format=row
skip_name_resolve=1
server_id=3306    

[client]
socket=/tmp/mysql.sock

31. ** mysql配置文件读取顺序**

https://dev.mysql.com/doc/refman/5.6/en/option-files.html

/etc/my.cnf
/etc/mysql/my.cnf
$MYSQL_HOME/my.cnf
~/.my.cnf
defaults-extra-file
--defaults-file


| /etc/my.cnf   | 全球选择   |
|:----|:----|
| /etc/mysql/my.cnf   | 全球选择   |
| ***SYSCONFDIR***/my.cnf   | 全球选择   |
| $MYSQL_HOME/my.cnf   | 特定于服务器的选项（仅限服务器）   |
| defaults-extra-file   | 指定的文件 [--defaults-extra-file](https://dev.mysql.com/doc/refman/5.7/en/option-file-options.html#option_general_defaults-extra-file)，如果有的话   |
| ~/.my.cnf   | 用户特定选项   |
| ~/.mylogin.cnf   | 用户特定的登录路径选项（仅限客户端）   |




mysqld先读取命令行配置，找不到，就读取配置文件，找不到，读取编译时的配置，最后读取mysqld默认的配置


Zabbix Agent获取MySQL数据
/etc/zabbix/.my.cnf
[mysql]
host = localhost
user = root
password = 123456
[mysqladmin]
host = localhost
user = root
password = 123456












32. ** 多实例**

3307
 [mysqld]
basedir=/application/mysql
datadir=/data/3307
socket=/data/3307/mysql.sock
log-error=/data/3307/mysql.log
log_bin=/data/3307/mysql-bin
binlog_format=row
skip_name_resolve=1
server_id=3307
port=3307

3308
[mysqld]
basedir=/application/mysql
datadir=/data/3308
socket=/data/3308/mysql.sock
log-error=/data/3308/mysql.log
log_bin=/data/3308/mysql-bin
binlog_format=row
skip_name_resolve=1
server_id=3308
port=3308
3309
[mysqld]
basedir=/application/mysql
datadir=/data/3309
socket=/data/3309/mysql.sock
log-error=/data/3309/mysql.log
log_bin=/data/3309/mysql-bin
binlog_format=row
skip_name_resolve=1
server_id=3309
port=3309

8. **mysql常用操作**
33. ** mysql**

mysql
-u  用户名
-p  密码
-h  mysql服务器ip地址
-S  套接字
-P  端口

34. **  mysql 登录**

mysql -uroot -poldboy -S /data/3306/mysql.sock
35. ** mysql 远程登录**

mysql -h 10.0.0.51 -uoldboy -p123456 -S /data/3308/mysql.sock -P3308

36. ** 登录数据库以后切换实例**

mysql> system mysql -S /data/3307/mysql.sock



37. ** 查看用户具有的权限**

mysql> show grants for oldboy@'172.16.1.%'\G;

38. ** 设置管理员密码**

mysqladmin -S /data/3306/mysql.sock -uroot password 'oldboy'



39. ** 修改管理员密码**

mysqladmin -S /data/3306/mysql.sock -uroot -p password 'oldboy123'









40. **跳过用户登录mysql**

第一步：修改对应实例的配置文件
vim my.cnf
[mysqld]        在这个标签下添加
**skip-grant-tables**
重启mysql实例
第二步：登录mysql实例
**mysql -S /data/3306/mysql.sock**


killall mysqld
**mysqld_safe --defaults-file=/data/3308/my.cnf --skip-grant-table &    **
mysql -uroot -p -S /data/3308/mysql.sock
mysql> update mysql.user set password = password("123456") where user = 'root'  and  host = 'localhost';
flush privileges;

--skip-networking   禁止远程连接

41. ** mysql停止（优雅关闭）**

1、
mysqladmin -uroot -p shutdown
2、
/.../.../mysql  stop
3、
kill -USR2 `cat patth/pid`



42. **  命令前加空格，历史记录不显示**

export HISTCONTROL=ignorespace

43. ** 添加超级用户**

mysql> grant all on *.* to admin@'%' identified by 'oldboy123' **with grant option**;

44. ** 超级用户登录**

mysql -h 10.0.0.51 -uadmin -poldboy123 -P3306


45. ** sql语句修改用户密码**

修改密码
mysql> update mysql.user set password=password('oldboy') where user='root' and host='localhost';

刷新权限
mysql> flush privileges;


46. ** 临时修改mysql提示符**

mysql> prompt **\u@\h**>
PROMPT set to '\u@\h>'
**root@localhost**>prompt **mysql**>
PROMPT set to 'mysql>'
**mysql**>

mysql>prompt **\u**>
PROMPT set to '\u>'
**root**>




47. **查看mysql版本**
12. **方法1**

mysql>** \s**
--------------
mysql  Ver 14.14 Distrib 5.5.32, for Linux (x86_64) using readline 5.1

Connection id:          2
Current database:       mysql
Current user:           root@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server version:         5.5.32-log Source distribution
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    utf8
Db     characterset:    utf8
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /data/3306/mysql.sock
Uptime:                 23 min 24 sec

Threads: 2  Questions: 23  Slow queries: 0  Opens: 37  Flush tables: 1  Open tables: 30  Queries per second avg: 0.016
13. **方法2**

mysql> **select version();**
+------------+
| version()  |
+------------+
| 5.5.32-log |
+------------+
1 row in set (0.00 sec)


查看错误代码含义
perror 1505


9. **sql语句**

[https://dev.mysql.com/doc/refman/5.7/en/sql-syntax.html](https://dev.mysql.com/doc/refman/5.7/en/sql-syntax.html)

[https://dev.mysql.com/doc/refman/5.7/en/functions.html](https://dev.mysql.com/doc/refman/5.7/en/functions.html)

[http://www.runoob.com/sql/sql-tutorial.html](http://www.runoob.com/sql/sql-tutorial.html)



48. ** sql分类**

DDL(Data Definition Language)-数据定义语言（create  alter  drop）管理基础数据，
例如：库、表  **运维要熟练，开发也要熟练**

DCL(Data Control Language)-数据控制语言（grant  revoke  commit  rollback），
用户授权、权限回收、数据提交回滚等   **运维要熟练**

DML(Data Manipulation Language)-数据操作语言（select  insert  delete  update），
针对数据库里的表里的数据进行操作，记录   **开发要熟练，运维要了解**


49. ** 数据库中的包含关系**

数据库服务器---》数据库（多个实例）---》多个库---》多个表---》多个字段(列)、记录(行)（数据）




















50. ** 帮助**

mysql> **? contents;**
You asked for help about help category: "Contents"
For more information, type 'help <item>', where <item> is one of the following
categories:
   Account Management
   Administration
   Compound Statements
   Data Definition
   Data Manipulation
   Data Types
   Functions
   Functions and Modifiers for Use with GROUP BY
   Geographic Features
   Help Metadata
   Language Structure
   Plugins
   Procedures
   Storage Engines
   Table Maintenance
   Transactions
   User-Defined Functions
   Utility


10. ** 库操作**

第一步在mysql下执行：rehash;
第二步use在一个库中：use mysql;然后就可以愉快的使用了

51. **创建数据库**

create database <数据库名>;
52. **查看已经创建的数据库信息**

show create database oldboy\G;
53. **创建数据库指定字符集**

mysql> create database oldgirl CHARACTER SET** gbk** COLLATE **gbk_chinese_ci**;
mysql>create database abc character set **utf8** collate **utf8_general_ci**;
54. **查看字符集和校对规则**

show character set;
55. **创建不同字符集格式的数据库命令**

create database oldboy; <==默认数据库配置，相当于创建拉丁字符集数据库。
create database oldboy_gbk DEFAULT CHARACTER SET **gbk** COLLATE **gbk_chinese_ci**; #<==创建gbk字符集数据库
create database oldboy_utf8 DEFAULT CHARACTER SET **utf8** COLLATE **utf8_general_ci**;<==创建utf8字符集数据库
56. **查看数据库**

show databases like '%boy%';
57. **查看当前所在数据库**

mysql> select database();
+------------+
| database() |
+------------+
| NULL       |
+------------+
1 row in set (0.02 sec)
58. **进入某个库**

mysql> use mysql;
Database changed

11. **表结构操作**
59. **查看一个库中的表**

mysql> show tables;
+---------------------------+
| Tables_in_mysql           |
+---------------------------+
| columns_priv              |
| db                        |
| event                     |
| func                      |
| general_log               |
| help_category             |
| help_keyword              |
| help_relation             |
| help_topic                |
| host                      |
| ndb_binlog_index          |
| plugin                    |
| proc                      |
| procs_priv                |
| proxies_priv              |
| servers                   |
| slow_log                  |
| tables_priv               |
| time_zone                 |
| time_zone_leap_second     |
| time_zone_name            |
| time_zone_transition      |
| time_zone_transition_type |
| user                      |
+---------------------------+
24 rows in set (0.18 sec)


60. **创建表**

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

```
CREATE TABLE `test` (
`id` int(4) NOT NULL AUTO_INCREMENT,
`name` char(20) NOT NULL,
PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=UTF8;
```


14. ** 创建一个表与之前的表结构相同**
```
create table student_0 like student;
```


15. ** 创建一个备份表**
```
create table t1_1 as select * from t1;
```



61. ** 查看已创建表的语句**
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

62. ** 查看表结构**
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








63. ** 生产场景创建的表**

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






64. ** 增加字段**

alter table 表名 add字段 类型 其他;

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



```
alter table test add sex char(4);    #←增加性别列sex
alter table test add age int(4) after name;   在name字段后面添加age字段
alter table test add qq varchar(15) first;    在表最前面
```






16. **增加1个字段：**

ALTER TABLE `etiantian` ADD `FIRSTPHOTO_URL` varchar(255) default NULL COMMENT '第一张图片URL'

17. **增2个字段：**

ALTER TABLE `basic` ADD `adhtml_top`  varchar(1024) default NULL COMMENT '顶部广告html' ,
                                           ADD `adhtml_right` varchar(1024) default NULL COMMENT '右侧广告html' ;

65. ** 改变字段：**

alter table ett_ambiguity change ambiguity_state  ambiguity_state tinyint  comment '状态，默认1=正常，0=失效';
ALTER TABLE `ett_photo`
MODIFY COLUMN `PHOTO_DESCRIPTION` varchar(512) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '描述' AFTER PHOTO_TITLE`;

66. ** 修改字段类型：**
```
mysql> alter table test modify age char(4) after name;
Query OK, 6 rows affected (0.00 sec)
Records: 6  Duplicates: 0  Warnings: 0
```


67. ** 修改字段名称**
```
mysql> alter table test change age oldboyage char(4) after name;
Query OK, 6 rows affected (0.01 sec)
Records: 6  Duplicates: 0  Warnings: 0
```
提示：工作中添加字段需求来自开发，运维或DBA拿着开发给的语句执行。




68. ** 修改表名**

mysql> **rename table test to oldboy;**
Query OK, 0 rows affected (0.00 sec)

mysql> show tables;                
+------------------+
| Tables_in_oldboy |
+------------------+
| course           |
| oldboy           |
| sc               |
| student          |
| test1            |
+------------------+
5 rows in set (0.00 sec)

mysql> **alter table oldboy rename to test;**
Query OK, 0 rows affected (0.00 sec)

mysql> show tables;                      
+------------------+
| Tables_in_oldboy |
+------------------+
| course           |
| sc               |
| student          |
| test             |
| test1            |
+------------------+
5 rows in set (0.00 sec)







12. ** 表内容操作**
69. ** 插入数据**

insert into 表名(字段名1,字段名2,...) values(值1,值2,...);

create table test(
id int(4) not null auto_increment,
name char(20) not null,
primary key(id)
);

mysql> **insert into test(id,name) values(1,'oldboy');**
Query OK, 1 row affected (0.00 sec)

mysql> select * from test;
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
+----+--------+
1 row in set (0.00 sec)

mysql> **insert into test(name) values('oldgirl');**
Query OK, 1 row affected (0.02 sec)

mysql> select * from test;
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
+----+---------+
2 rows in set (0.00 sec)


mysql>** insert into test values(3,'inca'); **
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


70. ** 批量插入数据**

mysql>** insert into test values(4,'zuma'),(5,'kaka');**
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



insert into student_0 select * from student;



71. ** 清空表中所有数据**

mysql> **truncate table test;**
Query OK, 0 rows affected (0.00 sec)

mysql> select * from test;
Empty set (0.00 sec)

mysql> **insert into test values(1,'oldboy'),(2,'oldgirl'),(3,'inca'),(4,'zuma'),(5,'kaka');**
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

补充强调：我们平时登录网站发帖子，发博文，实质上都是调用web网站的程序连接MySQL数据库，通过上述的insert语句把帖子博文数据存入数据库的。




72. ** 查询**

 查询中用到的关键词主要包含六个，并且他们的顺序依次为 
**select----from----where-----group by-----having------order by **
 

其中select和from是必须的，其他关键词是可选的，这六个关键词的执行顺序 
与sql语句的书写顺序并不是一样的，而是按照下面的顺序来执行 
from--where--group by--having--select--order by, 
from:需要从哪个数据表检索数据 
where:过滤表中数据的条件 
group by:如何将上面过滤出的数据分组 
having:对上面已经分组的数据进行过滤的条件  
select:查看结果集中的哪个列，或列的计算结果 
order by :按照什么样的顺序来查看返回的数据 




mysql> **select id,name from oldboy.test;**
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+












mysql>** select * from test limit 2;**
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
+----+---------+
2 rows in set (0.00 sec)

mysql> **select * from test limit 3;**
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | oldgirl |
|  3 | inca    |
+----+---------+
3 rows in set (0.00 sec)

mysql>** select * from test limit 1,3;**
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
|  3 | inca    |
|  4 | zuma    |
+----+---------+
3 rows in set (0.00 sec)





mysql> **select * from test where name='oldboy';**
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
+----+--------+


mysql>** select * from test where id=5;**
+----+------+
| id | name |
+----+------+
|  5 | kaka |
+----+------+
1 row in set (0.00 sec)

mysql>** select * from test where name='oldgirl';**
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
+----+---------+
1 row in set (0.00 sec)

mysql> desc test
    -> ;
+-------+----------+------+-----+---------+----------------+
| Field | Type     | Null | Key | Default | Extra          |
+-------+----------+------+-----+---------+----------------+
| id    | int(4)   | NO   | PRI | NULL    | auto_increment |
| name  | char(20) | NO   |     | NULL    |                |
+-------+----------+------+-----+---------+----------------+
2 rows in set (0.00 sec)

mysql> select * from test where id>3 and name='oldgirl';
Empty set (0.00 sec)

mysql>** select * from test where id<3 and name='oldgirl';**
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
+----+---------+
1 row in set (0.00 sec)

mysql> **select * from test where id>3 or name='oldgirl';**
+----+---------+
| id | name    |
+----+---------+
|  2 | oldgirl |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
3 rows in set (0.00 sec)


mysql> **select * from test where id>3 or name='oldgirl' order by id desc;**
+----+---------+
| id | name    |
+----+---------+
|  5 | kaka    |
|  4 | zuma    |
|  2 | oldgirl |
+----+---------+
3 rows in set (0.00 sec)







73. ** 小结**

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










74. ** 多表联查**

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

75. ** 排序**

select * from city where countrycode='chn' order by population desc;









76. ** 限制limit**

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

77. ** in语句**

select name,population,countrycode from city where population in (2000000,3000000,4000000);

78. ** between  and**

select name,population,countrycode from city where population between 1000000 and 1000001;





79. ** group by**

[https://dev.mysql.com/doc/refman/5.7/en/group-by-handling.html](https://dev.mysql.com/doc/refman/5.7/en/group-by-handling.html)


group by + 聚合函数（最大值、最小值等）


先分组聚合再筛选
select countrycode ,sum(population) from city group by countrycode having countrycode='CHN';

先筛选在分组聚合
select countrycode ,sum(population) from city where countrycode='CHN' group by countrycode;


80. ** union  结果集合并  用来代替or**

按行合并

select name,population,countrycode from city where countrycode='CHN' union select name,population,countrycode from city where population >10000000;

union all




81. ** 多表连接查询**

## sql数据准备
```
CREATE DATABASE school CHARSET utf8;
USE school


CREATE TABLE student(
sno INT NOT NULL PRIMARY KEY AUTO_INCREMENT COMMENT '学号',
sname VARCHAR(20) NOT NULL COMMENT '姓名',
sage TINYINT UNSIGNED NOT NULL COMMENT '年龄',
ssex ENUM('f','m') NOT NULL DEFAULT 'm' COMMENT '性别'
)ENGINE=INNODB CHARSET=utf8;


CREATE TABLE course(
cno INT NOT NULL PRIMARY KEY COMMENT '课程编号',
cname VARCHAR(20) NOT NULL COMMENT '课程名字',
tno INT NOT NULL COMMENT '教师编号'
)ENGINE=INNODB CHARSET utf8;


CREATE TABLE sc (
sno INT NOT NULL COMMENT '学号',
cno INT NOT NULL COMMENT '课程编号',
score INT NOT NULL DEFAULT 0 COMMENT '成绩'
)ENGINE=INNODB CHARSET=utf8;



CREATE TABLE teacher(
tno INT NOT NULL PRIMARY KEY COMMENT '教师编号',
tname VARCHAR(20) NOT NULL COMMENT '教师名字'
)ENGINE=INNODB CHARSET utf8;


INSERT INTO student(sno,sname,sage,ssex)
VALUES (1,'zhang3',18,'m');


INSERT INTO student(sno,sname,sage,ssex)
VALUES
(2,'zhang4',18,'m'),
(3,'li4',18,'m'),
(4,'wang5',19,'f');


INSERT INTO student
VALUES
(5,'zh4',18,'m'),
(6,'zhao4',18,'m'),
(7,'ma6',19,'f');


INSERT INTO student(sname,sage,ssex)
VALUES
('oldboy',20,'m'),
('oldgirl',20,'f'),
('oldp',25,'m');


INSERT INTO teacher(tno,tname) VALUES
(101,'oldboy'),
(102,'hesw'),
(103,'oldguo');

DESC course;
INSERT INTO course(cno,cname,tno)
VALUES
(1001,'linux',101),
(1002,'python',102),
(1003,'mysql',103);

DESC sc;
INSERT INTO sc(sno,cno,score)
VALUES
(1,1001,80),
(1,1002,59),
(2,1002,90),
(2,1003,100),
(3,1001,99),
(3,1003,40),
(4,1001,79),
(4,1002,61),
(4,1003,99),
(5,1003,40),
(6,1001,89),
(6,1003,77),
(7,1001,67),
(7,1003,82),
(8,1001,70),
(9,1003,80),
(10,1003,96);
```






传统连接
where A.ID=B.ID
select ci.name,ci.countrycode,ci.population,co.name from city as ci,country as co where ci.countrycode=co.code and ci.population<100;











82. ** 内连接**
18. ** 自动连接 （natural join）**

两个表有相同的字段countrycode
select name,countrycode,language,population from city natural join countrylanguage where population > 1000000 order by population;


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





19. ** join**

上海市属于哪个国家
select ci.name,ci.countrycode,co.name from city as ci,country as co where ci.countrycode=co.code and ci.name='shanghai';

select ci.name,ci.countrycode,co.name from city as ci join country as co on ci.countrycode=co.code and ci.name='shanghai';

83. ** 外连接**
20. ** left join**

![图片](https://images-cdn.shimo.im/nUFVmjLvisYL11W9/image.image/png!thumbnail)
select ci.name,ci.countrycode,co.name from city as ci left join country as co on ci.countrycode=co.code and ci.name='shanghai';

21. ** right join**

![图片](https://images-cdn.shimo.im/KWZWiDPlQJElLcIN/image.image/png!thumbnail)











84. ** 子查询**

select name from country where code= (select countrycode from city where population > 10000000);

select chnt.name,chnt.population from (select name,countrycode,population from city where countrycode='CHN') chnt limit 10;

select chnt.name,chnt.population from (select name,countrycode,population from city where countrycode='CHN') chnt where chnt.population>5000000  limit 10;


85. ** 使用****explain****查看select语句的执行计划**

mysql>** explain select * from test where name='oldboy'\G**
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

mysql> **alter table test add index ind_name(name(8));**
Query OK, 0 rows affected (0.01 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql>** explain select * from test where name='oldboy'\G**
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

官方手册需要大家掌握的章节5,6,7,8,10,11,13,14,15








86. ** 更新数据**

update 表名 set 字段=新值,… where 条件（一定要注意条件）

mysql> **select * from test;**
+----+---------+
| id | name    |
+----+---------+
|  1 | oldboy  |
|  2 | **oldgirl** |
|  3 | inca    |
|  4 | zuma    |
|  5 | kaka    |
+----+---------+
5 rows in set (0.00 sec)

mysql> **update test set name='****gongli****' where name='****oldgirl****';**
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> **select * from test;**
+----+--------+
| id | name   |
+----+--------+
|  1 | oldboy |
|  2 | **gongli** |
|  3 | inca   |
|  4 | zuma   |
|  5 | kaka   |
+----+--------+
5 rows in set (0.00 sec)



一次更新多个字段
```
update mysql.user set
Select_priv='Y',
Insert_priv='Y',           
Update_priv='Y',            
Create_priv='Y', 
Delete_priv='Y',          
Drop_priv='Y',            
Reload_priv='Y',           
Shutdown_priv='Y',         
Process_priv='Y',          
File_priv='Y',             
Grant_priv='Y',            
References_priv='Y',       
Index_priv='Y',            
Alter_priv='Y',            
Show_db_priv='Y',          
Super_priv='Y',            
Create_tmp_table_priv='Y', 
Lock_tables_priv='Y',      
Execute_priv='Y',          
Repl_slave_priv='Y',       
Repl_client_priv='Y',      
Create_view_priv='Y',      
Show_view_priv='Y',        
Create_routine_priv='Y',   
Alter_routine_priv='Y',    
Create_user_priv='Y',      
Event_priv='Y',            
Trigger_priv='Y',          
Create_tablespace_priv='Y'
where user='root';
```





87. ** 防止误操作MySQL数据库一例**

在mysql命令加上选项-U后，当发出没有WHERE或LIMIT关键字的UPDATE或DELETE时，mysql程序就会拒绝执行
mysql -S /data/3306/mysql.sock -uroot -poldboy** -U**



88. ** 删除数据**
22. ** 一行一行的删除**

mysql> **delete from test where id=3;**
Query OK, 1 row affected (0.00 sec)

mysql> select * from test;         
+----+--------+
| id | name   |
+----+--------+
|  1 | gongli |
|  2 | gongli |
|  4 | gongli |
|  5 | gongli |
+----+--------+
4 rows in set (0.00 sec)

23. **全部删除数据**

mysql> **truncate table test;**
Query OK, 0 rows affected (0.00 sec)

适用场景：drop table 可以先 truncate table  ，然后 drop table










24. ** 通过状态删除表中的数据（update代替delete）**

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

# 删除数据
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



89. ** 逻辑删除数据实例**

mysql> alter table test add state tinyint(2);
Query OK, 4 rows affected (0.03 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from test where state=1;     
Empty set (0.00 sec)

mysql> desc test;
+-------+------------+------+-----+---------+----------------+
| Field | Type       | Null | Key | Default | Extra          |
+-------+------------+------+-----+---------+----------------+
| id    | int(4)     | NO   | PRI | NULL    | auto_increment |
| name  | char(20)   | NO   | MUL | NULL    |                |
| state | tinyint(2) | YES  |     | NULL    |                |
+-------+------------+------+-----+---------+----------------+
3 rows in set (0.00 sec)

mysql> select * from test;
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |  NULL |
|  2 | gongli |  NULL |
|  4 | gongli |  NULL |
|  5 | gongli |  NULL |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> update test set state='1';    
Query OK, 4 rows affected (0.00 sec)
Rows matched: 4  Changed: 4  Warnings: 0

mysql> select * from test;       
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  4 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> select * from test where state=1;
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  4 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
4 rows in set (0.00 sec)

mysql> update test set state='0' where id=4;
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from test where state=1;    
+----+--------+-------+
| id | name   | state |
+----+--------+-------+
|  1 | gongli |     1 |
|  2 | gongli |     1 |
|  5 | gongli |     1 |
+----+--------+-------+
3 rows in set (0.00 sec)





13. **数据类型**

[https://dev.mysql.com/doc/refman/5.7/en/data-types.html](https://dev.mysql.com/doc/refman/5.7/en/data-types.html)

90. ** 数字**
| 字段类型   | 占存储空间   |
|:----|:----:|:----|:----:|
| TINYINT   | 1B   |
| SMALLINT   | 2B   |
| MEDIUMINT   | 3B   |
| INT   | 4B   |
| INTEGER   | 4B   |
| BIGINT   | 8B   |
| FLOAT(X)   | 4 如果X<=24  或 8 如果25<=X<=53    |
| FLOAT   | 4B   |
| DOUBLE   | 8B   |
| DOUBLE PRECISION   | 8B   |
| REAL   | 8B   |


91. ** 日期和时间类型**
| 字段类型   | 占存储空间   |
|:----|:----:|:----|:----:|
| DATE   | 3B   |
| DATETIME   | 8B   |
| TIMESTAMP   | 4B   |
| TIME   | 3B   |
| YEAR   | 1B   |


alter table student add bridate datetime;

insert into student values(1,'zhang3',12,'1',now());








92. ** 字符串类型**
| 字段类型   | 占存储空间   |
|:----|:----:|:----|:----:|
| CHAR(M)   | M字节，1<=M<=255   |
| VARCHAR(M)   | L+1 字节，在此 L<=M和1<=M<=255   |
| TINYBLOB,TINYTEXT   | L+1字节，在此L<2^8   |
| BLOB, TEXT   | L+2字节，在此L<2^16   |
| MEDIUMBLOB,  MEDIUMTEXT   | L+3字节，在此L<2^24   |
| LONGBLOB,  LONGTEXT   | L+4 字节，在此L<2^32   |
| ENUM('value1','value2',...)   | 1或2 字节，取决于枚举值的数目（最大值65535）   |
| SET('value1','value2',...)   | 1,2,3,4或8字节，取决于集合成员的数量（最多64个成员）   |



93. ** 列属性**
| 数据类型   | 属性   | 说明   |
|:----|:----:|:----|:----:|:----|:----:|
| 数值   | unsigned   | 无符号   |
| 仅整数   | AUTO_INCREMENT   | 生成包含连续唯一整数值的序列   |
| 字符串   | CHARACTER SET   | 指定要使用的字符集   |
| 字符串   | COLLATE   | 指定字符集校对规则   |
| 字符串   | BINARY   | 指定二进制整理   |
| 全部   | NULL或NOT NULL   | 指示列是否可以包含NULL值   |
| 全部   | DEFAULT   | 如果未为新记录指定值，则为其提供默认值   |







94. ** 数据类型 CHAR和VARCHAR的区别**

[https://dev.mysql.com/doc/refman/5.7/en/char.html](https://dev.mysql.com/doc/refman/5.7/en/char.html)
| 值   | CHAR(4)   | 存储空间   | VARCHAR(4)   | 存储空间   |
|:----|:----:|:----|:----:|:----|:----:|:----|:----:|:----|:----:|
| ''   | '    '   | 4B   | ''   | 1B   |
| 'ab'   | 'ab  '   | 4B   | 'ab'   | 3B   |
| 'abcd'   | 'abcd'   | 4B   | 'abcd'   | 5B   |
| 'abcdefgh'   | 'abcd'   | 4B   | 'abcd'   | 5B   |


小结：
1、char定长，不够的用空格补全，浪费存储空间，**查询速度快****，****多数系统表字段都是定长**
2、varchar变长，查询速度慢

95. ** 如何选择数据类型**

考虑哪些数据类型和字符集可以最大限度地减少存储和磁盘I/O
使用固定长度数据类型：
–如果存储的所有字符串值的长度相同

使用可变长度数据类型：
–如果存储的字符串值不同
–对于多字节字符集

对于频繁使用的字符，使用占用空间较少的多字节字符集
–使用基本多文种平面(Basic Multilingual Plane, BMP) 之外的其他Unicode 字符集。



# 函数
[https://dev.mysql.com/doc/refman/5.7/en/func-op-summary-ref.html](https://dev.mysql.com/doc/refman/5.7/en/func-op-summary-ref.html)

| [ABS()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_abs)   | 返回绝对值   |
|:----|:----|
| [ACOS()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_acos)   | 返回反余弦   |
| [ADDDATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_adddate)   | 将时间值（间隔）添加到日期值   |
| [ADDTIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_addtime)   | 添加时间   |
| [AES_DECRYPT()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_aes-decrypt)   | 使用AES解密   |
| [AES_ENCRYPT()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_aes-encrypt)   | 使用AES加密   |
| [AND](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_and)[， ](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_and)[&&](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_and)   | 逻辑和   |
| [ANY_VALUE()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_any-value)   | 抑制ONLY_FULL_GROUP_BY值拒绝   |
| [Area()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_area) （已弃用5.7.6）   | 返回Polygon或MultiPolygon区域   |
| [AsBinary()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_asbinary)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_asbinary)[AsWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_asbinary)（已弃用5.7.6）   | 从内部几何格式转换为WKB   |
| [ASCII()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ascii)   | 返回最左侧字符的数值   |
| [ASIN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_asin)   | 返回圆弧正弦   |
| [=](https://dev.mysql.com/doc/refman/5.7/en/assignment-operators.html#operator_assign-equal)   | 分配值（作为[SET](https://dev.mysql.com/doc/refman/5.7/en/set-variable.html) 语句的一部分 ，或作为语句中SET子句的 一部分[UPDATE](https://dev.mysql.com/doc/refman/5.7/en/update.html)）   |
| [:=](https://dev.mysql.com/doc/refman/5.7/en/assignment-operators.html#operator_assign-value)   | 分配值   |
| [AsText()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_astext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_astext)[AsWKT()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_astext)（已弃用5.7.6）   | 从内部几何格式转换为WKT   |
| [ASYMMETRIC_DECRYPT()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_asymmetric-decrypt)   | 使用私钥或公钥解密密文   |
| [ASYMMETRIC_DERIVE()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_asymmetric-derive)   | 从非对称密钥导出对称密钥   |
| [ASYMMETRIC_ENCRYPT()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_asymmetric-encrypt)   | 使用私钥或公钥加密明文   |
| [ASYMMETRIC_SIGN()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_asymmetric-sign)   | 从摘要生成签名   |
| [ASYMMETRIC_VERIFY()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_asymmetric-verify)   | 验证签名是否与摘要匹配   |
| [ATAN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_atan)   | 返回反正切   |
| [ATAN2()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_atan2)[， ](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_atan2)[ATAN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_atan2)   | 返回两个参数的反正切   |
| [AVG()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_avg)   | 返回参数的平均值   |
| [BENCHMARK()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_benchmark)   | 反复执行表达式   |
| [BETWEEN ... AND ...](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_between)   | 检查值是否在值范围内   |
| [BIN()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_bin)   | 返回包含数字的二进制表示的字符串   |
| [BINARY](https://dev.mysql.com/doc/refman/5.7/en/cast-functions.html#operator_binary)   | 将字符串转换为二进制字符串   |
| [BIT_AND()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_bit-and)   | 按位返回AND   |
| [BIT_COUNT()](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#function_bit-count)   | 返回设置的位数   |
| [BIT_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_bit-length)   | 以位为单位返回参数长度   |
| [BIT_OR()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_bit-or)   | 按位返回OR   |
| [BIT_XOR()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_bit-xor)   | 按位返回异或   |
| [&](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_bitwise-and)   | 按位AND   |
| [~](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_bitwise-invert)   | 按位反转   |
| [\|](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_bitwise-or)   | 按位OR   |
| [^](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_bitwise-xor)   | 按位异或   |
| [Buffer()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_buffer) （已弃用5.7.6）   | 返回距离几何体的给定距离内的点的几何   |
| [CASE](https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html#operator_case)   | 案例运营商   |
| [CAST()](https://dev.mysql.com/doc/refman/5.7/en/cast-functions.html#function_cast)   | 将值转换为特定类型   |
| [CEIL()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_ceil)   | 返回不小于参数的最小整数值   |
| [CEILING()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_ceiling)   | 返回不小于参数的最小整数值   |
| [Centroid()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_centroid) （已弃用5.7.6）   | 返回质心作为一个点   |
| [CHAR()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_char)   | 返回传递的每个整数的字符   |
| [CHAR_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_char-length)   | 返回参数中的字符数   |
| [CHARACTER_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_character-length)   | CHAR_LENGTH（）的同义词   |
| [CHARSET()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_charset)   | 返回参数的字符集   |
| [COALESCE()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_coalesce)   | 返回第一个非NULL参数   |
| [COERCIBILITY()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_coercibility)   | 返回字符串参数的归类强制性值   |
| [COLLATION()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_collation)   | 返回字符串参数的排序规则   |
| [COMPRESS()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_compress)   | 将结果作为二进制字符串返回   |
| [CONCAT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_concat)   | 返回连接字符串   |
| [CONCAT_WS()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_concat-ws)   | 返回与分隔符连接   |
| [CONNECTION_ID()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_connection-id)   | 返回连接的连接ID（线程ID）   |
| [Contains()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_contains) （已弃用5.7.6）   | 一个几何的MBR是否包含另一个几何的MBR   |
| [CONV()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_conv)   | 转换不同数字基数之间的数字   |
| [CONVERT()](https://dev.mysql.com/doc/refman/5.7/en/cast-functions.html#function_convert)   | 将值转换为特定类型   |
| [CONVERT_TZ()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_convert-tz)   | 从一个时区转换为另一个时区   |
| [ConvexHull()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_convexhull) （已弃用5.7.6）   | 返回几何体的凸包   |
| [COS()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_cos)   | 返回余弦   |
| [COT()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_cot)   | 归还余切   |
| [COUNT()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_count)   | 返回返回的行数   |
| [COUNT(DISTINCT)](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_count-distinct)   | 返回许多不同值的计数   |
| [CRC32()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_crc32)   | 计算循环冗余校验值   |
| [CREATE_ASYMMETRIC_PRIV_KEY()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-asymmetric-priv-key)   | 创建私钥   |
| [CREATE_ASYMMETRIC_PUB_KEY()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-asymmetric-pub-key)   | 创建公钥   |
| [CREATE_DH_PARAMETERS()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-dh-parameters)   | 生成共享DH密钥   |
| [CREATE_DIGEST()](https://dev.mysql.com/doc/refman/5.7/en/enterprise-encryption-functions.html#function_create-digest)   | 从字符串生成摘要   |
| [Crosses()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_crosses) （已弃用5.7.6）   | 一个几何是否与另一个几何相交   |
| [CURDATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_curdate)   | 返回当前日期   |
| [CURRENT_DATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-date)[， ](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-date)[CURRENT_DATE](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-date)   | CURDATE（）的同义词   |
| [CURRENT_TIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-time)[， ](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-time)[CURRENT_TIME](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-time)   | CURTIME（）的同义词   |
| [CURRENT_TIMESTAMP()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-timestamp)[， ](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-timestamp)[CURRENT_TIMESTAMP](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_current-timestamp)   | 同义词NOW（）   |
| [CURRENT_USER()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_current-user)[， ](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_current-user)[CURRENT_USER](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_current-user)   | 经过身份验证的用户名和主机名   |
| [CURTIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_curtime)   | 返回当前时间   |
| [DATABASE()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_database)   | 返回默认（当前）数据库名称   |
| [DATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date)   | 提取日期或日期时间表达式的日期部分   |
| [DATE_ADD()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-add)   | 将时间值（间隔）添加到日期值   |
| [DATE_FORMAT()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-format)   | 格式化日期指定   |
| [DATE_SUB()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_date-sub)   | 从日期中减去时间值（间隔）   |
| [DATEDIFF()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_datediff)   | 减去两个日期   |
| [DAY()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_day)   | DAYOFMONTH（）的同义词   |
| [DAYNAME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayname)   | 返回工作日的名称   |
| [DAYOFMONTH()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofmonth)   | 返回月中的某一天（0-31）   |
| [DAYOFWEEK()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofweek)   | 返回参数的工作日索引   |
| [DAYOFYEAR()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_dayofyear)   | 返回一年中的某一天（1-366）   |
| [DECODE()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_decode) （已弃用5.7.2）   | 解码使用ENCODE（）加密的字符串   |
| [DEFAULT()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_default)   | 返回表列的默认值   |
| [DEGREES()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_degrees)   | 将弧度转换为度数   |
| [DES_DECRYPT()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_des-decrypt) （已弃用5.7.6）   | 解密一个字符串   |
| [DES_ENCRYPT()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_des-encrypt) （已弃用5.7.6）   | 加密字符串   |
| [Dimension()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_dimension) （已弃用5.7.6）   | 几何尺寸   |
| [Disjoint()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_disjoint) （已弃用5.7.6）   | 两个几何形状的MBR是否不相交   |
| [Distance()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_distance) （已弃用5.7.6）   | 一个几何与另一个几何的距离   |
| [DIV](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_div)   | 整数除法   |
| [/](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_divide)   | 分部运营商   |
| [ELT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_elt)   | 返回索引号处的字符串   |
| [ENCODE()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_encode) （已弃用5.7.2）   | 编码一个字符串   |
| [ENCRYPT()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_encrypt) （已弃用5.7.6）   | 加密字符串   |
| [EndPoint()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_endpoint) （已弃用5.7.6）   | LineString的终点   |
| [Envelope()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_envelope) （已弃用5.7.6）   | 返回几何的MBR   |
| [=](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_equal)   | 平等的运营商   |
| [<=>](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_equal-to)   | NULL-safe等于运算符   |
| [Equals()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_equals) （已弃用5.7.6）   | 两个几何的MBR是否相等   |
| [EXP()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_exp)   | 提升到的力量   |
| [EXPORT_SET()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_export-set)   | 返回一个字符串，使得对于值位中设置的每个位，您获得一个on字符串，并且对于每个未设置的位，您将得到一个关闭字符串   |
| [ExteriorRing()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_exteriorring) （已弃用5.7.6）   | 返回Polygon的外环   |
| [EXTRACT()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_extract)   | 提取部分日期   |
| [ExtractValue()](https://dev.mysql.com/doc/refman/5.7/en/xml-functions.html#function_extractvalue)   | 使用XPath表示法从XML字符串中提取值   |
| [FIELD()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_field)   | 后续参数中第一个参数的索引（位置）   |
| [FIND_IN_SET()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_find-in-set)   | 第二个参数中第一个参数的索引（位置）   |
| [FLOOR()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_floor)   | 返回不大于参数的最大整数值   |
| [FORMAT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_format)   | 返回格式化为指定小数位数的数字   |
| [FOUND_ROWS()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_found-rows)   | 对于带有LIMIT子句的SELECT，返回的行数没有LIMIT子句   |
| [FROM_BASE64()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_from-base64)   | 解码base64编码的字符串并返回结果   |
| [FROM_DAYS()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_from-days)   | 将日期号码转换为日期   |
| [FROM_UNIXTIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_from-unixtime)   | 将Unix时间戳格式化为日期   |
| [GeomCollFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomcollfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomcollfromtext)[GeometryCollectionFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomcollfromtext)（已弃用5.7.6）   | 从WKT返回几何集合   |
| [GeomCollFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomcollfromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomcollfromwkb)[GeometryCollectionFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomcollfromwkb)（已弃用5.7.6）   | 从WKB返回几何集合   |
| [GeometryCollection()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_geometrycollection)   | 从几何构造几何集合   |
| [GeometryN()](https://dev.mysql.com/doc/refman/5.7/en/gis-geometrycollection-property-functions.html#function_geometryn) （已弃用5.7.6）   | 从几何集合中返回第N个几何   |
| [GeometryType()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_geometrytype) （已弃用5.7.6）   | 返回几何类型的名称   |
| [GeomFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomfromtext)[GeometryFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_geomfromtext)（已弃用5.7.6）   | 从WKT返回几何   |
| [GeomFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomfromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomfromwkb)[GeometryFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_geomfromwkb)（已弃用5.7.6）   | 从WKB返回几何   |
| [GET_FORMAT()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_get-format)   | 返回日期格式字符串   |
| [GET_LOCK()](https://dev.mysql.com/doc/refman/5.7/en/locking-functions.html#function_get-lock)   | 获取命名锁   |
| [GLength()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_glength) （已弃用5.7.6）   | 返回LineString的长度   |
| [>](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_greater-than)   | 大于运营商   |
| [>=](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_greater-than-or-equal)   | 大于或等于运营商   |
| [GREATEST()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_greatest)   | 返回最大的参数   |
| [GROUP_CONCAT()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_group-concat)   | 返回连接的字符串   |
| [GTID_SUBSET()](https://dev.mysql.com/doc/refman/5.7/en/gtid-functions.html#function_gtid-subset)   | 如果子集中的所有GTID也已设置，则返回true;否则返回true。否则是假的。   |
| [GTID_SUBTRACT()](https://dev.mysql.com/doc/refman/5.7/en/gtid-functions.html#function_gtid-subtract)   | 返回集合中不在子集中的所有GTID。   |
| [HEX()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_hex)   | 十进制或字符串值的十六进制表示   |
| [HOUR()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_hour)   | 提取小时   |
| [IF()](https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html#function_if)   | 如果/ else构造   |
| [IFNULL()](https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html#function_ifnull)   | Null if / else构造   |
| [IN()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_in)   | 检查值是否在一组值内   |
| [INET_ATON()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_inet-aton)   | 返回IP地址的数值   |
| [INET_NTOA()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_inet-ntoa)   | 从数值返回IP地址   |
| [INET6_ATON()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_inet6-aton)   | 返回IPv6地址的数值   |
| [INET6_NTOA()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_inet6-ntoa)   | 从数值返回IPv6地址   |
| [INSERT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_insert)   | 在指定位置插入子字符串，直到指定的字符数   |
| [INSTR()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_instr)   | 返回第一次出现的子串的索引   |
| [InteriorRingN()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_interiorringn) （已弃用5.7.6）   | 返回Polygon的第N个内环   |
| [Intersects()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_intersects) （已弃用5.7.6）   | 两个几何的MBR是否相交   |
| [INTERVAL()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_interval)   | 返回小于第一个参数的参数的索引   |
| [IS](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_is)   | 针对布尔值测试值   |
| [IS_FREE_LOCK()](https://dev.mysql.com/doc/refman/5.7/en/locking-functions.html#function_is-free-lock)   | 命名锁是否免费   |
| [IS_IPV4()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_is-ipv4)   | 参数是否为IPv4地址   |
| [IS_IPV4_COMPAT()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_is-ipv4-compat)   | 参数是否是IPv4兼容的地址   |
| [IS_IPV4_MAPPED()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_is-ipv4-mapped)   | 参数是否是IPv4映射地址   |
| [IS_IPV6()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_is-ipv6)   | 参数是否是IPv6地址   |
| [IS NOT](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_is-not)   | 针对布尔值测试值   |
| [IS NOT NULL](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_is-not-null)   | NOT NULL值测试   |
| [IS NULL](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_is-null)   | NULL值测试   |
| [IS_USED_LOCK()](https://dev.mysql.com/doc/refman/5.7/en/locking-functions.html#function_is-used-lock)   | 命名锁是否正在使用; 返回连接标识符，如果为true   |
| [IsClosed()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_isclosed) （已弃用5.7.6）   | 几何是否封闭且简单   |
| [IsEmpty()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_isempty) （已弃用5.7.6）   | 占位符功能   |
| [ISNULL()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_isnull)   | 测试参数是否为NULL   |
| [IsSimple()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_issimple) （已弃用5.7.6）   | 几何是否简单   |
| [JSON_APPEND()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-append) （已弃用5.7.9）   | 将数据附加到JSON文档   |
| [JSON_ARRAY()](https://dev.mysql.com/doc/refman/5.7/en/json-creation-functions.html#function_json-array)   | 创建JSON数组   |
| [JSON_ARRAY_APPEND()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-array-append)   | 将数据附加到JSON文档   |
| [JSON_ARRAY_INSERT()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-array-insert)   | 插入JSON数组   |
| [JSON_ARRAYAGG()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_json-arrayagg)   | 将结果集作为单个JSON数组返回   |
| [->](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#operator_json-column-path)   | 评估路径后从JSON列返回值; 相当于JSON_EXTRACT（）。   |
| [JSON_CONTAINS()](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#function_json-contains)   | JSON文档是否包含路径中的特定对象   |
| [JSON_CONTAINS_PATH()](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#function_json-contains-path)   | JSON文档是否包含路径中的任何数据   |
| [JSON_DEPTH()](https://dev.mysql.com/doc/refman/5.7/en/json-attribute-functions.html#function_json-depth)   | JSON文档的最大深度   |
| [JSON_EXTRACT()](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#function_json-extract)   | 从JSON文档返回数据   |
| [->>](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#operator_json-inline-path)   | 在评估路径并取消引用结果后，从JSON列返回值; 相当于JSON_UNQUOTE（JSON_EXTRACT（））。   |
| [JSON_INSERT()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-insert)   | 将数据插入JSON文档   |
| [JSON_KEYS()](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#function_json-keys)   | 来自JSON文档的键数组   |
| [JSON_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/json-attribute-functions.html#function_json-length)   | JSON文档中的元素数量   |
| [JSON_MERGE()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-merge) （已弃用5.7.22）   | 合并JSON文档，保留重复键。JSON_MERGE_PRESERVE（）的弃用词不再使用   |
| [JSON_MERGE_PATCH()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-merge-patch)   | 合并JSON文档，替换重复键的值   |
| [JSON_MERGE_PRESERVE()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-merge-preserve)   | 合并JSON文档，保留重复键   |
| [JSON_OBJECT()](https://dev.mysql.com/doc/refman/5.7/en/json-creation-functions.html#function_json-object)   | 创建JSON对象   |
| [JSON_OBJECTAGG()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_json-objectagg)   | 将结果集作为单个JSON对象返回   |
| [JSON_PRETTY()](https://dev.mysql.com/doc/refman/5.7/en/json-utility-functions.html#function_json-pretty)   | 以人类可读的格式打印JSON文档   |
| [JSON_QUOTE()](https://dev.mysql.com/doc/refman/5.7/en/json-creation-functions.html#function_json-quote)   | 引用JSON文档   |
| [JSON_REMOVE()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-remove)   | 从JSON文档中删除数据   |
| [JSON_REPLACE()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-replace)   | 替换JSON文档中的值   |
| [JSON_SEARCH()](https://dev.mysql.com/doc/refman/5.7/en/json-search-functions.html#function_json-search)   | JSON文档中的值路径   |
| [JSON_SET()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-set)   | 将数据插入JSON文档   |
| [JSON_STORAGE_SIZE()](https://dev.mysql.com/doc/refman/5.7/en/json-utility-functions.html#function_json-storage-size)   | 用于存储JSON文档的二进制表示的空间   |
| [JSON_TYPE()](https://dev.mysql.com/doc/refman/5.7/en/json-attribute-functions.html#function_json-type)   | JSON值的类型   |
| [JSON_UNQUOTE()](https://dev.mysql.com/doc/refman/5.7/en/json-modification-functions.html#function_json-unquote)   | 取消引用JSON值   |
| [JSON_VALID()](https://dev.mysql.com/doc/refman/5.7/en/json-attribute-functions.html#function_json-valid)   | JSON值是否有效   |
| [LAST_DAY](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_last-day)   | 返回参数的月份的最后一天   |
| [LAST_INSERT_ID()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_last-insert-id)   | 最后一次INSERT的AUTOINCREMENT列的值   |
| [LCASE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lcase)   | LOWER（）的同义词   |
| [LEAST()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_least)   | 返回最小的参数   |
| [LEFT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_left)   | 返回指定的最左边的字符数   |
| [<<](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_left-shift)   | 左移   |
| [LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_length)   | 以字节为单位返回字符串的长度   |
| [<](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_less-than)   | 不到运营商   |
| [<=](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_less-than-or-equal)   | 小于或等于运营商   |
| [LIKE](https://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#operator_like)   | 简单的模式匹配   |
| [LineFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_linefromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_linefromtext)[LineStringFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_linefromtext)（已弃用5.7.6）   | 从WKT构造LineString   |
| [LineFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_linefromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_linefromwkb)[LineStringFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_linefromwkb)（已弃用5.7.6）   | 从WKB构造LineString   |
| [LineString()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_linestring)   | 从Point值构造LineString   |
| [LN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_ln)   | 返回参数的自然对数   |
| [LOAD_FILE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_load-file)   | 加载指定的文件   |
| [LOCALTIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtime)[， ](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtime)[LOCALTIME](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtime)   | NOW（）的同义词   |
| [LOCALTIMESTAMP](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtimestamp)[， ](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtimestamp)[LOCALTIMESTAMP()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_localtimestamp)   | NOW（）的同义词   |
| [LOCATE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_locate)   | 返回第一次出现的子串的位置   |
| [LOG()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_log)   | 返回第一个参数的自然对数   |
| [LOG10()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_log10)   | 返回参数的以10为底的对数   |
| [LOG2()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_log2)   | 返回参数的base-2对数   |
| [LOWER()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lower)   | 以小写形式返回参数   |
| [LPAD()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_lpad)   | 返回字符串参数，使用指定的字符串进行左填充   |
| [LTRIM()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ltrim)   | 删除前导空格   |
| [MAKE_SET()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_make-set)   | 返回一组以逗号分隔的字符串，这些字符串具有相应的位设置位   |
| [MAKEDATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_makedate)   | 创建年份和年中的日期   |
| [MAKETIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_maketime)   | 从小时，分钟，秒创建时间   |
| [MASTER_POS_WAIT()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_master-pos-wait)   | 阻止，直到从站已读取并应用所有更新到指定位置   |
| [MATCH](https://dev.mysql.com/doc/refman/5.7/en/fulltext-search.html#function_match)   | 执行全文搜索   |
| [MAX()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_max)   | 返回最大值   |
| [MBRContains()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrcontains)   | 一个几何的MBR是否包含另一个几何的MBR   |
| [MBRCoveredBy()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrcoveredby)   | 一个MBR是否被另一个MBR覆盖   |
| [MBRCovers()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrcovers)   | 一个MBR是否涵盖另一个MBR   |
| [MBRDisjoint()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrdisjoint)   | 两个几何形状的MBR是否不相交   |
| [MBREqual()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrequal) （已弃用5.7.6）   | 两个几何的MBR是否相等   |
| [MBREquals()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrequals)   | 两个几何的MBR是否相等   |
| [MBRIntersects()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrintersects)   | 两个几何的MBR是否相交   |
| [MBROverlaps()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbroverlaps)   | 两个几何的MBR是否重叠   |
| [MBRTouches()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrtouches)   | 两种几何形状的MBR是否接触   |
| [MBRWithin()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_mbrwithin)   | 一个几何的MBR是否在另一个几何的MBR内   |
| [MD5()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_md5)   | 计算MD5校验和   |
| [MICROSECOND()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_microsecond)   | 从参数返回微秒   |
| [MID()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_mid)   | 返回从指定位置开始的子字符串   |
| [MIN()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_min)   | 返回最小值   |
| [-](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_minus)   | 减号运算符   |
| [MINUTE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_minute)   | 从论证中返回分钟   |
| [MLineFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mlinefromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mlinefromtext)[MultiLineStringFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mlinefromtext)（已弃用5.7.6）   | 从WKT构造MultiLineString   |
| [MLineFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mlinefromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mlinefromwkb)[MultiLineStringFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mlinefromwkb)（已弃用5.7.6）   | 从WKB构造MultiLineString   |
| [MOD()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_mod)   | 归还剩下的   |
| [%](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_mod)[， ](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_mod)[MOD](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_mod)   | 模数运算符   |
| [MONTH()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_month)   | 从过去的日期返回月份   |
| [MONTHNAME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_monthname)   | 返回月份名称   |
| [MPointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpointfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpointfromtext)[MultiPointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpointfromtext)（已弃用5.7.6）   | 从WKT构造MultiPoint   |
| [MPointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpointfromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpointfromwkb)[MultiPointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpointfromwkb)（已弃用5.7.6）   | 从WKB构造MultiPoint   |
| [MPolyFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpolyfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpolyfromtext)[MultiPolygonFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_mpolyfromtext)（已弃用5.7.6）   | 从WKT构造MultiPolygon   |
| [MPolyFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpolyfromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpolyfromwkb)[MultiPolygonFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_mpolyfromwkb)（已弃用5.7.6）   | 从WKB构造MultiPolygon   |
| [MultiLineString()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_multilinestring)   | 从LineString值构造MultiLineString   |
| [MultiPoint()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_multipoint)   | 从Point值构造MultiPoint   |
| [MultiPolygon()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_multipolygon)   | 从Polygon值构造MultiPolygon   |
| [NAME_CONST()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_name-const)   | 导致列具有给定名称   |
| [NOT](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_not)[， ](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_not)[!](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_not)   | 否定价值   |
| [NOT BETWEEN ... AND ...](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_not-between)   | 检查值是否不在值范围内   |
| [!=](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_not-equal)[， ](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_not-equal)[<>](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_not-equal)   | 不等于运营商   |
| [NOT IN()](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#function_not-in)   | 检查值是否不在一组值内   |
| [NOT LIKE](https://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#operator_not-like)   | 简单模式匹配的否定   |
| [NOT REGEXP](https://dev.mysql.com/doc/refman/5.7/en/regexp.html#operator_not-regexp)   | REGEXP的否定   |
| [NOW()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_now)   | 返回当前日期和时间   |
| [NULLIF()](https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html#function_nullif)   | 如果expr1 = expr2，则返回NULL   |
| [NumGeometries()](https://dev.mysql.com/doc/refman/5.7/en/gis-geometrycollection-property-functions.html#function_numgeometries) （已弃用5.7.6）   | 返回几何集合中的几何数量   |
| [NumInteriorRings()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_numinteriorrings) （已弃用5.7.6）   | 返回多边形内圈的数量   |
| [NumPoints()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_numpoints) （已弃用5.7.6）   | 返回LineString中的点数   |
| [OCT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_oct)   | 返回包含数字的八进制表示的字符串   |
| [OCTET_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_octet-length)   | LENGTH（）的同义词   |
| [OLD_PASSWORD()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_old-password)   | 返回PASSWORD 4.1之前实现的值   |
| [\|\|](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_or)[， ](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_or)[OR](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_or)   | 逻辑或   |
| [ORD()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ord)   | 返回参数最左侧字符的字符代码   |
| [Overlaps()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_overlaps) （已弃用5.7.6）   | 两个几何的MBR是否重叠   |
| [PASSWORD()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_password) （已弃用5.7.6）   | 计算并返回密码字符串   |
| [PERIOD_ADD()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_period-add)   | 将期间添加到年 - 月   |
| [PERIOD_DIFF()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_period-diff)   | 返回句点之间的月数   |
| [PI()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_pi)   | 返回pi的值   |
| [+](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_plus)   | 加法运算符   |
| [Point()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_point)   | 从坐标构造点   |
| [PointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_pointfromtext) （已弃用5.7.6）   | 从WKT构建点   |
| [PointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_pointfromwkb) （已弃用5.7.6）   | 从WKB构造点   |
| [PointN()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_pointn) （已弃用5.7.6）   | 从LineString返回第N个点   |
| [PolyFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_polyfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_polyfromtext)[PolygonFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_polyfromtext)（已弃用5.7.6）   | 从WKT构造多边形   |
| [PolyFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_polyfromwkb)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_polyfromwkb)[PolygonFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_polyfromwkb)（已弃用5.7.6）   | 从WKB构造多边形   |
| [Polygon()](https://dev.mysql.com/doc/refman/5.7/en/gis-mysql-specific-functions.html#function_polygon)   | 从LineString参数构造多边形   |
| [POSITION()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_position)   | LOCATE（）的同义词   |
| [POW()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_pow)   | 将引发的参数返回到指定的幂   |
| [POWER()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_power)   | 将引发的参数返回到指定的幂   |
| [PROCEDURE ANALYSE()](https://dev.mysql.com/doc/refman/5.7/en/procedure-analyse.html) （已弃用5.7.18）   | 分析查询的结果   |
| [QUARTER()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_quarter)   | 从日期参数返回季度   |
| [QUOTE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_quote)   | 转义参数以在SQL语句中使用   |
| [RADIANS()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_radians)   | 返回参数转换为弧度   |
| [RAND()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_rand)   | 返回随机浮点值   |
| [RANDOM_BYTES()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_random-bytes)   | 返回一个随机字节向量   |
| [REGEXP](https://dev.mysql.com/doc/refman/5.7/en/regexp.html#operator_regexp)   | string是否匹配正则表达式   |
| [RELEASE_ALL_LOCKS()](https://dev.mysql.com/doc/refman/5.7/en/locking-functions.html#function_release-all-locks)   | 释放所有当前命名的锁   |
| [RELEASE_LOCK()](https://dev.mysql.com/doc/refman/5.7/en/locking-functions.html#function_release-lock)   | 释放命名锁   |
| [REPEAT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_repeat)   | 重复指定次数的字符串   |
| [REPLACE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_replace)   | 替换指定字符串的出现次数   |
| [REVERSE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_reverse)   | 反转字符串中的字符   |
| [RIGHT()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_right)   | 返回指定的最右边的字符数   |
| [>>](https://dev.mysql.com/doc/refman/5.7/en/bit-functions.html#operator_right-shift)   | 右转   |
| [RLIKE](https://dev.mysql.com/doc/refman/5.7/en/regexp.html#operator_regexp)   | string是否匹配正则表达式   |
| [ROUND()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_round)   | 围绕论点   |
| [ROW_COUNT()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_row-count)   | 行数已更新   |
| [RPAD()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_rpad)   | 追加指定次数的字符串   |
| [RTRIM()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_rtrim)   | 删除尾随空格   |
| [SCHEMA()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_schema)   | DATABASE（）的同义词   |
| [SEC_TO_TIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_sec-to-time)   | 将秒转换为'HH：MM：SS'格式   |
| [SECOND()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_second)   | 返回秒（0-59）   |
| [SESSION_USER()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_session-user)   | USER（）的同义词   |
| [SHA1()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_sha1)[， ](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_sha1)[SHA()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_sha1)   | 计算SHA-1 160位校验和   |
| [SHA2()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_sha2)   | 计算SHA-2校验和   |
| [SIGN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_sign)   | 返回参数的符号   |
| [SIN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_sin)   | 返回参数的正弦值   |
| [SLEEP()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_sleep)   | 睡几秒钟   |
| [SOUNDEX()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_soundex)   | 返回soundex字符串   |
| [SOUNDS LIKE](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#operator_sounds-like)   | 比较声音   |
| [SPACE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_space)   | 返回指定数量的空格的字符串   |
| [SQRT()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_sqrt)   | 返回参数的平方根   |
| [SRID()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_srid) （已弃用5.7.6）   | 返回几何的空间参考系统ID   |
| [ST_Area()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-area)   | 返回Polygon或MultiPolygon区域   |
| [ST_AsBinary()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-asbinary)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-asbinary)[ST_AsWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-asbinary)   | 从内部几何格式转换为WKB   |
| [ST_AsGeoJSON()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geojson-functions.html#function_st-asgeojson)   | 从几何体生成GeoJSON对象   |
| [ST_AsText()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-astext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-astext)[ST_AsWKT()](https://dev.mysql.com/doc/refman/5.7/en/gis-format-conversion-functions.html#function_st-astext)   | 从内部几何格式转换为WKT   |
| [ST_Buffer()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-buffer)   | 返回距离几何体的给定距离内的点的几何   |
| [ST_Buffer_Strategy()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-buffer-strategy)   | 为ST_Buffer（）生成策略选项   |
| [ST_Centroid()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-centroid)   | 返回质心作为一个点   |
| [ST_Contains()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-contains)   | 一个几何是否包含另一个   |
| [ST_ConvexHull()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-convexhull)   | 返回几何体的凸包   |
| [ST_Crosses()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-crosses)   | 一个几何是否与另一个几何相交   |
| [ST_Difference()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-difference)   | 两个几何的返回点集差异   |
| [ST_Dimension()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-dimension)   | 几何尺寸   |
| [ST_Disjoint()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-disjoint)   | 一个几何是否与另一个几何脱节   |
| [ST_Distance()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-distance)   | 一个几何与另一个几何的距离   |
| [ST_Distance_Sphere()](https://dev.mysql.com/doc/refman/5.7/en/spatial-convenience-functions.html#function_st-distance-sphere)   | 两个几何形状之间的最小地球距离   |
| [ST_EndPoint()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-endpoint)   | LineString的终点   |
| [ST_Envelope()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-envelope)   | 返回几何的MBR   |
| [ST_Equals()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-equals)   | 一个几何是否与另一个几何相等   |
| [ST_ExteriorRing()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-exteriorring)   | 返回Polygon的外环   |
| [ST_GeoHash()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geohash-functions.html#function_st-geohash)   | 产生geohash值   |
| [ST_GeomCollFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomcollfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomcollfromtext)[ST_GeometryCollectionFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomcollfromtext)[，](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomcollfromtext)[ST_GeomCollFromTxt()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomcollfromtext)   | 从WKT返回几何集合   |
| [ST_GeomCollFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomcollfromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomcollfromwkb)[ST_GeometryCollectionFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomcollfromwkb)   | 从WKB返回几何集合   |
| [ST_GeometryN()](https://dev.mysql.com/doc/refman/5.7/en/gis-geometrycollection-property-functions.html#function_st-geometryn)   | 从几何集合中返回第N个几何   |
| [ST_GeometryType()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-geometrytype)   | 返回几何类型的名称   |
| [ST_GeomFromGeoJSON()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geojson-functions.html#function_st-geomfromgeojson)   | 从GeoJSON对象生成几何   |
| [ST_GeomFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomfromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomfromtext)[ST_GeometryFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-geomfromtext)   | 从WKT返回几何   |
| [ST_GeomFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomfromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomfromwkb)[ST_GeometryFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-geomfromwkb)   | 从WKB返回几何   |
| [ST_InteriorRingN()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-interiorringn)   | 返回Polygon的第N个内环   |
| [ST_Intersection()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-intersection)   | 返回点设置两个几何的交集   |
| [ST_Intersects()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-intersects)   | 一个几何是否与另一个相交   |
| [ST_IsClosed()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-isclosed)   | 几何是否封闭且简单   |
| [ST_IsEmpty()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-isempty)   | 占位符功能   |
| [ST_IsSimple()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-issimple)   | 几何是否简单   |
| [ST_IsValid()](https://dev.mysql.com/doc/refman/5.7/en/spatial-convenience-functions.html#function_st-isvalid)   | 几何是否有效   |
| [ST_LatFromGeoHash()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geohash-functions.html#function_st-latfromgeohash)   | 从geohash值返回纬度   |
| [ST_Length()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-length)   | 返回LineString的长度   |
| [ST_LineFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-linefromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-linefromtext)[ST_LineStringFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-linefromtext)   | 从WKT构造LineString   |
| [ST_LineFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-linefromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-linefromwkb)[ST_LineStringFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-linefromwkb)   | 从WKB构造LineString   |
| [ST_LongFromGeoHash()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geohash-functions.html#function_st-longfromgeohash)   | 从geohash值返回经度   |
| [ST_MakeEnvelope()](https://dev.mysql.com/doc/refman/5.7/en/spatial-convenience-functions.html#function_st-makeenvelope)   | 两点左右的矩形   |
| [ST_MLineFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mlinefromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mlinefromtext)[ST_MultiLineStringFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mlinefromtext)   | 从WKT构造MultiLineString   |
| [ST_MLineFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mlinefromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mlinefromwkb)[ST_MultiLineStringFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mlinefromwkb)   | 从WKB构造MultiLineString   |
| [ST_MPointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpointfromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpointfromtext)[ST_MultiPointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpointfromtext)   | 从WKT构造MultiPoint   |
| [ST_MPointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpointfromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpointfromwkb)[ST_MultiPointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpointfromwkb)   | 从WKB构造MultiPoint   |
| [ST_MPolyFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpolyfromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpolyfromtext)[ST_MultiPolygonFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-mpolyfromtext)   | 从WKT构造MultiPolygon   |
| [ST_MPolyFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpolyfromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpolyfromwkb)[ST_MultiPolygonFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-mpolyfromwkb)   | 从WKB构造MultiPolygon   |
| [ST_NumGeometries()](https://dev.mysql.com/doc/refman/5.7/en/gis-geometrycollection-property-functions.html#function_st-numgeometries)   | 返回几何集合中的几何数量   |
| [ST_NumInteriorRing()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-numinteriorrings)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-numinteriorrings)[ST_NumInteriorRings()](https://dev.mysql.com/doc/refman/5.7/en/gis-polygon-property-functions.html#function_st-numinteriorrings)   | 返回多边形内圈的数量   |
| [ST_NumPoints()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-numpoints)   | 返回LineString中的点数   |
| [ST_Overlaps()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-overlaps)   | 一个几何是否与另一个重叠   |
| [ST_PointFromGeoHash()](https://dev.mysql.com/doc/refman/5.7/en/spatial-geohash-functions.html#function_st-pointfromgeohash)   | 将geohash值转换为POINT值   |
| [ST_PointFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-pointfromtext)   | 从WKT构建点   |
| [ST_PointFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-pointfromwkb)   | 从WKB构造点   |
| [ST_PointN()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-pointn)   | 从LineString返回第N个点   |
| [ST_PolyFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-polyfromtext)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-polyfromtext)[ST_PolygonFromText()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkt-functions.html#function_st-polyfromtext)   | 从WKT构造多边形   |
| [ST_PolyFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-polyfromwkb)[， ](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-polyfromwkb)[ST_PolygonFromWKB()](https://dev.mysql.com/doc/refman/5.7/en/gis-wkb-functions.html#function_st-polyfromwkb)   | 从WKB构造多边形   |
| [ST_Simplify()](https://dev.mysql.com/doc/refman/5.7/en/spatial-convenience-functions.html#function_st-simplify)   | 返回简化几何   |
| [ST_SRID()](https://dev.mysql.com/doc/refman/5.7/en/gis-general-property-functions.html#function_st-srid)   | 返回几何的空间参考系统ID   |
| [ST_StartPoint()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_st-startpoint)   | LineString的起始点   |
| [ST_SymDifference()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-symdifference)   | 返回点设置两个几何的对称差异   |
| [ST_Touches()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-touches)   | 一个几何是否接触另一个   |
| [ST_Union()](https://dev.mysql.com/doc/refman/5.7/en/spatial-operator-functions.html#function_st-union)   | 返回点集两个几何的并集   |
| [ST_Validate()](https://dev.mysql.com/doc/refman/5.7/en/spatial-convenience-functions.html#function_st-validate)   | 返回验证的几何体   |
| [ST_Within()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_st-within)   | 一个几何是否在另一个之内   |
| [ST_X()](https://dev.mysql.com/doc/refman/5.7/en/gis-point-property-functions.html#function_st-x)   | 返回Point的X坐标   |
| [ST_Y()](https://dev.mysql.com/doc/refman/5.7/en/gis-point-property-functions.html#function_st-y)   | 返回Point的Y坐标   |
| [StartPoint()](https://dev.mysql.com/doc/refman/5.7/en/gis-linestring-property-functions.html#function_startpoint) （已弃用5.7.6）   | LineString的起始点   |
| [STD()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_std)   | 返回人口标准差   |
| [STDDEV()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_stddev)   | 返回人口标准差   |
| [STDDEV_POP()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_stddev-pop)   | 返回人口标准差   |
| [STDDEV_SAMP()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_stddev-samp)   | 返回样本标准差   |
| [STR_TO_DATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_str-to-date)   | 将字符串转换为日期   |
| [STRCMP()](https://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#function_strcmp)   | 比较两个字符串   |
| [SUBDATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_subdate)   | 使用三个参数调用时DATE_SUB（）的同义词   |
| [SUBSTR()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substr)   | 返回指定的子字符串   |
| [SUBSTRING()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substring)   | 返回指定的子字符串   |
| [SUBSTRING_INDEX()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substring-index)   | 在指定的分隔符出现次数之前从字符串返回子字符串   |
| [SUBTIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_subtime)   | 减去时间   |
| [SUM()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_sum)   | 归还总和   |
| [SYSDATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_sysdate)   | 返回函数执行的时间   |
| [SYSTEM_USER()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_system-user)   | USER（）的同义词   |
| [TAN()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_tan)   | 返回参数的正切值   |
| [TIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_time)   | 提取传递的表达式的时间部分   |
| [TIME_FORMAT()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_time-format)   | 格式化为时间   |
| [TIME_TO_SEC()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_time-to-sec)   | 返回转换为秒的参数   |
| [TIMEDIFF()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_timediff)   | 减去时间   |
| [*](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_times)   | 乘法运算符   |
| [TIMESTAMP()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_timestamp)   | 使用单个参数，此函数返回日期或日期时间表达式; 有两个参数，参数的总和   |
| [TIMESTAMPADD()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_timestampadd)   | 在datetime表达式中添加间隔   |
| [TIMESTAMPDIFF()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_timestampdiff)   | 从日期时间表达式中减去间隔   |
| [TO_BASE64()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_to-base64)   | 返回转换为base-64字符串的参数   |
| [TO_DAYS()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_to-days)   | 返回转换为days的日期参数   |
| [TO_SECONDS()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_to-seconds)   | 返回自0年以来转换为秒的日期或日期时间参数   |
| [Touches()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-object-shapes.html#function_touches) （已弃用5.7.6）   | 一个几何是否接触另一个   |
| [TRIM()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_trim)   | 删除前导和尾随空格   |
| [TRUNCATE()](https://dev.mysql.com/doc/refman/5.7/en/mathematical-functions.html#function_truncate)   | 截断到指定的小数位数   |
| [UCASE()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_ucase)   | UPPER（）的同义词   |
| [-](https://dev.mysql.com/doc/refman/5.7/en/arithmetic-functions.html#operator_unary-minus)   | 更改参数的符号   |
| [UNCOMPRESS()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_uncompress)   | 解压缩压缩的字符串   |
| [UNCOMPRESSED_LENGTH()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_uncompressed-length)   | 压缩前返回字符串的长度   |
| [UNHEX()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_unhex)   | 返回包含数字的十六进制表示的字符串   |
| [UNIX_TIMESTAMP()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_unix-timestamp)   | 返回Unix时间戳   |
| [UpdateXML()](https://dev.mysql.com/doc/refman/5.7/en/xml-functions.html#function_updatexml)   | 返回替换的XML片段   |
| [UPPER()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_upper)   | 转换为大写   |
| [USER()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_user)   | 客户端提供的用户名和主机名   |
| [UTC_DATE()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_utc-date)   | 返回当前的UTC日期   |
| [UTC_TIME()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_utc-time)   | 返回当前的UTC时间   |
| [UTC_TIMESTAMP()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_utc-timestamp)   | 返回当前的UTC日期和时间   |
| [UUID()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_uuid)   | 返回通用唯一标识符（UUID）   |
| [UUID_SHORT()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_uuid-short)   | 返回整数值通用标识符   |
| [VALIDATE_PASSWORD_STRENGTH()](https://dev.mysql.com/doc/refman/5.7/en/encryption-functions.html#function_validate-password-strength)   | 确定密码的强度   |
| [VALUES()](https://dev.mysql.com/doc/refman/5.7/en/miscellaneous-functions.html#function_values)   | 定义INSERT期间要使用的值   |
| [VAR_POP()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_var-pop)   | 返回人口标准差异   |
| [VAR_SAMP()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_var-samp)   | 返回样本方差   |
| [VARIANCE()](https://dev.mysql.com/doc/refman/5.7/en/group-by-functions.html#function_variance)   | 返回人口标准差异   |
| [VERSION()](https://dev.mysql.com/doc/refman/5.7/en/information-functions.html#function_version)   | 返回表示MySQL服务器版本的字符串   |
| [WAIT_FOR_EXECUTED_GTID_SET()](https://dev.mysql.com/doc/refman/5.7/en/gtid-functions.html#function_wait-for-executed-gtid-set)   | 等到给定的GTID在slave上执行。   |
| [WAIT_UNTIL_SQL_THREAD_AFTER_GTIDS()](https://dev.mysql.com/doc/refman/5.7/en/gtid-functions.html#function_wait-until-sql-thread-after-gtids)   | 等到给定的GTID在slave上执行。   |
| [WEEK()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_week)   | 返回周数   |
| [WEEKDAY()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_weekday)   | 返回工作日索引   |
| [WEEKOFYEAR()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_weekofyear)   | 返回日期的日历周（1-53）   |
| [WEIGHT_STRING()](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_weight-string)   | 返回字符串的权重字符串   |
| [Within()](https://dev.mysql.com/doc/refman/5.7/en/spatial-relation-functions-mbr.html#function_within) （已弃用5.7.6）   | 一个几何的MBR是否在另一个几何的MBR内   |
| [X()](https://dev.mysql.com/doc/refman/5.7/en/gis-point-property-functions.html#function_x) （已弃用5.7.6）   | 返回Point的X坐标   |
| [XOR](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_xor)   | 逻辑异或   |
| [Y()](https://dev.mysql.com/doc/refman/5.7/en/gis-point-property-functions.html#function_y) （已弃用5.7.6）   | 返回Point的Y坐标   |
| [YEAR()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_year)   | 回归年份   |
| [YEARWEEK()](https://dev.mysql.com/doc/refman/5.7/en/date-and-time-functions.html#function_yearweek)   | 返回年份和星期   |




```
drop database if exists oldboy;
create database oldboy charset utf8mb4 collate utf8mb4_bin;
use oldboy;
create table t_100w (id int,num int,k1 char(2),k2 char(4),dt timestamp);
```

```
delimiter //
create  procedure rand_data(in num int)
begin
declare str char(62) default 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
declare str2 char(2);
declare str4 char(4);
declare i int default 0;
while i<num do
set str2=concat(substring(str,1+floor(rand()*61),1),substring(str,1+floor(rand()*61),1));
set str4=concat(substring(str,1+floor(rand()*61),2),substring(str,1+floor(rand()*61),2));
set i=i+1;
insert into t_100w values (i,floor(rand()*num),str2,str4,now());
end while;
end;
//
delimiter ;
```

```
call rand_data(1000000);
commit;
```







# 运算符
[https://dev.mysql.com/doc/refman/5.7/en/non-typed-operators.html](https://dev.mysql.com/doc/refman/5.7/en/non-typed-operators.html)



# 控制流
[https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html](https://dev.mysql.com/doc/refman/5.7/en/control-flow-functions.html)
[https://dev.mysql.com/doc/refman/5.7/en/flow-control-statements.html](https://dev.mysql.com/doc/refman/5.7/en/flow-control-statements.html)


## IF(expr1,expr2,expr3)
**如果expr1是TRUE （expr1 <> 0和expr1 <> NULL），则IF() 返回expr2。否则，它返回expr3**

```
mysql> SELECT IF(1>2,2,3);
        -> 3
mysql> SELECT IF(1<2,'yes','no');
        -> 'yes'
```



## case
```
CASE value WHEN [compare_value] THEN result [WHEN [compare_value] THEN result ...] [ELSE result] END
```
第一个CASE语法返回 result第一个 为true的比较

```
CASE WHEN [condition] THEN result [WHEN [condition] THEN result ...] [ELSE result] END
```
第二种语法返回第一个条件为true的结果。如果没有比较或条件为真，则返回结果，或者如果没有 部分。 value=compare_value ELSENULLELSE


```
mysql> SELECT CASE 1 WHEN 1 THEN 'one' WHEN 2 THEN 'two' ELSE 'more' END;
    -> 'one'

mysql> SELECT CASE WHEN 1>0 THEN 'true' ELSE 'false' END;
        -> 'true'
```




### 统计各位老师,所教课程的及格率
```
SELECT teacher.`tname`,course.`cname`,
COUNT(CASE WHEN sc.`score`>60 THEN 1 END)/COUNT(sc.`score`)
FROM teacher
JOIN course ON teacher.`tno`=course.`tno`
JOIN sc ON course.`cno`=sc.`cno`
GROUP BY teacher.`tname`
```



### 统计每门课程:优秀(85分以上),良好(70-85),一般(60-70),不及格(小于60)的学生列表

```
SELECT course.`cname`, 
CASE WHEN sc.`score`>85 THEN student.`sname` END  AS 优秀,
CASE WHEN sc.`score`>70 AND sc.`score`<=85 THEN student.`sname` END AS 良好 ,
CASE WHEN sc.`score`>=60 AND sc.`score`<=70 THEN student.`sname` END  AS 一般, 
CASE WHEN sc.`score`<60 THEN student.`sname` END  AS 不及格
FROM course
JOIN sc ON course.`cno`=sc.`cno`
JOIN student ON sc.`sno`=student.`sno`
```


```
SELECT course.`cname`, 
GROUP_CONCAT(CASE WHEN sc.`score`>85 THEN student.`sname` END  ) AS 优秀,
GROUP_CONCAT(CASE WHEN sc.`score`>70 AND sc.`score`<=85 THEN student.`sname` END) AS 良好,
GROUP_CONCAT(CASE WHEN sc.`score`>=60 AND sc.`score`<=70 THEN student.`sname` END) AS 一般, 
GROUP_CONCAT(CASE WHEN sc.`score`<60 THEN student.`sname` END) AS 不及格
FROM course
JOIN sc ON course.`cno`=sc.`cno`
JOIN student ON sc.`sno`=student.`sno`
GROUP BY course.`cname`
```



# sql编程
## case
```
CASE case_value
    WHEN when_value THEN statement_list
    [WHEN when_value THEN statement_list] ...
    [ELSE statement_list]
END CASE
```

或
```
CASE
    WHEN search_condition THEN statement_list
    [WHEN search_condition THEN statement_list] ...
    [ELSE statement_list]
END CASE
```


存储程序
```
DELIMITER |

CREATE PROCEDURE p()
  BEGIN
    DECLARE v INT DEFAULT 1;

    CASE v
      WHEN 2 THEN SELECT v;
      WHEN 3 THEN SELECT 0;
      ELSE
        BEGIN
        END;
    END CASE;
  END;
  |
```


## if
```
IF search_condition THEN statement_list
    [ELSEIF search_condition THEN statement_list] ...
    [ELSE statement_list]
END IF
```



```
DELIMITER //

CREATE FUNCTION SimpleCompare(n INT, m INT)
  RETURNS VARCHAR(20)

  BEGIN
    DECLARE s VARCHAR(20);

    IF n > m THEN SET s = '>';
    ELSEIF n = m THEN SET s = '=';
    ELSE SET s = '<';
    END IF;

    SET s = CONCAT(n, ' ', s, ' ', m);

    RETURN s;
  END //
DELIMITER ;
```



## loop
```
[begin_label:] LOOP
    statement_list
END LOOP [end_label]
```


```
CREATE PROCEDURE doiterate(p1 INT)
BEGIN
  label1: LOOP
    SET p1 = p1 + 1;
    IF p1 < 10 THEN
      ITERATE label1;
    END IF;
    LEAVE label1;
  END LOOP label1;
  SET @x = p1;
END;
```



## while
```
[begin_label:] WHILE search_condition DO
    statement_list
END WHILE [end_label]
```


```
CREATE PROCEDURE dowhile()
BEGIN
  DECLARE v1 INT DEFAULT 5;

  WHILE v1 > 0 DO
    ...
    SET v1 = v1 - 1;
  END WHILE;
END;
```






14. ** MySQL 元数据**
96. ** 元数据获取**

1、数据库、表对象的一些定义信息都可以称之为元数据
2、数据库的一些状态统计

元数据是存放到数据库的系统表（基表）


97. ** Information_schema使用**

DESC information_schema.TABLES

```
TABLE_SCHEMA    ---->库名
TABLE_NAME      ---->表名
ENGINE          ---->引擎
TABLE_ROWS      ---->表的行数
AVG_ROW_LENGTH  ---->表中行的平均行（字节）
INDEX_LENGTH    ---->索引的占用空间大小（字节）
```


```
show tables from information_schema;
```

## **tables 表**
### 查看数据库中所有表
```
select table_name from tables;
```


### 查看每个库的所有表
```
SELECT TABLE_SCHEMA,GROUP_CONCAT(TABLE_NAME)
FROM TABLES
GROUP BY TABLE_SCHEMA;
```


### 查看world、oldboy库中有哪些表
```
mysql> select table_name,table_schema from tables where table_schema='world' or table_schema='oldboy';
+-----------------+--------------+
| table_name      | table_schema |
+-----------------+--------------+
| student         | oldboy       |
| student_0       | oldboy       |
| city            | world        |
| country         | world        |
| countrylanguage | world        |
+-----------------+--------------+
5 rows in set (0.00 sec)
```



### 查看数据库中innodb引擎表
```
mysql> select table_name,table_schema from tables where engine='innodb';
+----------------------+--------------+
| table_name           | table_schema |
+----------------------+--------------+
| innodb_index_stats   | mysql        |
| innodb_table_stats   | mysql        |
| slave_master_info    | mysql        |
| slave_relay_log_info | mysql        |
| slave_worker_info    | mysql        |
| student              | oldboy       |
| student_0            | oldboy       |
| city                 | world        |
| country              | world        |
| countrylanguage      | world        |
+----------------------+--------------+
```


### 查看数据库中共有多少表
```
mysql> select count(table_name) from tables;
+-------------------+
| count(table_name) |
+-------------------+
|               144 |
+-------------------+
1 row in set (0.00 sec)
```



### **concat拼接**
```
select concat("mysqldump ", "-uroot", " -poldboy123", "table_schema", " ", "table_name"," >/tmp/",table_schema,"_",table_name,".sql") from information_schema.tables;


select concat("mysqldump ", "-uroot", " -poldboy123", "table_schema", " ", "table_name"," >/tmp/",table_schema,"_",table_name,".sql") from information_schema.tables into outfile "/tmp/bak.sh";
```


### 分库分表备份
vim /etc/my.cnf
```
secure-file-priv=/tmp       
```


```
select concat("mysqldump ", "-uroot", " -p123 ",TABLE_SCHEMA," ",TABLE_NAME," >/bak/",TABLE_SCHEMA,"_",TABLE_NAME,".sql")from information_schema.tables into outfile '/tmp/tabbak.sh';
```


mkdir /bak


备份所有表结构
```
create table world.city_0 like world.city;
mysql -e 'select concat("create table ",table_schema,".",table_name,"_0"," like ",table_schema,".",table_name)from information_schema.tables;'|grep -v concat
```



### 查看每张表占用磁盘空间大小
```
SELECT TABLE_SCHEMA,TABLE_NAME, TABLE_ROWS*AVG_ROW_LENGTH+INDEX_LENGTH
FROM TABLES
WHERE TABLE_SCHEMA='world';
```



### 每个库占用磁盘空间大小
```
SELECT TABLE_SCHEMA,SUM(TABLE_ROWS*AVG_ROW_LENGTH+INDEX_LENGTH)
FROM TABLES
GROUP BY TABLE_SCHEMA
```

### 数据库占用磁盘空间总大小
```
SELECT SUM(TABLE_ROWS*AVG_ROW_LENGTH+INDEX_LENGTH)
FROM TABLES
```





### **统计数据量**
```
SELECT  
CONCAT(table_schema, '.', table_name) AS "Name"  
,CONCAT(ROUND(table_rows / 1000, 2), 'K') AS "Rows"  
,CONCAT(ROUND(data_length / ( 1024 * 1024  ), 2), 'M') AS "Row Size"  
,CONCAT(ROUND(index_length / ( 1024 * 1024  ), 2), 'M') AS "Index Size"  
,CONCAT(ROUND(( data_length + index_length ) / ( 1024 * 1024  ), 2), 'M') AS "Total"  
,ROUND(index_length / data_length, 2) "Row / Index Ratio"  
FROM information_schema.TABLES  
ORDER BY data_length + index_length DESC  
LIMIT 10; 
```

### **等待事件查看**
```
SELECT 
r.trx_id waiting_trx_id 
,r.trx_mysql_thread_id waiting_thread 
,r.trx_query waiting_query 
,b.trx_id blocking_trx_id 
,b.trx_mysql_thread_id blocking_thread 
,b.trx_query blocking_query 
FROM information_schema.innodb_lock_waits w 
JOIN information_schema.innodb_trx b ON b.trx_id = w.blocking_trx_id 
JOIN information_schema.innodb_trx r ON r.trx_id = w.requesting_trx_id;
```









# **Show命令的使用介绍**
[http://dev.mysql.com/doc/refman/5.7/en/show.html](http://dev.mysql.com/doc/refman/5.7/en/show.html)





# **用户和权限**
![图片](https://uploader.shimo.im/f/RidMckxtPnI6CQZH.png!thumbnail)




98. **查看当前登录用户**
25. **方法1**

mysql> system whoami
root
26. **方法2**

mysql> **select user();**
+----------------+
| user()         |
+----------------+
| root@localhost |
+----------------+
1 row in set (0.00 sec)














99. ** 添加、收回权限**

mysql> grant all on *.* to oldboy@'172.16.1.%' identified by 'oldboy123';
Query OK, 0 rows affected (0.00 sec)

mysql> show grants for oldboy@'172.16.1.%'\G
*************************** 1. row ***************************
Grants for oldboy@172.16.1.%: GRANT ALL PRIVILEGES ON *.* TO 'oldboy'@'172.16.1.%' IDENTIFIED BY PASSWORD '*FE28814B4A8B3309DAC6ED7D3237ADED6DA1E515'
1 row in set (0.00 sec)

mysql> revoke select ON *.* from 'oldboy'@'172.16.1.%';
Query OK, 0 rows affected (0.00 sec)

mysql> show grants for oldboy@'172.16.1.%'\G
*************************** 1. row ***************************
Grants for oldboy@172.16.1.%: GRANT INSERT, UPDATE, DELETE, CREATE, DROP, RELOAD, SHUTDOWN, PROCESS, FILE, REFERENCES, INDEX, ALTER, SHOW DATABASES, SUPER, CREATE TEMPORARY TABLES, LOCK TABLES, EXECUTE, REPLICATION SLAVE, REPLICATION CLIENT, CREATE VIEW, SHOW VIEW, CREATE ROUTINE, ALTER ROUTINE, CREATE USER, EVENT, TRIGGER, CREATE TABLESPACE ON *.* TO 'oldboy'@'172.16.1.%' IDENTIFIED BY PASSWORD '*FE28814B4A8B3309DAC6ED7D3237ADED6DA1E515'
1 row in set (0.00 sec)

100. ** 查看权限**

show grants for 'oldboy'@'10.0.0.%';











101. ** mysql中的权限**

SELECT
INSERT
UPDATE
DELETE
CREATE
DROP
RELOAD
SHUTDOWN
PROCESS
FILE
REFERENCES
INDEX
ALTER
SHOW DATABASES
SUPER
CREATE TEMPORARY TABLES
LOCK TABLES
EXECUTE
REPLICATION SLAVE
REPLICATION CLIENT
CREATE VIEW
SHOW VIEW
CREATE ROUTINE
ALTER ROUTINE
CREATE USER
EVENT
TRIGGER
CREATE TABLESPACE

| 权限   | 授予表格列   | 含义   |
|:----|:----|:----|
| [ALL [PRIVILEGES]](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_all)   | “ all privileges ”的同义词   | 服务器管理   |
| [ALTER](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_alter)   | Alter_priv   | 表   |
| [ALTER ROUTINE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_alter-routine)   | Alter_routine_priv   | 存储例程   |
| [CREATE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create)   | Create_priv   | 数据库，表或索引   |
| [CREATE ROUTINE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create-routine)   | Create_routine_priv   | 存储例程   |
| [CREATE TABLESPACE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create-tablespace)   | Create_tablespace_priv   | 服务器管理   |
| [CREATE TEMPORARY TABLES](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create-temporary-tables)   | Create_tmp_table_priv   | 表   |
| [CREATE USER](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create-user)   | Create_user_priv   | 服务器管理   |
| [CREATE VIEW](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_create-view)   | Create_view_priv   | 查看   |
| [DELETE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_delete)   | Delete_priv   | 表   |
| [DROP](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_drop)   | Drop_priv   | 数据库，表或视图   |
| [EVENT](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_event)   | Event_priv   | 数据库   |
| [EXECUTE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_execute)   | Execute_priv   | 存储例程   |
| [FILE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_file)   | File_priv   | 服务器主机上的文件访问   |
| [GRANT OPTION](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_grant-option)   | Grant_priv   | 数据库，表或存储例程   |
| [INDEX](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_index)   | Index_priv   | 表   |
| [INSERT](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_insert)   | Insert_priv   | 表或列   |
| [LOCK TABLES](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_lock-tables)   | Lock_tables_priv   | 数据库   |
| [PROCESS](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_process)   | Process_priv   | 服务器管理   |
| [PROXY](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_proxy)   | 请参阅proxies_priv表   | 服务器管理   |
| [REFERENCES](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_references)   | References_priv   | 数据库或表   |
| [RELOAD](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_reload)   | Reload_priv   | 服务器管理   |
| [REPLICATION CLIENT](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_replication-client)   | Repl_client_priv   | 服务器管理   |
| [REPLICATION SLAVE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_replication-slave)   | Repl_slave_priv   | 服务器管理   |
| [SELECT](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_select)   | Select_priv   | 表或列   |
| [SHOW DATABASES](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_show-databases)   | Show_db_priv   | 服务器管理   |
| [SHOW VIEW](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_show-view)   | Show_view_priv   | 查看   |
| [SHUTDOWN](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_shutdown)   | Shutdown_priv   | 服务器管理   |
| [SUPER](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_super)   | Super_priv   | 服务器管理   |
| [TRIGGER](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_trigger)   | Trigger_priv   | 表   |
| [UPDATE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_update)   | Update_priv   | 表或列   |
| [USAGE](https://dev.mysql.com/doc/refman/5.7/en/privileges-provided.html#priv_usage)   | “ no privileges ”的同义词   | 服务器管理   |







102. ** 创建用户**

CREATE USER 'username'@'localhost' IDENTIFIED BY 'passwd';


mysql>** ****create user oldgirl@'10.0.0.%' identified by '123456';**
Query OK, 0 rows affected (0.00 sec)

mysql> show grants for oldgirl@'10.0.0.%'\G
*************************** 1. row ***************************
Grants for oldgirl@10.0.0.%: GRANT USAGE ON *.* TO 'oldgirl'@'10.0.0.%' IDENTIFIED BY PASSWORD '*6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9'
1 row in set (0.00 sec)


103. ** 创建一个权限和root一样大的system用户**

**grant all on *.* to 'system'@'localhost' identified by '123456' with grant option;**

104. ** 查看用户**

select user,host,password from mysql.user;

MySQL5.7
mysql> select user,host,authentication_string from mysql.user;
+---------------+-----------+-------------------------------------------+
| user          | host      | authentication_string                     |
+---------------+-----------+-------------------------------------------+
| root          | localhost | *6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9 |
| mysql.session | localhost | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE |
| mysql.sys     | localhost | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE |
+---------------+-----------+-------------------------------------------+
3 rows in set (0.00 sec)


105. ** 删除用户**

方法1
mysql> drop user 'oldgirl'@'10.0.0.%';

方法2
mysql> delete from mysql.user where host='127.0.0.1';

mysql> delete from mysql.user where user='oldgirl';

106. ** 刷新权限**

直接对表内容的修改，需要刷新权限
mysql> flush privileges;


107. ** 授权**

mysql> **grant all on *.* to oldgirl@'10.0.0.%';**
Query OK, 0 rows affected (0.00 sec)

mysql> show grants for oldgirl@'10.0.0.%'\G
*************************** 1. row ***************************
Grants for oldgirl@10.0.0.%: GRANT ALL PRIVILEGES ON *.* TO 'oldgirl'@'10.0.0.%' IDENTIFIED BY PASSWORD '*6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9'
1 row in set (0.00 sec)


mysql> **grant all on *.* to oldgirl@'10.0.0.0/255.255.255.0';**

108. ** 权限规则**

给库授权相当于给目录授权
给表授权相当于给文件授权
权限取并集



109. ** 授权注意事项**

select,insert,update,delete 4个权限即可，有的开源软件，例如discuz bbs，还需要create,drop等比较危险的权限。

110. ** 严格的授权：重视安全，忽略了方便**

GRANT SELECT, INSERT, UPDATE, DELETE ON `blog`.* TO 'blog'@'10.0.0.%' identified by 'oldboy456';

111. ** 生产环境从库（只读）用户的授权**

GRANT SELECT ON `blog`.* TO 'blog'@'10.0.0.%' identified by 'oldboy456';


15. **mysqladmin的相关命令**

mysqladmin password oldboy123  #<==设置密码
mysqladmin -uroot -poldboy123 password oldboy  #<==修改密码
mysqladmin -uroot -poldboy123 status   #<==查看状态
mysqladmin -uroot -poldboy123 extended-status    #<==show global status;
mysqladmin -uroot -poldboy123 -S /data/3306/mysql.sock -i 1 status
mysqladmin -uroot -poldboy123 flush-logs
mysqladmin -uroot -poldboy123 processlist
mysqladmin -uroot -poldboy123 processlist -i 1 实时跟踪。
watch mysqladmin -uroot -poldboy123 processlist
mysqladmin -uroot -poldboy123 shutdown  #<==关闭mysql
mysqladmin -uroot -poldboy123 variables  #<==show variables

mysqladmin支持下列命令
create databasename：创建一个新数据库；
drop databasename：删除一个数据库及其所有表；
extended-status：给出服务器的一个扩展状态消息；
flush-hosts：清空所有缓存的主机；
flush-logs：清空所有日志；
flush-tables：清空所有表；
flush-privileges：再次装载授权表(同reload)；
kill id,id,...：杀死mysql线程；
password 新口令：将老密码改为新密码；
ping：检查mysqld是否活着；
processlist：显示服务其中活跃线程列表；
reload：重载授权表；
refresh：清空所有表并关闭和打开日志文件；
shutdown：关掉服务器；
status：给出服务器的简短状态消息；
variables：打印出可用变量；
version：得到服务器的版本信息。


 [http://man.linuxde.net/mysqladmin](http://man.linuxde.net/mysqladmin)


16. **mysql相关命令**

mysql [OPTIONS] [database]   #命令方式
 - , --help         #显示帮助信息并退出
 -I, --help          #显示帮助信息并退出
 --auto-rehash       #自动补全功能，就像linux里面，按Tab键出提示差不多，下面有例子

 -A, --no-auto-rehash  #默认状态是没有自动补全功能的。-A就是不要自动补全功能
 -B, --batch         #mysql不使用历史文件，禁用交互
 (Enables --silent)
 --character-sets-dir=name   #字体集的安装目录                    
 --default-character-set=name    #设置数据库的默认字符集
 -C, --compress      #在客户端和服务器端传递信息时使用压缩
 -#, --debug[=#]     #bug调用功能
 -D, --database=name #使用哪个数据库
 --delimiter=name    #mysql默认命令结束符是分号，下面有例子
 -e, --execute=name  #执行mysql的sql语句
 -E, --vertical      #垂直打印查询输出
 -f, --force         #如果有错误跳过去，继续执行下面的
 -G, --named-commands
 /*Enable named commands. Named commands mean this program's
 internal commands; see mysql> help . When enabled, the
 named commands can be used from any line of the query,
 otherwise only from the first line, before an enter.
 Disable with --disable-named-commands. This option is
 disabled by default.*/
 -g, --no-named-commands
 /*Named commands are disabled. Use \* form only, or use
 named commands only in the beginning of a line ending
 with a semicolon (;) Since version 10.9 the client now
 starts with this option ENABLED by default! Disable with
 '-G'. Long format commands still work from the first
 line. WARNING: option deprecated; use
 --disable-named-commands instead.*/
 -i, --ignore-spaces #忽视函数名后面的空格.
 --local-infile      #启动/禁用 LOAD DATA LOCAL INFILE.
 -b, --no-beep       #sql错误时，禁止嘟的一声
 -h, --host=name     #设置连接的服务器名或者Ip
 -H, --html          #以html的方式输出
 -X, --xml           #以xml的方式输出
 --line-numbers      #显示错误的行号
 -L, --skip-line-numbers  #忽略错误的行号
 -n, --unbuffered    #每执行一次sql后，刷新缓存
 --column-names      #查寻时显示列信息，默认是加上的
 -N, --skip-column-names  #不显示列信息
 -O, --set-variable=name  #设置变量用法是--set-variable=var_name=var_value
 --sigint-ignore     #忽视SIGINT符号(登录退出时Control-C的结果)
 -o, --one-database  #忽视除了为命令行中命名的默认数据库的语句。可以帮跳过日志中的其它数据库的更新。
 --pager[=name]      #使用分页器来显示查询输出，这个要在linux可以用more,less等。
 --no-pager          #不使用分页器来显示查询输出。
 -p, --password[=name] #输入密码
 -P, --port=#        #设置端口
 --prompt=name       #设置mysql提示符
 --protocol=name     #使用什么协议
 -q, --quick         #不缓存查询的结果，顺序打印每一行。如果输出被挂起，服务器会慢下来，mysql不使用历史文件。
 -r, --raw           #写列的值而不转义转换。通常结合--batch选项使用。
 --reconnect         #如果与服务器之间的连接断开，自动尝试重新连接。禁止重新连接，使用--disable-reconnect。
 -s, --silent        #一行一行输出，中间有tab分隔
 -S, --socket=name   #连接服务器的sockey文件
 --ssl               #激活ssl连接，不激活--skip-ssl
 --ssl-ca=name       #CA证书
 --ssl-capath=name   #CA路径
 --ssl-cert=name     #X509 证书
 --ssl-cipher=name   #SSL cipher to use (implies --ssl).
 --ssl-key=name      #X509 密钥名
 --ssl-verify-server-cert #连接时审核服务器的证书
 -t, --table         #以表格的形势输出
 --tee=name          #将输出拷贝添加到给定的文件中，禁时用--disable-tee
 --no-tee            #根--disable-tee功能一样
 -u, --user=name     #用户名
 -U, --safe-updates  #Only allow UPDATE and DELETE that uses keys.
 -U, --i-am-a-dummy  #Synonym for option --safe-updates, -U.
 -v, --verbose       #输出mysql执行的语句
 -V, --version       #版本信息
 -w, --wait          #服务器down后，等待到重起的时间
 --connect_timeout=# #连接前要等待的时间
 --max_allowed_packet=# #服务器接收／发送包的最大长度
 --net_buffer_length=# #TCP / IP和套接字通信缓冲区大小。
 --select_limit=#    #使用--safe-updates时SELECT语句的自动限制
 --max_join_size=#   #使用--safe-updates时联接中的行的自动限制
 --secure-auth       #拒绝用(pre-4.1.1)的方式连接到数据库
 --server-arg=name   #Send embedded server this as a parameter.
 --show-warnings     #显示警告
























17. **mysql变量查看与设置**

mysql> **show variables like '%key_buffer%';**
+-----------------+----------+
| Variable_name   | Value    |
+-----------------+----------+
| key_buffer_size | 16777216 |
+-----------------+----------+
1 row in set (0.00 sec)

mysql> **system grep key_buffer /data/3306/my.cnf;**
key_buffer_size = 16M

mysql>** set global key_buffer_size = 1024*1024*8;**
Query OK, 0 rows affected (0.00 sec)

mysql> **show variables like '%key_buffer%';**
+-----------------+---------+
| Variable_name   | Value   |
+-----------------+---------+
| key_buffer_size | 8388608 |
+-----------------+---------+
1 row in set (0.00 sec)

key_buffer_size  myisam引擎的索引的缓冲区


不重启数据库更改数据库参数小结
1、set global key_buffer_size = 1024*1024*32;  #<==及时生效，重启mysql失效。
2、配置文件也要改，编辑/etc/my.cnf，修改key_buffer_size = 32M。


mysql>** show variables like '%log_bin%';**
+---------------------------------+-------+
| Variable_name                   | Value |
+---------------------------------+-------+
| log_bin                         | ON    |
| log_bin_trust_function_creators | OFF   |
| sql_log_bin                     | ON    |
+---------------------------------+-------+

show session status;

mysql>** show global status like "%select%";**
+------------------------+-------+
| Variable_name          | Value |
+------------------------+-------+
| Com_insert_select      | 0     |
| Com_replace_select     | 0     |
| Com_select             | 16    |
| Select_full_join       | 0     |
| Select_full_range_join | 0     |
| Select_range           | 0     |
| Select_range_check     | 0     |
| Select_scan            | 17    |
+------------------------+-------+

18. **show命令**

show databases; #列出所有数据库
show tables; #列出默认数据库中的表
show tables from <database_name>  #列出指定数据库中的表
show columns from <table_name> #显示表的列结构
show processlist; #查看数据库里正在执行的SQL语句，可能无法看全完整SQL语句。
show full processlist;  #查看正在执行的完整SQL语句，完整显示。
set global key_buffer_size = 1024*1024*32 #不重启数据库调整数据库参数，直接生效，重启后失效。
show variables; #查看数据库的配置参数信息，例如：my.cnf里参数的生效情况。
show variables like '%log_bin%';"
kill ID  #杀掉SQL线程的命令，ID为线程号。
show session status #查看当前会话的数据库状态信息
show status; #列出当前数据库状态
show global status; #查看整个数据库运行状态信息，很重要，要分析并要做好监控。
show engine innodb status; #显示innodb引擎的性能状态（早期版本show innodb status）
show index from <table_name>  #显示表中有关索引和索引列的信息
show character set; #显示可用的字符集及其默认整理
show collation;  #显示每个字符集的整理

mysqlshow  [options]   [db_name  [table_name  [column_name] ] ]


19. ** 索引**

[https://dev.mysql.com/doc/refman/5.7/en/optimization-indexes.html](https://dev.mysql.com/doc/refman/5.7/en/optimization-indexes.html)

112. ** 索引介绍**

   数据库的索引就像书的目录一样，如果在字段上建立了索引，那么以索引列为查询条件时可以加快查询数据的速度
113. ** 索引类型**

BTREE:B+树索引  包括 主键、唯一、普通索引
HASH：HASH索引
FULLTEXT：全文索引
RTREE：R树索引


114. ** 创建主键索引**

1、在建表时，可以增加创建主键索引的语句
```
create table student(
id int(4) not null AUTO_INCREMENT,
name char(20) not null,
age tinyint(2) NOT NULL default '0',
dept varchar(16) default NULL,
primary key(id),
KEY index_name(name)
);
```


提示：
**1、****primary key(id)    ****主键**
**2、****KEY index_name(name)   **** name字段普通索引**
**优化：在唯一值多的列上建索引查询效率高**


create table student(
id int(4) not null,
name char(20) not null,
age tinyint(2) NOT NULL default '0',
dept varchar(16) default NULL
);




```
mysql> show create table student\G;
*************************** 1. row ***************************
       Table: student
Create Table: CREATE TABLE `student` (
  `id` int(4) NOT NULL AUTO_INCREMENT,
  `name` char(20) NOT NULL,
  `age` tinyint(2) NOT NULL DEFAULT '0',
  `dept` varchar(16) DEFAULT NULL,
  PRIMARY KEY (`id`),
  KEY `index_name` (`name`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8
1 row in set (0.00 sec)
```


mysql> **desc student;**
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(4)      | NO   | PRI | NULL    | auto_increment |
| name  | char(20)    | NO   | MUL | NULL    |                |
| age   | tinyint(2)  | NO   |     | 0       |                |
| dept  | varchar(16) | YES  |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
4 rows in set (0.00 sec)


```
create table student(
id int(4) not null,
name char(20) not null,
age tinyint(2) NOT NULL default '0',
dept varchar(16) default NULL,
primary key(id),
KEY index_name(name)
);
```


**创建主键索引**
```
alter table student change id id int primary key auto_increment;
```
**提示：只有int类型且为primary key  才可以使用 auto_increment**

alter table student change column id id int(4) not null auto_increment primary key;


115. ** 创建普通索引************

普通索引一般是建表以后，在根据需求（表慢了）添加的

116. ** 查看索引**

mysql> **show index from student\G;**
*************************** 1. row ***************************
        Table: student
   Non_unique: 0
     Key_name: PRIMARY
 Seq_in_index: 1
  Column_name: id
    Collation: A
  Cardinality: 0
     Sub_part: NULL
       Packed: NULL
         Null:
   Index_type: BTREE
      Comment:
Index_comment:
*************************** 2. row ***************************
        Table: student
   Non_unique: 1
     Key_name: index_name
 Seq_in_index: 1
  Column_name: name
    Collation: A
  Cardinality: 0
     Sub_part: NULL
       Packed: NULL
         Null:
   Index_type: BTREE
      Comment:
Index_comment:
2 rows in set (0.00 sec)

mysql> **show index from student where column_name='dept'\G;**
*************************** 1. row ***************************
        Table: student
   Non_unique: 1
     Key_name: ind_dept
 Seq_in_index: 1
  Column_name: dept
    Collation: A
  Cardinality: 0
     Sub_part: NULL
       Packed: NULL
         Null: YES
   Index_type: BTREE
      Comment:
Index_comment:
1 row in set (0.00 sec)

117. ** 删除索引**
```
alter table student drop index index_name;
```

drop index index_name on test;


删除主键（带自增的主键不能被删除）  **工作中没有这么做的**
**alter table student drop primary key;**


118. ** 添加索引**

添加索引的速度取决于当时的数据量，数据量越大，创建索引越慢
生产场景：
**如果数据量特别大的时候，不适合建立索引，会影响用户访问，曾经400-500条记录的表，建立索引，花了90-180秒**
**尽量选择在业务低谷时建立索引**

```
alter table student add index index_name(name);
```

```
create index index_name on test(name);
```


119. ** 对字段的前n个字符创建普通索引**

给student表的dept字段前8个字节创建索引
create index index_dept on student(dept(8));

alter table student add index index_dept(name(8));


120. ** 为表的多个字段创建联合索引**

**create index index_name_dept on student(name,dept);**



121. ** 多字段联合索引（不同字段，不同字符）**

**create index ind_name_dept on student(name(8),dept(10));**



























122. ** 统计表记录的唯一值**

mysql> select count(user && host) from mysql.user;
+---------------------+
| count(user && host) |
+---------------------+
|                   2 |
+---------------------+
1 row in set (0.00 sec)

mysql> select count(distinct user,host) from mysql.user;
+---------------------------+
| count(distinct user,host) |
+---------------------------+
|                         2 |
+---------------------------+
1 row in set (0.00 sec)

mysql> select count(user) from mysql.user;
+-------------+
| count(user) |
+-------------+
|           2 |
+-------------+
1 row in set (0.00 sec)

mysql> select count(distinct user) from mysql.user;
+----------------------+
| count(distinct user) |
+----------------------+
|                    1 |
+----------------------+
1 row in set (0.00 sec)

**提示：尽量在唯一值多的大表上建立索引**


提示：按条件列查询数据时，联合索引是有前缀生效特性的
index(a,b,c)
仅a, ab, abc 三个查询条件列可以走索引
b, bc, ac, c 等无法使用索引了
尽量把最常用作为查询条件的列，放在第一位置,也可以多列创建联合主键

123. ** 创建唯一索引（非主键）**

mysql> **create unique index uni_ind_name on student(name);**
Query OK, 0 rows affected (0.11 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> desc student;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| name  | char(20)    | NO   | **UNI** | NULL    |                |
| age   | tinyint(2)  | NO   |     | 0       |                |
| dept  | varchar(16) | YES  |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
4 rows in set (0.00 sec)


alter table testtab add unique index inx_uni(name);













## **执行计划**
[https://dev.mysql.com/doc/refman/5.7/en/explain-output.html](https://dev.mysql.com/doc/refman/5.7/en/explain-output.html)

** explain 或 desc**

27. ** 查看执行计划，是否走索引**
```
mysql> explain select name from country  where name like "c%" limit 10;
+----+-------------+---------+------+---------------+------+---------+------+------+-------------+
| id | select_type | table   | type | possible_keys | key  | key_len | ref  | rows | Extra       |
+----+-------------+---------+------+---------------+------+---------+------+------+-------------+
|  1 | SIMPLE      | country | ALL  | NULL          | NULL | NULL    | NULL |  239 | Using where |
+----+-------------+---------+------+---------------+------+---------+------+------+-------------+
```


type : 表示MySQL在表中找到所需行的方式，又称“访问类型”，
常见类型如下:
ALL, index,  range, ref, eq_ref, const, system, NULL
从左到右，性能从最差到最好

ALL：Full Table Scan， MySQL将遍历全表以找到匹配的行
index：Full Index Scan，index与ALL区别为index类型只遍历索引树
range:索引范围扫描，对索引的扫描开始于某一点，返回匹配值域的行。
显而易见的索引范围扫描是带有between或者where子句里带有<,>查询。
当mysql使用索引去查找一系列值时，例如IN()和OR列表，也会显示range（范围扫描）,当然性能上面是有差异的。

ref：使用非唯一索引扫描或者唯一索引的前缀扫描，返回匹配某个单独值的记录行

eq_ref：类似ref，区别就在使用的索引是唯一索引，对于每个索引键值，表中只有一条记录匹配，简单来说，
就是多表连接中使用primary key或者 unique key作为关联条件

const、system：当MySQL对查询某部分进行优化，并转换为一个常量时，使用这些类型访问。
如将主键置于where列表中，MySQL就能将该查询转换为一个常量

NULL：MySQL在优化过程中分解语句，执行时甚至不用访问表或索引，
   例如从一个索引列里选取最小值可以通过单独索引查找完成。


压力测试
```
 mysqlslap --defaults-file=/etc/my.cnf \
--concurrency=100 --iterations=1 --create-schema='oldboy' \
--query="select * from oldboy.t_100w where k2='780P'" engine=innodb \
--number-of-queries=2000 -uroot -p123 -verbose
```



28. ** 查看是否有索引**
```
show index from country;
```



29. ** 查看唯一值数量，查看是否合适做索引**

mysql> select count(distinct name) from country;
+----------------------+
| count(distinct name) |
+----------------------+
|                  239 |
+----------------------+

mysql> select count(name) from country;
+-------------+
| count(name) |
+-------------+
|         239 |
+-------------+



30. ** 创建索引**

mysql> alter table country add index name_idx(name);
Query OK, 0 rows affected (0.02 sec)
Records: 0  Duplicates: 0  Warnings: 0
31. ** 再次查看执行计划，是否走索引**

mysql> explain select name from country  where name like "c%" limit 10;
+----+-------------+---------+-------+---------------+----------+---------+------+------+--------------------------+
| id | select_type | table   | type  | possible_keys | key      | key_len | ref  | rows | Extra                    |
+----+-------------+---------+-------+---------------+----------+---------+------+------+--------------------------+
|  1 | SIMPLE      | country | range | name_idx      | name_idx | 52      | NULL |   22 | Using where; Using index |
+----+-------------+---------+-------+---------------+----------+---------+------+------+--------------------------+






124. ** 创建索引的基本知识小结**

1、索引类似书的目录，可以加快查询数据的速度
2、索引创建在表的列（字段）上
3、索引会加快查询速度，也会影响更新速度，因为更新要维护索引数据
4、索引不是越多越好，在频繁查询的表语句where后的条件列上创建索引
5、在大表以及重复值少的条件列上创建索引
6、多个列联合索引有前缀生效特性
7、当字段内容前N个字符已经接近唯一时，可以对字段的前N个字符创建索引
8、索引分为主键、唯一、普通索引

create table test(id int,name varchar(20),gender enum('F','M'),age int,mail varchar(30),bridate datetime);












20. **  view视图**

视图方便查询，便于程序可读

```
create view view_l_aa as select * from test1 where name='aa';
```










21. ** mysql日志**

[https://dev.mysql.com/doc/refman/5.7/en/server-logs.html](https://dev.mysql.com/doc/refman/5.7/en/server-logs.html)


125. ** 错误日志**

mysql的错误日志（error log）记录mysql服务进程mysqld在启动/关闭或运行过程中遇到的错误信息

配置方法：
方法1:
[mysqld_safe]
```
log_error= /application/mysql-5.6.34/data/mysql-db01.err
```
方法2：
```
mysqld_safe --defaults-file=/etc/my.cnf --log-error=/application/mysql-5.6.34/data/mysql-db01.err &
```


mysql> show variables like "%log_error%";
+---------------+---------------------------------+
| Variable_name | Value                           |
+---------------+---------------------------------+
| log_error     | /data/3306/mysql_oldboy3306.err |
+---------------+---------------------------------+
1 row in set (0.00 sec)

5.6版本
mysql> show variables like '%log_error%';
+---------------------+-----------------------------------------------+
| Variable_name       | Value                                         |
+---------------------+-----------------------------------------------+
| binlog_error_action | IGNORE_ERROR                                  |
| log_error           | /application/mysql-5.6.34/data/mysql-db01.err |
+---------------------+-----------------------------------------------+





126. ** 普通查询日志（general query log）**

普通查询日志（general query log），记录客户端连接信息和执行的sql语句信息

[root@MySQL ~]# grep gene /data/3306/my.cnf
general_log = on
general_log_file = /data/3306/data/MySQL_oldboy.log


临时生效：

mysql> set global general_log_file = "/data/3306/data/MySQL_oldboy.log";
Query OK, 0 rows affected (0.04 sec)

mysql> show variables like 'general_log%';
+------------------+----------------------------------+
| Variable_name    | Value                            |
+------------------+----------------------------------+
| general_log      | ON                               |
| general_log_file | /data/3306/data/MySQL_oldboy.log |
+------------------+----------------------------------+
2 rows in set (0.00 sec)
mysql> set global general_log = on; 
Query OK, 0 rows affected (0.03 sec)













127. ** 慢查询日志**

mysql> show variables like '%slow_query%';
+---------------------+----------------------------------------------------+
| Variable_name       | Value                                              |
+---------------------+----------------------------------------------------+
| slow_query_log      | OFF                                                |
| slow_query_log_file | /application/mysql-5.6.34/data/mysql-db01-slow.log |
+---------------------+----------------------------------------------------+


slow_query_log = on
long_query_time = 1                  #超过1秒，记录到slow log 里
log_queries_not_using_indexes         # 没有走索引的语句，slow log 里
log-slow-queries = /data/3306/slow.log   # slow log 文件
min_examined_row_limit = 1000       #记录查询结果大于1000条的sql语句



mysql5.6
slow-query-log=1
long_query_time = 2
log_queries_not_using_indexes
slow_query_log_file= /data/3306/slow.log
min_examined_row_limit = 1000


慢日志切割
[root@db01 data]# mv slow.log slow_$(date +%F).log
[root@db01 data]# **mysqladmin flush-log**** **








mysqldumpslow
/path/mysqldumpslow-s c -t 10 /database/mysql/slow-log这会输出记录次数最多的10条SQL语句，其中：

-s 是表示按照何种方式排序，c、t、l、r分别是按照运行次数、时间、查询时间、返回的记录数来排序，ac、at、al、ar，表示相应的倒叙；

-t 是top n的意思，即为返回前面多少条的数据；

-g后边可以写一个正则匹配模式，大小写不敏感的；
例子：/path/mysqldumpslow-s r -t 10 /database/mysql/slow-log得到返回记录集最多的10个查询。/path/mysqldumpslow-s t -t 10 -g “left join”/database/mysql/slow-log得到按照时间排序的前10条里面含有左连接的查询语句。




mysqlsla分析慢查询

mysqlsla分析案例
http://blog.itpub.net/7607759/viewspace-692828/

慢查询日志分析工具mysqlsla或pt-query-digest(推荐)
pt-query-diges，mysqldumpslow, mysqlsla, myprofi, mysql-explain-slow-log, mysqllogfilter 比较







22. **  二进制日志(binlog)**
128. ** 二进制日志（binary log）介绍**

     二进制日志，记录数据的增删改（insert,update,delete,create,drop,alter）的相关信息，用户主从复制及增量恢复的基础


129. ** 二进制日志（binary log）调整**

mysql> show variables like '%log_bin%';
+---------------------------------+------------------------------------------------+
| Variable_name                   | Value                                          |
+---------------------------------+------------------------------------------------+
| log_bin                         | ON                                             |
| log_bin_basename                | /application/mysql-5.6.34/data/mysql-bin       |
| log_bin_index                   | /application/mysql-5.6.34/data/mysql-bin.index |
| log_bin_trust_function_creators | OFF                                            |
| log_bin_use_v1_row_events       | OFF                                            |
| sql_log_bin                     | ON                                             |
+---------------------------------+------------------------------------------------+


[root@db01 ~]# grep log-bin /data/3306/my.cnf
log-bin = /data/3306/mysql-bin
binlog_format=row

130. ** 临时不记录binlog**

mysql> set session sql_log_bin = OFF;
Query OK, 0 rows affected (0.00 sec)


131. ** 二进制日志log-bin作用**

1、以二进制形式记录对数据库进行的写操作SQL语句
2、用于MySQL主从复制
3、增量数据备份及恢复
set sql_log_bin=0
source /opt/new.sql



132. ** binlog文件切割条件**

1、数据库重启，自动切割新文件
2、mysqladmin -S /data/3306/mysql.sock -uroot -poldboy flush-logs
3、文件达到1.1G，自动切割




133. ** 查看binlog方法**

mysqlbinlog mysql-bin.000001

show master status;
show binary logs;
show binlog events in 'mysql-bin.000001';

134. ** 查看binlog日志详细内容**
```
mysqlbinlog --base64-output=decode-rows -v mysql-bin.000007
```


135. ** mysqlbinlog 命令筛选指定库的数据**
```
mysqlbinlog -d blog mysql-bin.000001 -r /root/blog.sql
```

```
mysqlbinlog --base64-output=decode-rows -d blog -v /application/mysql/data/mysql-bin.000001 -r /root/blog.sql
```
注意：只有切入数据库（use 库名）再插入数据才能在binlog中找到数据


```
mysqlbinlog oldboy-bin.000009 --start-position=8826 --stop-position=8975 -r pos.sql
```




136. ** 刷新binlog**

flush logs;




137. ** 删除binlog日志方法**

1、设置参数自动删除
```
expire_logs_days = 7  #<==删除7天前的日志
```

2、从头删到指定的文件位置
```
mysql> purge binary logs to 'mysql-bin.000004';      # mysql-bin.000004 不会被删除
Query OK, 0 rows affected (0.03 sec)

mysql> system ls -l /data/3306/mysql-bin*
-rw-rw---- 1 mysql mysql   126 8月  21 16:31 /data/3306/mysql-bin.000004
-rw-rw---- 1 mysql mysql   126 8月  21 16:32 /data/3306/mysql-bin.000005
-rw-rw---- 1 mysql mysql 15881 8月  28 19:16 /data/3306/mysql-bin.000006
-rw-rw---- 1 mysql mysql    84 8月  28 19:26 /data/3306/mysql-bin.index
```

3、按照时间删除
```
mysql> PURGE MASTER LOGS BEFORE '2016-08-28 13:00:00';
Query OK, 0 rows affected (0.02 sec)

mysql> system ls -l /data/3306/mysql-bin*             
-rw-rw---- 1 mysql mysql 15881 8月  28 19:16 /data/3306/mysql-bin.000006
-rw-rw---- 1 mysql mysql    28 8月  28 19:28 /data/3306/mysql-bin.index
```


4、删除3天前的binlog日志
```
mysql> PURGE MASTER LOGS BEFORE DATE_SUB(NOW( ), INTERVAL 3 DAY);
Query OK, 0 rows affected (0.00 sec)

mysql> system ls -l /data/3306/mysql-bin*
-rw-rw---- 1 mysql mysql 15881 8月  28 19:16 /data/3306/mysql-bin.000006
-rw-rw---- 1 mysql mysql    28 8月  28 19:28 /data/3306/mysql-bin.index
```

[root@centos72 data]# pwd
/application/mysql/data
[root@centos72 data]# ls
auto.cnf      ibdata1      mysql             mysql-bin.000003    test
centos72.err  ib_logfile0  mysql-bin.000001  mysql-bin.index
centos72.pid  ib_logfile1  mysql-bin.000002  performance_schema
[root@centos72 data]# **cat mysql-bin.index**** **
./mysql-bin.000001
./mysql-bin.000002
./mysql-bin.000003


expire_logs_days = 7    #  删除7天前的日志


mysql> set global expire_logs_days = 7;
Query OK, 0 rows affected (0.00 sec)

mysql> show variables like 'expire_logs_days%';
+------------------+-------+
| Variable_name    | Value |
+------------------+-------+
| expire_logs_days | 7     |
+------------------+-------+

138. ** 清除所有binlog，  从零开始记录binlog**
```
mysql> reset master;
Query OK, 0 rows affected (0.01 sec)
```


log-bin = mysql-bin
sync-binlog = 1
innodb_support_xa = 1

139. ** 查看binlog事件**

show binlog events in 'mysql-bin.000002';


23. **  mysql binlog三种模式**

默认为STATEMENT模式（语句模式）
140. **  STATEMENT模式**

  每一条被修改数据的sql都会记录到master的bin-log中，slave在复制的时候sql进程会解析成和原来master端执行过的相同的sql来再次执行
优点： 记录的记录简单，内容少
    statement 下的优点首先解决了row 下的缺点，不需要记录每一行数据的变化，减少bin-log日志量，节约磁盘IO，提高性能。因为它只需要记录在master上执行的语句的细节，以及执行语句时候的上下文的信息
缺点：导致主从不一致
    由于它是记录的执行语句，所以，为了让这些语句再slave端也能正确执行，那么它还必须记录每条语句在执行的时候的一些相关信息，也就是上下文信息，以保证所有语句在slave端执行的时候能够得到和在master端执行时候相同的结果。另外就是，由于mysql现在发展比较快，很多的新功能不断的加入，使mysql的复制遇到了不小的挑战，自然复制的时候涉及到越复杂的内容，bug也就越容易出现。在statement下，目前已经发现的就有不少情况会造成mysql的复制出现问题，主要是修改数据的时候使用了某些特定的函数或者功能的时候会出现，比如：sleep（）函数在有些版本中就不能正确复制，在存储过程中使用了last_insert_id（）函数，可能会使slave和master上得到不一致的id等等。由于row是基于每一行来记录的变化，所以不会出现类似的问题
32. **永久设置**

binlog_format = 'STATEMENT'
33. **临时设置**
```
 mysql> set global binlog_format = 'STATEMENT';
Query OK, 0 rows affected (0.00 sec)
```

34. **查看**
```
mysql> show variables like "%binlog_format%";
+---------------+-----------+
| Variable_name | Value     |
+---------------+-----------+
| binlog_format | STATEMENT |
+---------------+-----------+
```



141. **  ROW**

行级模式
优点：记录数据很细（逐行），主从复制容易保持一致
缺点：占用大量磁盘空间，降低磁盘性能
35. **永久设置**

binlog_format = 'ROW'
36. **临时设置**

mysql> set global binlog_format = '**ROW**';
Query OK, 0 rows affected (0.00 sec)








142. ** MIXED（混合）**

智能模式
37. **永久设置**

binlog_format = 'MIXED'
38. **临时设置**

mysql> set global binlog_format = '**MIXED**';
Query OK, 0 rows affected (0.00 sec)



143. ** 企业场景如何选择binlog的模式**

1、互联网公司，使用mysql的功能相对少（存储过程、触发器、函数）
   选择默认的语句模式，statement    中小公司
2、公司如果用到使用mysql的特殊功能（存储过程、触发器、函数）
   则选择mixed模式
3、公司如果用到使用mysql的特殊功能（存储过程、触发器、函数），又希望数据最大化一致，此时最好ROW模式


24. ** mysql相关企业案例**

mysql -e "kill 89;" 
企业案例：mysql sleep线程过多的问题案例。
mysql> show processlist;                
+----+------+-----------+------+---------+------+-------+------------------+
| Id | User | Host      | db   | Command | Time | State | Info             |
+----+------+-----------+------+---------+------+-------+------------------+
| 89 | root | localhost | NULL | Query   |    0 | NULL  | show processlist |
+----+------+-----------+------+---------+------+-------+------------------+
1 row in set (0.00 sec)
mysql> kill 89;
慢查询堵了数据库，mysql> kill 84; 84是ID，kill（insert,update）可能要丢数据。

解决办法：
mysql> show variables like '%_timeout%';
+----------------------------+----------+
| Variable_name              | Value    |
+----------------------------+----------+
| connect_timeout            | 10       |
| interactive_timeout        | 28800    |
| wait_timeout               | 28800    |
+----------------------------+----------+
10 rows in set (0.00 sec)
set global wait_timeout = 60;
set global interactive_timeout = 60; 
企业案例：mysql sleep线程过多的问题案例。
1、配置文件里修改：
[mysqld]
interactive_timeout = 120  #此参数设置后wait_timeout自动生效。
wait_timeout = 120
2、其他方法：
1.PHP程序中，不使用持久链接，即使用mysql_connect而不是pconnect（JAVA调整连接池）。
2.PHP程序执行完毕，应该显式调用mysql_close。
3.逐步分析MySQL的SQL查询及慢查询日志，找到查询过慢的SQL,优化之。
http://www.cnblogs.com/pedro/p/4627239.html 

[root@centos71 ~]# mysql -e "show variables like 'log_bin';"
+---------------+-------+
| Variable_name | Value |
+---------------+-------+
| log_bin       | ON    |
+---------------+-------+




mysql> **show variables like 'max_connections';**
+-----------------+-------+
|
Variable_name   | Value |
+-----------------+-------+
|
max_connections | 800   |
+-----------------+-------+
这台服务器最大连接数是256，然后查询一下该服务器响应的最大连接数；
mysql>** ****show global status like 'Max_used_connections';**
+----------------------+-------+
|
Variable_name        | Value |
+----------------------+-------+
|
Max_used_connections | 245    |
+----------------------+-------+
MySQL服务器过去的最大连接数是245，没有达到服务器连接数的上线800，不会出现1040错误。
**Max_used_connections /max_connections * 100% =**
**85%**
**最大连接数占上限连接数的****85%****左右****,****如果发现比例在****10%****以下，则说明****MySQL****服务器连接数的上限设置得过高了**




[root@db01 opt]# mysql -e "show variables;"|grep key_buffer
key_buffer_size 8388608

[root@db01 opt]# mysql -e "**set global key_buffer_size = 1024*1024*16;**"
[root@db01 opt]# mysql -e "show variables;"|grep key_buffer
key_buffer_size 16777216



show processlist;   #查看数据库里正在执行的sql语句，可能无法看全完整sql语句
show full processlist;  #查看正在执行的完整sql语句，完整显示
set global key_buffer_size = 1024* 1024*32;    #不重启数据库调整数据库参数，直接生效，重启失效
show variables;   #查看数据库的配置参数信息，例如：my.cnf里参数的生效情况
show variables like '%log_bin%';
kill ID     #杀掉sql线程的命令，ID为线程号
show session status;   #查看当前会话的数据库状态信息
show global status;   #查看整个数据库运行状态信息，很重要，要分析并做好监控
show engine innodb status;  #显示innodb显示innodb引擎的性能状态







25. **字符集**

[https://dev.mysql.com/doc/refman/5.7/en/charset-unicode-utf8mb3.html](https://dev.mysql.com/doc/refman/5.7/en/charset-unicode-utf8mb3.html)



144. ** 字符集介绍**

简单地说，字符集就是一套文字符号及其编码、比较规则的集合，第一个计算机字符集ASCII
mysql数据库字符集包括 字符集（CHARACTER）和 校对规则（COLLATION）两个概念，其中，字符集是用来定义mysql数据字符串的存储方式。而校对规则是定义比较字符串的方式

编译mysql时候，指定字符集了，这样以后建库的时候就直接create database oldboy;
二进制安装mysql，我们没有指定字符集，此时字符集默认latin1,此时需要建立建UTF8字符集的库，就需要指定UTF8字符集建库

create database oldboy DEFAULT CHARACTER SET UTF8 DEFAULT COLLATE=utf8_general_ci;


145. ** mysql数据库常见字符集介绍**

    在互联网环境中，使用mysql时常用的字符集有：
| 常用字符集   | 一个汉字长度（字节）   | 说明   |
|:----|:----:|:----|:----:|:----|:----:|
| GBK   | 2   | 不是国际标准，对中文环境支持的很好   |
| UTF8   | 3   | 中英文混合的环境，建议使用此字符集，用的比较多的   |
| latin1   | 1   | mysql的默认字符集   |
| utf8mb4   | 4   | UTF-8 Unicode，移动互联网   |



146. ** mysql如何选择合适的字符集**

1、如果处理各种各样的文字，发布到不同语言国家地区，应该选Unicode字符集，对mysql来说就是UTF-8（每个汉字三字节），如果应用需要处理英文，仅有少量汉字UTF-8更好
2、如果只需支持中文，并且数据量很大，性能要求也很高，可选GBK（定长 每个汉字占双字节，英文也占双字节），如果需大量运算，比较排序等，定长字符集，更快，性能高
3、处理移动互联网业务，可能需要使用utf8mb4字符集





147. ** 查看支持的字符集**

mysql> show character set;
+----------+-----------------------------+---------------------+--------+
| Charset  | Description                 | Default collation   | Maxlen |
+----------+-----------------------------+---------------------+--------+
| big5     | Big5 Traditional Chinese    | big5_chinese_ci     |      2 |
| dec8     | DEC West European           | dec8_swedish_ci     |      1 |
| cp850    | DOS West European           | cp850_general_ci    |      1 |
| hp8      | HP West European            | hp8_english_ci      |      1 |
| koi8r    | KOI8-R Relcom Russian       | koi8r_general_ci    |      1 |
| latin1   | cp1252 West European        | latin1_swedish_ci   |      1 |
| latin2   | ISO 8859-2 Central European | latin2_general_ci   |      1 |
| swe7     | 7bit Swedish                | swe7_swedish_ci     |      1 |
| ascii    | US ASCII                    | ascii_general_ci    |      1 |
| ujis     | EUC-JP Japanese             | ujis_japanese_ci    |      3 |
| sjis     | Shift-JIS Japanese          | sjis_japanese_ci    |      2 |
| hebrew   | ISO 8859-8 Hebrew           | hebrew_general_ci   |      1 |
| tis620   | TIS620 Thai                 | tis620_thai_ci      |      1 |
| euckr    | EUC-KR Korean               | euckr_korean_ci     |      2 |
| koi8u    | KOI8-U Ukrainian            | koi8u_general_ci    |      1 |
| gb2312   | GB2312 Simplified Chinese   | gb2312_chinese_ci   |      2 |
| greek    | ISO 8859-7 Greek            | greek_general_ci    |      1 |
| cp1250   | Windows Central European    | cp1250_general_ci   |      1 |
| gbk      | GBK Simplified Chinese      | gbk_chinese_ci      |      2 |

show charset;










148. ** 查看校对规则**

show collation;

ci：大小写不敏感
cs或bin：大小写敏感

149. **配置文件设置字符集**

my.cnf
character-set-server=utf8

150. ** 查看字符集**

mysql> show variables like 'character_set%';
+--------------------------+-------------------------------------------+
| Variable_name            | Value
+--------------------------+-------------------------------------------+
| character_set_client     | utf8            #客户端字符集
| character_set_connection | utf8            #客户端连接字符集
| character_set_database   | utf8            #数据库字符集，配置文件指定或建库建表指定
| character_set_filesystem | binary           #文件系统字符集
| character_set_results    | utf8            #客户端返回结果字符集
| character_set_server     | utf8           #服务器字符集，配置文件指定或建库建表指定
| character_set_system     | utf8          #系统字符集
| character_sets_dir       | /application/mysql-5.5.32/share/charsets/ |
+--------------------------+-------------------------------------------+
8 rows in set (0.00 sec)









151. ** 修改客户端字符集**
39. ** 方法一**

mysql> **set names latin1; **                   
Query OK, 0 rows affected (0.00 sec)

mysql> show variables like 'character_set%';
+--------------------------+-------------------------------------------+
| Variable_name            | Value                                     |
+--------------------------+-------------------------------------------+
| character_set_client     | latin1                                    |
| character_set_connection | latin1                                    |
| character_set_database   | gbk                                       |
| character_set_filesystem | binary                                    |
| character_set_results    | latin1                                    |
| character_set_server     | utf8                                      |
| character_set_system     | utf8                                      |
| character_sets_dir       | /application/mysql-5.5.49/share/charsets/ |
+--------------------------+-------------------------------------------+
8 rows in set (0.00 sec)

SET character_set_client = gbk;
SET character_set_results = gbk;
SET character_set_connection = gbk;





40. ** 方法2**

my.cnf
[client]
default-character-set=gbk
41. ** 方法3**

mysql -uroot -poldboy123 -S /data/3307/mysql.sock --default-character-set=latin1




152. ** 修改服务器端字符集**

1、配置文件
my.cnf
[mysqld]
character-set-server=gbk

2、命令行
set  character_set_server=gbk;
set  character_set_database=gbk;

153. **防止乱码**
42. ** 客服端字符集**

character_set_client
character_set_connection
character_set_results
控制
a、 set names gbk;
    set character_set_client=gbk;
b、 mysql -uroot -poldboy -S /data/3306/mysql.sock --default-character-set=latin1
c、 配置文件my.cnf
[client]
default-character-set=gbk












43. ** 数据库字符集**

character_set_database
character_set_server
控制：
a、配置文件
[mysqld]
character-set-server=gbk    #<==适合5.5
b、命令行
set character_set_server=gbk;
set character_set_database=gbk;

44. ** 建库指定字符集**

建库：
create database oldboy DEFAULT CHARACTER SET gbk COLLATE gbk_chinese_ci;
建表：
CREATE TABLE `test`(
   `id` int(4) NOT NULL AUTO_INCREMENT,
   `name`  char(20) NOT NULL,
   PRIMARY KEY(`id`)
) ENGINE=InnoDB DEFAULT CHARSET=gbk;

45. ** linux系统服务端字符集**

[root@oldboy ~]# cat /etc/sysconfig/i18n
LANG="zh_CN.UTF-8"
46. ** ssh 客户端字符集**

UTF-8



154. **库修改字符集**

alter database oldboy CHARACTER SET latin1 COLLATE = latin1_swedish_ci;
alter database oldboy CHARACTER SET utf8 collate utf8_general_ci;

155. **表修改字符集**

alter table test CHARACTER SET latin1;  



156. ** 字符集修改问题，对新数据生效，对老数据不行**

alter table test character set=gbk collate gbk_chinese_ci;
alter database oldboy CHARACTER SET latin1 COLLATE= latin1_swedish_ci;






157. ** 更改字符集总的思想**

1、数据库不要更新，导出所有数据
2、把导出的数据进行字符集替换（替换表和库）
3、修改my.cnf  更改mysql客户端服务端字符集，重启生效
4、导入更改过字符集的数据，包括表结构语句，提供服务
5、ssh客户端，以及程序更改为对应字符集










1、客户端字符集
character_set_client
character_set_connection
character_set_results
控制：
a.set names gbk;
  set character_set_client=gbk;
b.mysql -uroot -poldboy123 -S /data/3307/mysql.sock --default-character-set=latin1
c.配置文件my.cnf
[client]
default-character-set=gbk

2、数据库字符集：
character_set_database
character_set_server
控制：
a.配置文件
[mysqld]
character-set-server=gbk   #<==适合5.5
b.命令行
set character_set_server=gbk;  
set character_set_database=gbk; 

3、建库
建库：
create database oldboy DEFAULT CHARACTER SET gbk COLLATE gbk_chinese_ci;
建表：
CREATE TABLE `test` (
  `id` int(4) NOT NULL AUTO_INCREMENT,
  `name` char(20) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=gbk
4、linux系统服务端字符集
[root@oldboy ~]# cat /etc/sysconfig/i18n 
LANG="zh_CN.UTF-8"
5、SSH客户端字符集
UTF-8
6、开发的程序的字符集
简体 UTF8
http://download.comsenz.com/DiscuzX/3.2/Discuz_X3.2_SC_UTF8.zip 


# **引擎**
[https://dev.mysql.com/doc/refman/5.7/en/innodb-storage-engine.html](https://dev.mysql.com/doc/refman/5.7/en/innodb-storage-engine.html)



## **什么是存储引擎**
   在讲清楚什么是存储引擎之前，我们先来个比喻，我们都知道录制一个视频文件，可以转成不同的格式如mp4，avi，wmv等，而存在我们电脑的磁盘上也会存在于不同类型的文件系统中如windows里常见的ntfs，fat32，存在于linux里常见的ext3，ext4，xfs，但是，给我们或者用户看到实际视频内容都是一样的。直观区别是，占用系统的空间大小与清晰程度可能不同

[数据库引擎](http://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E5%BA%93%E5%BC%95%E6%93%8E)是用于存储、处理和保护数据的核心服务

数据库的引擎  ====   操作系统的文件系统


| **特征**   | **支持**   |
|:----|:----|
| **B树索引**   | **是**   |
| **备份/时间点恢复****（在服务器中实现，而不是在存储引擎中实现。）**   | **是**   |
| **群集数据库支持**   | **没有**   |
| **聚集索引**   | **是**   |
| **压缩数据**   | **是**   |
| **数据缓存**   | **是**   |
| **加密数据**   | **是（通过加密功能在服务器中实现;在MySQL 5.7及更高版本中，支持静态数据表空间加密。）**   |
| **外键支持**   | **是**   |
| **全文搜索索引**   | **是（在MySQL 5.6及更高版本中可以使用InnoDB对FULLTEXT索引的支持。）**   |
| **地理空间数据类型支持**   | **是**   |
| **地理空间索引支持**   | **是（在MySQL 5.7及更高版本中可以使用InnoDB对地理空间索引的支持。）**   |
| **哈希索引**   | **否（InnoDB在内部利用哈希索引来实现其自适应哈希索引功能。）**   |
| **索引缓存**   | **是**   |
| **锁定粒度**   | **行**   |
| **MVCC**   | **是**   |
| **复制支持****（在服务器中实现，而不是在存储引擎中实现。）**   | **是**   |
| **存储限制**   | **64TB**   |
| **T树索引**   | **没有**   |
| **transaction**   | **是**   |
| **更新数据字典的统计信息**   | **是**   |




![图片](https://images-cdn.shimo.im/ZsApxYDZLHIiFXJ8/image.image/png!thumbnail)


## 功能
数据读写
数据安全
提高性能
热备份
自动故障恢复
高可用方面支持




158. ** 常用的存储引擎**

innodb   myisam   memory   NDB.BLACKHOLE
innodb最重要


Innodb  目前MySQL版本的默认存储引擎，支持事务，支持行级锁，默认情况下表结构单独形成一个文件，表数据则统一在ibdata1文件中

MyISAM  老版本MySQL的默认存储引擎，不支持事务，表级锁，但是由于表创建的时候会创建独立的三个文件（表定义，表数据，表索引），所以适合文件级的迁移；另外，查询全表count（*）是直接从统计资料获取，所以速度非常快

Memory  数据存储在内存中，保证极高的数据存取速度，但关闭或者崩溃后数据会丢失，一般都用Redis代替

159. ** 查看默认的存储引擎 **

select @@default_storage_engine;
show variabbles like '%engine%';

160. ** 查看支持的存储引擎**
```
mysql> show engines;
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+
| Engine             | Support | Comment                                                        | Transactions | XA   | Savepoints |
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+
| InnoDB             | DEFAULT | Supports transactions, row-level locking, and foreign keys     | YES          | YES  | YES        |
| CSV                | YES     | CSV storage engine                                             | NO           | NO   | NO         |
| MyISAM             | YES     | MyISAM storage engine                                          | NO           | NO   | NO         |
| BLACKHOLE          | YES     | /dev/null storage engine (anything you write to it disappears) | NO           | NO   | NO         |
| PERFORMANCE_SCHEMA | YES     | Performance Schema                                             | NO           | NO   | NO         |
| MRG_MYISAM         | YES     | Collection of identical MyISAM tables                          | NO           | NO   | NO         |
| ARCHIVE            | YES     | Archive storage engine                                         | NO           | NO   | NO         |
| MEMORY             | YES     | Hash based, stored in memory, useful for temporary tables      | NO           | NO   | NO         |
| FEDERATED          | NO      | Federated MySQL storage engine                                 | NULL         | NULL | NULL       |
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+
```



查看数据库中myisam引擎的表
```
select table_schema,table_name,engine from tables where engine='myisam';
```


161. ** 设置存储引擎类型**

1、在启动配置文件中设置服务器存储引擎
[mysqld]
default-storage-engine=<Storage Engine>

2、使用SET 命令为当前客户机会话设置
SET @@storage_engine=<Storage Engine>;

3、在CREATE TABLE 语句指定：
CREATE TABLE t (iINT) ENGINE = <Storage Engine>;











26. **  myisam**

   MyISAM引擎是mysql关系数据库管理系统的默认存储引擎（mysql5.5.5以前）。这种mysql表存储结构从旧的ISAM代码扩展出许多有用的功能。在新版本的mysql中，InnoDB引擎由于其对事务参照完整性，以及更高的并发性等优点开始逐步的取MyISAM引擎

   提示：mysql5.1数据库的默认存储引擎为MyISAM
    每一个MyISAM的表都对应于硬盘上的三个文件。这三个文件有一样的文件名，但是有不同的扩展名指示其类型用途：frm文件保存表的定义，这个文件并不是MyISAM引擎的一部分，而是服务器的一部分；MYD保存表的数据；MYI是表的索引文件。MYD和MYI是MyISAM的关键点









162. ** MyISAM引擎特点**

1、不支持事务
事务是指逻辑上的一组操作，组成这组操作的各个单元，要么全成功要么全失败
2、表级锁定，数据更新时锁定整个表：其锁定机制是表级锁定，这虽然可以让锁定的实现成本很小但是也同时大大降低了其并发性能
3、读写互相阻塞：不仅会在写入的时候阻塞读取，MyISAM还会在读取的时候阻塞写入，但读本身并不会阻塞另外的读
4、只会缓存索引：MyISAM可以通过key_buffer_size缓存索引，以大大提高访问性能减少磁盘IO，但是这个缓存区只会缓存索引，而不会缓存数据
5、读取速度较快。占用资源相对少
6、不支持外键约束，但支持全文索引
7、MyISAM引擎是MySQL5.5.5前缺省的存储引擎



163. ** MyISAM引擎适用的生产业务场景**

1、不需要事务支持的业务（例如转账就不行）
2、一般为读数据比较多的应用，读写都频繁场景不适用，读多或者写多的都适合
3、读写并发访问相对较低的业务（纯读纯写高并发也可以）（锁定机制问题）
4、数据修改相对较少的业务（阻塞问题）
5、以读为主的业务，例如：数据库系统表、www，blog，图片信息数据库，用户数据库，商品库等业务
6、对数据一致性要求不是非常高的业务（不支持事务）
7、硬件资源比较差的机器可以用MyISAM（占用资源少）
小结：单一对数据库的读或写操作都可以使用MyISAM，所谓单一就是尽量纯读，或者纯写（insert,update,delete）等
8、使用读写分离的MySQL从库可以使用MyISAM


164. ** MyISAM引擎调优精要**

1、设置合适的索引（缓存机制）
2、调整读写优先级，根据实际需求确保重要操作更优先执行
3、启用延迟插入改善大批量写入性能（降低写入频率，尽可能多条数据一次性写入）
4、尽量顺序操作让insert数据都写入到尾部，减少堵塞
5、分解大的时间长的sql操作，降低单个操作的阻塞时间
6、降低并发数（减少对mysql访问），某些高并发场景通过应用进行排队队列机制Q队列
7、对于相对静态（更改不频繁）的数据库数据，充分利用query cache或memcached/redis
缓存服务可以极大的提高访问效率，网站动态内容静态化，减少对数据库的访问










165. ** MyISAM引擎重要参数：**

key_buffer_size = 1024M

166. ** session级别参数**

session 级别参数  每线程独占，不能太大

sort_buffer_size = 1M
join_buffer_size = 1M

167. ** myisam 特点：面试必答项**

1、Table-level locking
2、full-text search indexes
3、Index caches
4、No Transactions
5、占用资源少
6、读写阻塞、读读不阻塞
7、不支持外键


27. ** InnoDB引擎**

**5.7 InnoDB引擎**

![图片](https://uploader.shimo.im/f/sisocwxzIj0nkYuL.png!thumbnail)




168. ** 什么是InnoDB引擎**

      InnoDB引擎是mysql数据库的另一个重要的存储引擎，正成为目前mysql AB所发行新版的标准，被包含在所有二进制安装包里。和其它的存储引擎相比，InnoDB引擎的优点是支持兼容ACID的事务（类似于PostgreSQL），以及参数完整性（即对外键的支持）



[root@db01 ~]# egrep ibda /data/3306/my.cnf
innodb_data_file_path = ibdata1:128M:autoextend
[root@db01 ~]# grep ibdata /data/3306/my.cnf
innodb_data_file_path = ibdata1:128M:autoextend

innodb_data_file_path = ibdata1:1G:ibdata2:1G:autoextend

innodb_file_per_table = 1      独立表空间

innodb_buffer_pool_size = 2048M















169. ** innodb特点：面试必答项**

1、支持事务：支持4个事务隔离级别，支持多版本读
2、行级锁定（更新时一般是锁定当前行）：通过索引实现，全表扫描仍然会是表锁
3、读写阻塞与事务隔离级别相关
4、具有非常高效的缓存特性：能缓存索引，也能缓存数据
5、整个表和主键以Cluster方式存储，组成一颗平衡树
6、所有Secondary Index都会保存主键信息
7、支持分区，表空间，类似Oracle数据库
8、支持外键约束，5.5以前不支持全文索引，以后支持
9、InnoDB对硬件资源要求比较高



1、row-level locking
2、full-text search indexes
3、data caches
4、index caches
5、transactions
6、占用资源多
7、读写阻塞与事务隔离级别相关
8、支持外键
















170. ** innoDB引擎适用的生产业务场景**

1、需要事务支持的业务（具有较好的事务特性）
2、行级锁定对高并发有很好的适应能力，但需要确保查询是通过索引完成
3、数据读写及更新都较为频繁的场景，如：BBS,SNS，微博，微信等
4、数据一致性要求较高的业务，例如：充值转账，银行卡转账
5、硬件设备内存较大，可以利用InnoDB较好的缓存能力来提高内存利用率，尽可能减少磁盘IO





171. ** InnoDB引擎调优精要**

1、主键尽可能小，避免给Secondary index带来过大的空间负担
2、建立有效索引避免全表扫描，因为会使用表锁
3、尽可能缓存所有的索引和数据，提高响应速度，减少磁盘IO消耗
4、在大批量小插入的时候，尽量自己控制事务而不要使用autocommit自动提交。有开关可以控制提交方式
5、合理设置innodb_flush_log_at_trx_commit参数值，不要过度追求安全性
   如果innodb_flush_log_at_trx_commit的值为0，log buffer 每秒就会被刷写日志文件到磁盘，提交事务的时候不做任何操作
6、避免主键更新，因为这会带来大量的数据移动







grep -i innodb my.cnf
innodb_additional_mem_pool_size = 16M
innodb_buffer_pool_size = 2048M
innodb_data_file_path = ibdata1:1024M:autoextend
innodb_file_io_threads = 4
innodb_thread_concurrency = 8
innodb_flush_log_at_trx_commit = 2
innodb_log_buffer_size = 16M
innodb_log_file_size = 128M
innodb_log_files_in_group = 3
innodb_max_dirty_pages_pct = 90
innodb_lock_wait_timeout = 120
innodb_file_per_table = 0
innodb_file_per_table
innodb_data_home_dir = /data/xxx
innodb_log_group_home_dir=/data/xxx



show variables like '%innodb_%';






172. ** 不同的引擎如何备份？混合引擎如何备份。**

myisam或者混合:
mysqldump -uroot -poldboy123 -A -x -B -F –R --master-data=2 |gzip >/data/bak$(date +%F).sql.gz
innodb:
mysqldump -uroot -poldboy123 -A -B -F –R --master-data=2 --single-transaction |gzip >/data/bak$(date +%F).sql.gz


173. ** 引擎查看**

mysql> show engines;
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+
| Engine             | Support | Comment                                                        | Transactions | XA   | Savepoints |
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+
| MEMORY             | YES     | Hash based, stored in memory, useful for temporary tables      | NO           | NO   | NO         |
| CSV                | YES     | CSV storage engine                                             | NO           | NO   | NO         |
| MRG_MYISAM         | YES     | Collection of identical MyISAM tables                          | NO           | NO   | NO         |
| BLACKHOLE          | YES     | /dev/null storage engine (anything you write to it disappears) | NO           | NO   | NO         |
| MyISAM             | YES     | MyISAM storage engine                                          | NO           | NO   | NO         |
| InnoDB             | DEFAULT | Supports transactions, row-level locking, and foreign keys     | YES          | YES  | YES        |
| ARCHIVE            | YES     | Archive storage engine                                         | NO           | NO   | NO         |
| PERFORMANCE_SCHEMA | YES     | Performance Schema                                             | NO           | NO   | NO         |
| FEDERATED          | NO      | Federated MySQL storage engine                                 | NULL         | NULL | NULL       |
+--------------------+---------+----------------------------------------------------------------+--------------+------+------------+

174. ** Innodb引擎重要参数：**

innodb_additional_mem_pool_size = 4M  #用来设置InnoDB存储的数据目录信息和其他内部数据结构的内存池大小。应用程序里的表越多，你需要在这里面分配越多的内存。对于一个相对稳定的应用，这个参数的大小也是相对稳定的，也没有必要预留非常大的值。如果InnoDB用广了这个池内的内存，InnoDB开始从操作系统分配内存，并且往MySQL错误日志写警告信息。默认为1MB，当发现错误日志中已经有相关的警告信息时，就应该适当的增加该参数的大小。

innodb_buffer_pool_size = 64M  #InnoDB使用一个缓冲池来保存索引和原始数据，设置越大，在存取表里面数据时所需要的磁盘I/O越少。强烈建议不要武断地将InnoDB的Buffer Pool值配置为物理内存的50%~80%，应根据具体环境而定。

innodb_data_file_path = ibdata1:128M:autoextend  #设置配置一个可扩展大小的尺寸为128MB的单独文件，名为ibdata1.没有给出文件的位置，所以默认的是在MySQL的数据目录内。

innodb_file_io_threads = 4  #InnoDB中的文件I/O线程。通常设置为4，如果是windows可以设置更大的值以提高磁盘I/O

innodb_thread_concurrency = 8  #你的服务器有几个CPU就设置为几，建议用默认设置，一般设为8。

innodb_flush_log_at_trx_commit = 1  #设置为0就等于innodb_log_buffer_size队列满后在统一存储，默认为1，也是最安全的设置。

innodb_log_buffer_size = 2M  #默认为1MB，通常设置为8~16MB就足够了。

innodb_log_file_size = 32M  #确定日志文件的大小，更大的设置可以提高性能，但也会增加恢复数据库的时间。

innodb_log_files_in_group = 3  #为提高性能,MySQL可以以循环方式将日志文件写到多个文件。推荐设置为3。

innodb_max_dirty_pages_pct = 90  #InnoDB主线程刷新缓存池中的数据。
innodb_lock_wait_timeout = 120  #InnoDB事务被回滚之前可以等待一个锁定的超时秒数。InnoDB在它自己的锁定表中自动检测事务死锁并且回滚事务。InnoDB用locak tables 语句注意到锁定设置。默认值是50秒。

innodb_file_per_table = 0  #InnoDB为独立表空间模式，每个数据库的每个表都会生成一个数据空间。0关闭，1开启。














28. ** 表空间**

![图片](https://images-cdn.shimo.im/QcTbmPiTKvwxIuR0/image.image/png!thumbnail)

175. ** 共享表空间**

查看共享表空间
mysql> show variables like '%innodb_data_file%';
+-----------------------+------------------------+
| Variable_name         | Value                  |
+-----------------------+------------------------+
| innodb_data_file_path | ibdata1:12M:autoextend |
+-----------------------+------------------------+


设置共享表空间
[mysqld]
innodb_data_file_path=ibdata1:50M;ibdata2:50M:autoextend






2018-04-08 17:04:16 15141 [ERROR] InnoDB: Data file ./ibdata1 is of a different size 768 pages (rounded down to MB) than specified in the .cnf file 3200 pages!

```
echo 768*16/1024 |bc
12
```


[mysqld]
innodb_data_file_path=ibdata1:12M;ibdata2:50M:autoextend




176. ** 独立表空间模式**

1、除了系统表空间之外，InnoDB还在数据库目录中创建另外的表空间，用于每个InnoDB表的.ibd文件
2、InnoDB创建的每个新表在数据库目录中设置一个.ibd文件来搭配表的.frm文件。
3、可以使用innodb_file_per_table选项控制此设置
4、更改该设置仅会更改已创建的新表的默认值。

innodb_file_per_table=0   #InnoDB为独立表空间模式，每个数据库的每个表都会生成一个数据空间。0  关闭 ，  1  开启

MySQL5.6 默认开启独立表空间模式
mysql> show variables like '%innodb_file_per%';
+-----------------------+-------+
| Variable_name         | Value |
+-----------------------+-------+
| innodb_file_per_table | ON    |
+-----------------------+-------+






独立表空间优点：
1、每个表都有自己独立的表空间
2、每个表的数据和索引都会存在自己的表空间中
3、可以实现单表在不同的数据库中移动
4、空间可以回收（除drop table操作外，表空间不能自己回收）





![图片](https://images-cdn.shimo.im/XJAoJsIfNDkQvbkU/image.image/png!thumbnail)


177. **  使用表空间模拟数据恢复**

1、创建一个表结构相同的表
create table city_bak as select * from city;

2、删除新创建表的表空间
alter table t1 discard tablespace;

表空间文件消失
[root@db01 lufei]# ls /application/mysql/data/lufei/
db.opt  t1.frm

3、拷贝备份数据文件（ibd文件）到当前数据库目录并授权
[root@db01 lufei]# cp /backup/full/lufei/t1.ibd /application/mysql/data/lufei/
[root@db01 lufei]# chown -R mysql.mysql /application/mysql/data/lufei/t1.ibd
[root@db01 lufei]# ls /application/mysql/data/lufei/
db.opt  t1.frm  t1.ibd

4、导入表空间
alter table t1 import tablespace;








29. **  修改引擎**

mysql> **ALTER TABLE student  ENGINE = MyISAM;**
Query OK, 9 rows affected (0.21 sec)
Records: 9  Duplicates: 0  Warnings: 0


178. ** 使用sed对备份内容进行引擎转换**

mysqldump  > oldboy_1.sql
nohup sed -e 's#MyISAM#InnoDB#g' oldboy.sql > oldboy_1.sql &
mysql < oldboy_1.sql


独立命令：
mysql_convert_table_format  --user=root --password=oldboy123 --socket=/data/3306/mysql.sock --engine=MyISAM oldboy t2
依赖：yum -y install perl-DBI perl-DBD-MySQL perl-Time-HiRes

179. **生产环境中如何批量更改mysql引擎**

   一般来说这样的需求不多见，但偶尔也会有，在这里我们推荐使用sed对备份内容进行引擎转换的方式，当然了，不要忘了修改my.cnf使之支持并能高效的使用对应的引擎

mysq命令语句修改
创建后引擎的更改，5.0以上
alter table oldboy engine=innodb;
alter table oldboy engine=myisam;




30. ** 数据库事务**

     简单的说，事务就是指逻辑上的一组sql语句操作，组成这组操作的各个sql语句，
执行时要么全成功要么全失败
例如：oldboy给oldgirl转账5块钱，流程如下
a、从oldboy银行卡取出5块，计算式money-5
b、把上面5块钱打入oldgirl的账户上，oldgirl收到5块，money+5
上述转账的过程，对应的sql语句为
   update oldboy_account set money=money-5 where name='oldboy';
   update oldgirl_account set money=money+5 where name='oldgirl';

**事务只针对DML语句**



180. ** 事务的四大特性（ACID）**

1、原子性（**Atomicity**）
事务是一个不可分割的单位，事务中的所有sql等操作要么都发生，要么都不发生
原子（atom）指化学反应不可再分的基本微粒，原子在化学反应中不可分割
2、一致性（**Consistency**）
事务发生前和发生后，数据的完整性必须保持一致
3、隔离性(**Isolation**)
当并发访问数据库时，一个正在执行的事务在执行完毕前，对于其它的会话是不可见的，多个并发事务之间的数据是相互隔离的。还记得备份的参数么  --single-transaction
4、持久性（Durability）
  一个事务一旦被提交，它对数据库中的数据改变就是永久性的。如果出了错误，事务也不允许撤销，只能通过“补偿性事务”



181. ** 事务提交和事务回滚**

set global autocommit=on   开启自动提交
rollback   回滚事务
commit    提交事务
提示：事务引擎基于表的，所以要在表上插入、更新测试事务的特性




mysql> show global variables like "%autocommit%";
+---------------+-------+
| Variable_name | Value |
+---------------+-------+
| autocommit    | ON    |
+---------------+-------+
1 row in set (0.00 sec)

mysql> set global autocommit=Off;


182. ** MYSQL的事务控制语句**

START TRANSACTION（或BEGIN）：显式开始一个新事务
SAVEPOINT：分配事务过程中的一个位置，以供将来引用
ROLLBACK：取消当前事务所做的更改
ROLLBACK TO SAVEPOINT：取消在savepoint之后执行的更改
RELEASE SAVEPOINT：删除savepoint标识符
COMMIT：永久记录当前事务所做的更改
SET AUTOCOMMIT：为当前连接禁用或启用默认autocommit模式


183. ** 设置自动提交（关闭）**

永久设置 
/etc/my.cnf 
autocommit=0
临时设置
mysql> set session  autocommit=0;
mysql> set global autocommit=0;






184. ** 事务日志redo**

Redo是什么？
–redo,顾名思义“重做日志”，是事务日志的一种。
作用是什么？
–在事务ACID过程中，实现的是“D”持久化的作用。

redo日志两个文件
ib_logfile0  ib_logfile1

redo 记录页的变化信息

![图片](https://images-cdn.shimo.im/v924Pskc7q87HoyR/image.image/png!thumbnail)








185. ** 事务日志undo**

回滚段
事务槽

undo是什么？
–undo,顾名思义“回滚日志”，是事务日志的一种。
作用是什么？
–在事务ACID过程中，实现的是“C”一致性的作用。

undo 记录页变化之前的数据（快照）

![图片](https://images-cdn.shimo.im/90q0ZHeMvRANNjgz/image.image/png!thumbnail)






186. ** 事务中的锁**

什么是'锁'？
–'锁'顾名思义就是锁定的意思。
'锁'的作用是什么？
–在事务ACID过程中，“锁”和“隔离级别”一起来实现“I”隔离性的作用

![图片](https://images-cdn.shimo.im/4dWV0KkIjugdnDQ1/image.image/png!thumbnail)

锁的粒度：
1、MyIasm：低并发锁——表级锁
2、Innodb：高并发锁——行级锁





四种隔离级别
[mysqld]
transaction-isolation = REPEATABLE-READ

READ UNCOMMITTED
–允许事务查看其他事务所进行的未提交更改

READ COMMITTED
–允许事务查看其他事务所进行的已提交更改

REPEATABLE READ******
–确保每个事务的SELECT 输出一致
–InnoDB的默认级别

SERIALIZABLE
–将一个事务的结果与其他事务完全隔离



































# **mysql 备份**
https://www.percona.com



187. ** 备份数据作用**

1、恢复数据到测试库的时候
2、人为通过SQL语句将数据删除的时候
3、做数据库主从复制的时候

188. ** 物理备份**

直接复制的数据库文件，恢复比较快
XtraBackup

189. ** 逻辑备份**

逻辑备份指备份出的文件是可读的，一般为文本文件。
常用备份工具：mysqldump
就是以SQL语句的形式，将数据导出成文件
优点：简单、方便、可靠
      导出的数据可以跨平台、跨版本、跨软件
缺点：速度慢
mysqldump是mysql官方自带的逻辑备份工具，还能实现分库分表备份
应用场景：
      1、适用于数据量不是特别大的场景，打包前50G以内的数据库数据
      2、跨版本、系统升级时候用mysqldump迁移数据

全量备份  -----  mysqldump

增量备份  -----  binlog日志
启用：
log-bin = mysql-bin
sync-binlog = 1
innodb_support_xa = 1



31. ** 逻辑备份—mysqldump命令**

mysqldump重要参数说明
**-B**, --databases   在备份数据中增加建库及use库的语句，同时可以直接接多个库名，备份多个库
-A, --all-databases  备份所有的数据库
**-d**                只备份表结构（sql语句形式）
**-t **               只备份表数据（sql语句形式）
-T               将库表和数据分离成不同的文件，数据是纯文本，表结构是SQL语句
**-F**，--flush-logs    刷新binlog日志，生成新binlog文件
**--master-data**={1|2}  在备份结果中增加binlog日志文件名及对应的binlog位置点（即
                  change master...语句）值为1 ，不注释 ，  值为2， 注释
                  此参数执行时会打开--lock-all-tables功能，除非有--single-transaction在，使用此
                  参数时会关闭--lock-tables功能
-x，--lock-all-tables  备份时对所有数据库的表执行全局读锁
-l，--lock-tables     锁定所有的表为只读
**--single-transaction**   在备份innodb引擎数据表时，通常启用该选项来获取一个一致性的数据快照
                  备份，它的工作原理是设定本次备份会话的隔离级别为REPEATABLE READ,
                   并将整个备份放在一个事务中，以确保执行本次dump会话时，不会看到其他
                   连接会话已经提交了的数据，即备份开始时刻的数据是什么样备份出来就是
                    什么样子，也就相当于锁表备份数据，但是这个参数允许备份期间写入数据
**-R**，--routines      备份存储过程和函数数据
**--triggers **          备份触发器数据
--compact          只显示很少的有用输出，适合学习和测试环境调试用
-c, --complete-insert  使用包含列名称的完整INSERT语句
-e, --extended-insert  使用多行INSERT语法

   mysqldump命令可以将数据库中的数据备份成一个文本文件。表的结构和表中的数据将存储在生成的文本文件中。

mysqldump命令需要权限：
select, show  view  trigger   lock  tables
备份：
mysqldump  参数  >file_name.sql




mysql> select concat("mysqldump"," -uroot -p123456 " ,table_schema," ",table_name, " ",">/backup/",table_name,".sql") from information_schema.tables;

## 只导出表结构
```
mysqldump  -d --triggers=false>xx.sql
```

## 只导数据
```
mysqldump  -t --triggers=false>xx.sql
```

## 只导出触发器
```
mysqldump  -tdn  --triggers>xx.sql
```

## 只导出存储过程
mysqldump  -Rtdn --triggers=false>xx.sql
特别关注
--single-transaction
--master-data=1|2   是否加入change  master信息
--where=name
-c, --complete-insert  使用包含列名称的完整INSERT语句
-e, --extended-insert  使用多行INSERT语法

mysqldump  -S /data/3306/mysql.sock -t -c -e --single-transaction --master-data=2 --triggers=false  oldboy student --where "name='oldboy'"  -uroot -poldboy  > student_data.sql


mysqldump --master-data=2 **-B** oldboy|gzip>/opt/oldboy.sql.gz


single-transaction:
针对innodb引擎表，可以不锁表，在一个事物中拿到一个一致性快照
（1） set session transaction isolation level repeatable read
    使当前session的事物级别为可重复读
（2）start  transaction  /*!40100 with consistent snapshot */
  开始一个事物并且获得一个一致性快照，获得最新的LSN
（3）unlocktables
   释放锁，这也解释了为什么说使用mysqldump不会锁表







190. ** myisam引擎企业生产备份命令（适合所有引擎或混合引擎）:**
```
mysqldump -uroot -poldboy123 -S /data/3306/mysql.sock -A -B -R --master-data=2 -x |gzip >/opt/alL__$(date +%F).sql.sql.gz
```
提示：-F也可以不用，与--master-data有些重复。



191. ** innodb引擎企业生产备份命令:推荐使用的**
```
mysqldump -uroot -poldboy123 -S /data/3306/mysql.sock -A -B -R --master-data=2 --single-transaction |gzip >/opt/alL__$(date +%F).sql.sql.gz
```


192. ** 备份单表**
```
mysqldump  dbname  tablename  > dbname_tablename.sql
```


193. ** 备份多个库**
```
mysqldump -B  dbname1 dbname2  > db.sql
```



194. ** 备份一个库的多个表**
```
mysqldump  dbname  tablename1  tablename2  tablename3  > dbname_tablename.sql
```



```
select concat("mysqldump ",table_schema," ",table_name," >/data/backup/",table_schema,"_",table_name,".sql") from information_schema.tables where table_schema not in('sys','information_schema','performance_schema') into outfile '/tmp/mysqldump.sh';
```



32. ** 数据库恢复**
195. ** sql文件恢复**

set sql_log_bin=0
source /opt/new.sql
导入windows  下 sql文件
cat new.sql
set names utf8;
use oldboy
insert into test(name) values('小陶');
**提示：如果UTF8数据库，人工编辑的SQL文件，格式建议为“UTF8没有签名”格式**





196. ** binlog文件恢复**

二进制日志非常关键：
1、完成时间点的数据库恢复
2、数据库的复制需要
Tip: 备份二进制之前可以执行flush logs  生成一个新的二进制日志文件，然后备份之前的二进制文件，而且如果进行数据库全备之前执行flush logs  ，  恢复时不需要去定位日志的起点

恢复方法：
mysqlbinlog mysql-bin.0000001|mysql -uroot -p database
mysqlbinlog mysql-bin.000000[1-9] |mysql -uroot -p database

mysqlbinlog** ****-d test** mysql-bin.000001 > /tmp/test.sql








197. ** 数据恢复演练**

use world
update city set countrycode='CHN' where countrycode='JPN';
delete from city where countrycode ='USA';
delete from city where countrycode <> 'CHN';
delete from city where name='tokyo';

要求：恢复到tokyo被删除之前的状态。





# **mysql配置文件**
[mysqld]
skip_name_resolve = 1
socket  = /application/mysql-5.6.34/tmp/mysql.sock
open_files_limit  = 65535
max_connections = 512
max_connect_errors = 1000000
external-locking = FALSE
server-id = 3306
log-bin = /application/mysqlbinlog/mybinlog
sync_binlog = 1
binlog-ignore-db = mysql
binlog_cache_size = 4M
max_binlog_size = 1G
expire_logs_days = 7
innodb_buffer_pool_size = 128M
performance_schema_max_table_instances = 200
table_definition_cache = 200
table_open_cache = 128




# **mysql优化**
[https://dev.mysql.com/doc/refman/5.7/en/optimization.html](https://dev.mysql.com/doc/refman/5.7/en/optimization.html)
## **硬件层面优化**
  1.1 数据库物理机采购：
  1.2 服务器硬件配置调整
    1.2.1 服务器BIOS调整：
    1.2.2 阵列卡调整：

## **操作系统层面优化**
    2.1.1 操作系统及MySQL实例选择
    2.1.2 文件系统层优化 
    2.1.3 linux内核参数优化 
  2.2 mysql数据库层面优化
    2.2.1 my.cnf参数优化
    2.2.2 关于库表的设计规范


# **SQL语句的优化**
## **现场抓慢查询sql语句**
  紧急且重要 ：show full processlist; （登录数据库现场抓，连续执行2次，超过2秒）
mysql -S /data/3306/mysql.sock -uroot -poldboy -e "show full processlist;"|grep -vi "sleep"

1、
mysql> show full processlist;

2、explain 语句检查索引执行情况
explain select * from test where name='oldboy'\G;
explain select SQL_NO_CACHE * from test where name='oldboy'\G;

1）查看已经创建的索引情况
show index from test\G;



2）统计表记录的唯一值
select count(distinct name) from test;


3）通过唯一值的数量找出需要建索引的列，对需要建立索引的条件列建立索引
   生产场景，大表高峰期不能建立索引，（300万条记录以上）

alter table test add index index_name(name);










**建索引前后的对比**
建索引前：
mysql> explain select * from test where name='zuma'\G;
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

建索引后
mysql> explain select * from test where name='zuma'\G;
*************************** 1. row ***************************
           id: 1
  select_type: SIMPLE
        table: test
         type: ref
possible_keys: index_name
          key: index_name
      key_len: 60
          ref: const
         rows: 1
        Extra: Using where; Using index
1 row in set (0.00 sec)

4） 慢查询语句发给开发人员

















## **平时抓慢查询sql语句**
重要不紧急：记录以及分析慢查询日志
1、配置参数记录慢查询语句
slow_query_log = on
long_query_time = 1                  #超过1秒，记录到slow log 里
log_queries_not_using_indexes         # 没有走索引的语句，slow log 里
log-slow-queries = /data/3306/slow.log   # slow log 文件
min_examined_row_limit = 1000       #记录查询结果大于1000条的sql语句

2、 按天切割慢查询日志，如果并发太大可以按小时
1）mv 然后flush进程
2）cp复制，然后利用>清空
3）定时任务
mv /data/3306/slow.log /opt/$( date +%F)_slow.log
mysqladmin -uroot -poldboy -S /data/3306/mysql.sock flush-logs


[分析mysql慢查询日志的好工具--mysqlsla](http://blog.itpub.net/7607759/viewspace-692828/) 
http://blog.itpub.net/7607759/viewspace-692828

慢查询日志工具
pt-query-digest   mysqldumpslow  mysqlsla  myprofi  mysql-explain-slow-log  mysqllogfilter







## **mysql  profiler**
http://www.cnblogs.com/ggjucheng/archive/2012/11/15/2772058.html

MySQL 的 Query Profiler 是一个使用非常方便的 Query 诊断分析工具，通过该工具可以获取一条Query 在整个执行过程中多种资源的消耗情况，如 CPU，IO，IPC，SWAP 等，以及发生的 PAGE FAULTS，CONTEXT SWITCHE 等等，同时还能得到该 Query 执行过程中 MySQL 所调用的各个函数在源文件中的位置

开启profiling
mysql> set profiling=1;
Query OK, 0 rows affected, 1 warning (0.00 sec)


查询
mysql> show profiles;
+----------+------------+----------------+
| Query_ID | Duration   | Query          |
+----------+------------+----------------+
|        1 | 0.00026025 | show profiling |
+----------+------------+----------------+
1 row in set, 1 warning (0.00 sec)

mysql> show profile cpu for query 1;
+---------------+----------+----------+------------+
| Status        | Duration | CPU_user | CPU_system |
+---------------+----------+----------+------------+
| starting      | 0.000220 | 0.000000 |   0.000000 |
| freeing items | 0.000031 | 0.000000 |   0.000000 |
| cleaning up   | 0.000009 | 0.000000 |   0.000000 |
+---------------+----------+----------+------------+
3 rows in set, 1 warning (0.00 sec)




mysql> show profile memory for query 1;
+---------------+----------+
| Status        | Duration |
+---------------+----------+
| starting      | 0.000220 |
| freeing items | 0.000031 |
| cleaning up   | 0.000009 |
+---------------+----------+
3 rows in set, 1 warning (0.00 sec)


mysql> show profile cpu,memory,block io for query 1;
+---------------+----------+----------+------------+--------------+---------------+
| Status        | Duration | CPU_user | CPU_system | Block_ops_in | Block_ops_out |
+---------------+----------+----------+------------+--------------+---------------+
| starting      | 0.000220 | 0.000000 |   0.000000 |            0 |             0 |
| freeing items | 0.000031 | 0.000000 |   0.000000 |            0 |             0 |
| cleaning up   | 0.000009 | 0.000000 |   0.000000 |            0 |             0 |
+---------------+----------+----------+------------+--------------+---------------+
3 rows in set, 1 warning (0.00 sec)


3、网站集群架构上的优化
4、流程，制度，安全优化










## **纵向拆表**


创建新表
CREATE TABLE `country_1` (
  `Code` char(3) NOT NULL DEFAULT '',
  `Name` char(52) NOT NULL DEFAULT '',
  `Continent` enum('Asia','Europe','North America','Africa','Oceania','Antarctica','South America') NOT NULL DEFAULT 'Asia',
  PRIMARY KEY (`Code`),
  KEY `name_idx` (`Name`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1

从旧表导入数据到新表
insert into country_1(code,name,continent) select code,name,continent from country;


## **横向拆表**

create table country_1_p1 like country_1;

insert into country_1_p1 select code,name,continent from country_1 order by code limit 100;

create table country_1_p2 like country_1;

insert into country_1_p2 select code,name,continent from country_1 order by code limit 139 offset 100;
