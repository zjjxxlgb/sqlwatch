# easysql
A tool can check the sql syntax and find the tables which been modified.


功能：
定制mysql源码，输入SQL文件进行SQL语法检查，并识别出哪些表有变更，提高SQL上线时备份的效率。


SQL语法检查:
sqlwatch \<test.sql 2\>&1|grep ERROR

SQL变更表识别:
sqlwatch \<test.sql 2\>&1|grep dbtablename

编译安装

yum install cmake

yum install perl

yum install perl-DBD*

yum install libaio.so.1

yum install *CPAN*

yum install *libaio*

yum install *Curses*

yum install ncurses-devel

yum install ksh

useradd -m -d /home/mysql -u 202 -g dba mysql

mkdir -p /data0/mysql2/dbdata进入

 进入源码目录
 
cmake -DCMAKE_INSTALL_PREFIX=/data0/mysql/ -DMYSQL_DATADIR=/data0/mysql2/dbdata -DMYSQL_UNIX_ADDR=/data0/mysql2/dbdata/mysql.sock -DSYSCONFDIR=/data0/mysql2/dbdata/config -DDEFAULT_CHARSET=utf8 -DDEFAULT_COLLATION=utf8_general_ci -DEXTRA_CHARSETS=all -DWITH_DEBUG=0 -DENABLED_LOCAL_INFILE=1 -DWITH_INNOBASE_STORAGE_ENGINE=1 -DWITH_PARTITION_STORAGE_ENGINE=1

重命名 mysqld为sqlwatch

