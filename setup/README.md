##下载或更新依赖包##
````Bash
yum update openssl
````
##生成密码##
````Bash
/usr/local/mysql-proxy/bin/encrypt 123456
````
##将密码加入到配置文件中##
````Bash
vi /usr/local/mysql-proxy/conf/test.cnf
````
![修改之后](https://raw.githubusercontent.com/piggsoft/Atlas-reseach/master/res/1.png)
##运行Atlas##
进入/usr/local/mysql-proxy/bin目录，执行下面的命令启动、重启或停止Atlas。

(1).	sudo ./mysql-proxyd test start，启动Atlas。

(2).	sudo ./mysql-proxyd test restart，重启Atlas。

(3).	sudo ./mysql-proxyd test stop，停止Atlas。

**注意：**

(1).	运行文件是：mysql-proxyd(不是mysql-proxy)。

(2).	test是conf目录下配置文件的名字，也是配置文件里instance项的名字，三者需要统一。

(3).	可以使用ps -ef | grep mysql-proxy查看Atlas是否已经启动或停止。
##测试运行状态##
执行命令：mysql -h127.0.0.1 -P1234 -u用户名 -p密码，如果能连上则证明Atlas初步测试正常，可以再尝试发几条SQL语句看看执行结果是否正确。

进入Atlas的管理界面的命令：mysql -h127.0.0.1 -P2345 -uuser -ppwd，进入后执行:select * from help;查看管理DB的各类命令。

##遇到的问题##
* 使用mysql -h127.0.0.1 -P1234 -u用户名 -p密码，可以进入client环境，但是执行sql出现错误。
    ERROR 2006 (HY000): MySQL server has gone away    
    No connection. Trying to reconnect...  
    Connection id:4  
    Current database: *** NONE ***  
    ERROR 2013 (HY000): Lost connection to MySQL server during query  
查看log发现错误原因是：
````(critical) proxy-plugin.c.1450: I have no server backend, closing connection````  
尝试将/usr/local/mysql-proxyd/conf/test.cnf中的backendserver地址改为内网IP，问题解决。  
具体的原因还需查明
