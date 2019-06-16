# MySQL5.7二进制安装

标签（空格分隔）： 数据库

---

# 1.安装依赖,解压mysql二进制包到/usr/local/ ,并创建软链接mysql

```bash
yum install bison-devel ncurses-devel libaio-devel
```

# 2.添加mysql环境变量

```bash
vim /etc/profile.d/mysql.sh 
export PATH=/usr/local/mysql/bin:$PATH
```

# 3.创建mysql用户

```bash
useradd -s /sbin/nologin mysql -M
```

# 4.授权

```bash
chown -R mysql.mysql /usr/local/mysql/
```

# 5.初始化MySQL数据库

```bash
mysqld --initialize-insecure --user=mysql --basedir=/usr/local/mysql --datadir=/usr/local/mysql/data
```

# 6.systemd管理MySQL

```vim
vim /etc/systemd/system/mysqld.service 
[Unit]
Description=MySQL Server
Documentation=man:mysqld(8)
Documentation=http://dev.mysql.com/doc/refman/en/using-systemd.html
After=network.target
After=syslog.target

[Install]
WantedBy=multi-user.target

[Service]
User=mysql
Group=mysql
ExecStart=/usr/local/mysql/bin/mysqld --defaults-file=/etc/my.cnf
LimitNOFILE = 5000
```

# 7.重新加载systemd

```bash
systemctl daemon-reload
```

# 8.配置文件

```vim
vim /etc/my.cnf
[mysqld]
basedir=/usr/local/mysql
datadir=/usr/local/mysql/data
user=mysql
log-error=/usr/local/mysql/data/error.log
```

# 9.启动MySQL

```bash
systemctl start mysqld.service
```
