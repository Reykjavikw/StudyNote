**MySQL（解压版）下载及安装**

+ 进入MySQL下载官网:https://dev.mysql.com/downloads/mysql/

  <!--5.8版本后开始收费-->

  ![image-20200125193901643](C:\Users\Dell\AppData\Roaming\Typora\typora-user-images\image-20200125193901643.png)

+ **配置环境变量**

  新增系统环境变量：

  键名：Path

  值为：mysql下载位置的bin目录，注意Path中不同值之间的“；”符号不能省略

------

1. 准备好`my.ini`文件，可以先新建一个`my.txt`文件，然后通过重命名修改文件后缀为`.ini`，以前的版本解压后或许会存在my.ini文件，但是5.7.21版本没有，因此要自己手动创建该文件，文件的内容如下：



```csharp
[client]
port=3306
default-character-set=utf8

[mysql] 
default-character-set=utf8 

[mysqld] 
port = 3306 
basedir=D:/mysql-5.7.25-winx64
datadir=D:/mysql-5.7.25-winx64/data  
collation-server = utf8_unicode_ci
init-connect='SET NAMES utf8'
character-set-server = utf8
max_connections=200 
default-storage-engine=INNODB 
sql_mode=NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES 
```

​	此步骤要注意：红框内为MySQL的安装路径，并且文件夹之间用`“/”`而不是`“\”`分隔,否则在下面的操作中可能会出错

![img](https:////upload-images.jianshu.io/upload_images/7236178-37dfb303e157dc83.png?imageMogr2/auto-orient/strip|imageView2/2/w/511/format/webp)

​	**此配置文件中默认设置的是UTF-8的编码方式**
​	 编辑好`my.ini`文件之后，将`my.ini`文件放到你的安装目录下

------

2. 以管理员身份打开cmd命令窗口，将目录切换到MySQL的安装目录的bin目录下

------

3. 执行以下语句进行MySQL的安装



```undefined
mysqld -install
```

​	执行命令后提示：`Service successfully installed.` 表示安装成功

------

4. 执行以下语句进行MySQL的初始化my



```undefined
mysqld --initialize-insecure --user=mysql 
```

​	执行命令后会在MySQL的安装目录下生成data目录并创建root用户。

![img](https:////upload-images.jianshu.io/upload_images/7236178-8878bd3769ca4e28.png?imageMogr2/auto-orient/strip|imageView2/2/w/650/format/webp)

------

5. 执行以下命令以启动mysql服务



```undefined
net start mysql
```

​	执行后会有如下提示：

```
MySQL服务正在启动..
MySQL服务已经启动成功.
```

6. 启动MySQL之后，root用户的密码为空，设置密码，命令如下：



```undefined
mysqladmin -u root -p password 新密码 
Enter password: 旧密码
```

​	需要输入旧密码时，由于旧密码为空，所以直接回车即可。

7. 修改密码（必须先启动mysql），执行如下命令回车，enter password也回车，密码一般设置为root，方便记忆

	mysqladmin -u root -p password

8. 退出exit 就行了，记住直接关闭cmd窗口是没有退出的，要输入exit才会退出啊
   	

	exit

9. Navicat图形化界面连接mysql

10. 解压Navicat 12 for MySQL到指定路径，直接运行exe文件即可

