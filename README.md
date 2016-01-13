# easysql
check the sql syntax and find the tables which been modified.


功能：
定制mysql源码，输入SQL文件进行SQL语法检查，并识别出哪些表有变更，提高SQL上线时备份的效率。


SQL语法检查:
sqlwatch <test.sql 2>&1|grep ERROR

SQL变更表识别:
sqlwatch <test.sql 2>&1|grep dbtablename
