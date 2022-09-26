# 安装mysql

1. [压缩包下载地址](https://dev.mysql.com/downloads/mysql/5.5.html#downloads)  第一个

2. 解压压缩包

3. 打开文件，配置bin目录到系统环境变量

4. 新建my.ini文件

   ```
   [mysql]
   # 设置mysql客户端默认字符集
   default-character-set=utf8
   [mysqld]
   # 设置3306端口
   port = 3306
   # 设置mysql的安装目录
   basedir = D:\\mysql\\mysql-8.0.17-winx64
   # 设置mysql数据库的数据的存放目录
   datadir = D:\\mysql\\mysql-8.0.17-winx64\\data
   # 允许最大连接数
   max_connections=20
   # 服务端使用的字符集默认为8比特编码的latin1字符集
   character-set-server=utf8
   # 创建新表时将使用的默认存储引擎
   default-storage-engine=INNODB
   # 创建模式
   sql_mode = NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES

​	设置mysql的安装目录

4. 进入cmd初始化mysql

   ```html
   mysqld --initialize
   ```

5. 系统会生成一个data文件夹 打开文件夹搜索找到.err后缀的文件

6. 找到用户名root 开头的 密码是localhost后面的字符

7. 在管理员cmd中输入

   ```html
    net start mysql
   ```

   

8. 输入

   ```html
   mysql -u用户名 -p密码
   ```

   

9. 第一次进入修改密码

   ```html
   alter user 'root'@'localhost' identified with mysql_native_password by ' **这里填写新密码** ';
   ```

   