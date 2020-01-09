# oracle
oracle相关资料



windows安装数据库完毕后，创建表空间和用户，同时给用户赋予此表空间；


CREATE TABLESPACE CARPRO  --表空间名
DATAFILE  'D:\app\liyanchao\oradata\ecapital\CARPRO01.dbf'   --表空间对应的数据文件
SIZE 100M  --数据文件大小
AUTOEXTEND ON NEXT 10M  --数据文件不够用自动扩展，每次扩展大小
MAXSIZE 2048M   --数据文件最大文件大小
LOGGING   --启动重做日志
PERMANENT --指定表空间为永久性的表空间
EXTENT MANAGEMENT LOCAL   --指定新建表空间为本地管理方式的表空间
SEGMENT SPACE MANAGEMENT auto    --指定本地管理表空间中段的存储管理方式，AUTO自动，MANUAL手工。



create temporary tablespace CARPRO_TEMP
tempfile 'D:\app\liyanchao\oradata\ecapital\CARPR_TEMP.dbf'
SIZE 100M  --数据文件大小
AUTOEXTEND ON NEXT 10M  --数据文件不够用自动扩展，每次扩展大小
MAXSIZE 2048M   --数据文件最大文件大小
EXTENT MANAGEMENT LOCAL   --指定新建表空间为本地管理方式的表空间



create user CARPRO identified by 123456;
