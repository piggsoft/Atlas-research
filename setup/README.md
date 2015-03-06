##下载或更新依赖包##
````shell
yum update openssl
````
##生成密码##
````shell
/usr/local/mysql-proxy/bin/encrypt 123456
````
##将密码加入到配置文件中##
````shell
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
